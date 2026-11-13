# November 4, 2026 · Office hours with Kathleen McKeown

**Participants** · Peter Driscoll and Kathleen McKeown  
**Project** · Learning a representation of harm in JEP testimony  
**Source** · Local recording metadata dates this 12m36s clip to November 4 at 7:11 p.m. New York time. It begins mid-sentence. The edited dialogue follows the saved machine transcript. Speaker labels are inferred, uncertain wording is marked, and personal asides are omitted from this public edition.

## Summary

McKeown wanted to see a passage, the harm it expressed and the expert marking that connected the two. The codebook Peter showed her defined categories. Whether the team had passages labeled with those categories remained open. She suggested setting aside around fifty examples for a class evaluation and considering natural language inference when the harm is implicit.

| Question | What the discussion established |
| --- | --- |
| What can human examples do? | Clarify the task for the researcher, illustrate it in a prompt, support fine-tuning if enough accumulate, and supply independent evaluation cases. McKeown advised holding some out. |
| Why consider natural language inference (NLI)? | A speaker might describe an experience without naming the harm. McKeown suggested looking into inference from the explicit words. The discussion did not specify hypotheses, labels, or an NLI training procedure. |
| What alternatives did they discuss? | Peter proposed adapting an encoder to Colombian legal Spanish and training it on broad harm similarities from other case material. McKeown suggested adapting the model to unlabeled documents from the training portion of the target corpus. |
| What was still uncertain? | How frequently harm occurs, how often people describe it in different ways, and whether existing court materials contain labeled spans. Peter's figures on transcript counts and mentions were estimates. |

**Next step and call to action.** Bring one short passage and its expert label to the joint meeting the following day. Ask the collaborators which marks already exist in the text and which would require new annotation. Set aside examples for evaluation before using other examples in prompts or training.

## Edited transcript

### 1. Defining a benchmark

**Kathleen** · [Opening unclear] to benchmark how well models can do this task. But to do that you definitely need examples of what the harms are. It sounded, as he described them, like they could be implicit in the text. They're not necessarily explicitly stated. Since they're in Colombian Spanish, there may be things specific to the culture about what kinds of harms you're likely to get, what kinds of harms occur, or how people [wording unclear].

I suggested we meet tomorrow because I talked to you one day and had one idea of what this was about, then I talked to him another day and had a different idea. There were specific things you'd need to do for the problem to make sense. [Personal assessment omitted.] I thought it best that we all talk together.

**Peter** · I'm glad you did. Initially I was trying to figure out how to do this. It's challenging and I didn't fully understand it.

**Kathleen** · If he has examples I can see, that would help. Once you see them, you have some idea whether this is doable. If they're in Colombian Spanish, I don't know Spanish. Do you?

**Peter** · Yes. [Personal aside omitted.] What you mentioned last time about visualization really helps me understand the problem. It's a question of how it's documented. They may produce clear evidence if prompted, but I don't think they're doing it for every single person. A judge makes a determination using experience. I'm not sure of the status of the annotations of the trials themselves. There are concrete findings about what harm occurred in different trials, the codebook and what was learned. I have that and I read it over.

### 2. A category definition and a labeled passage

**Kathleen** · Could you give an example now? Sometimes it's hard for me because I don't see it. Even what you show me today, I'll see it in five minutes, and there's a whole bunch more behind it.

**Peter** · They're saying emotional, mental and physical are three kinds of harm they encountered. [Spanish wording unclear.] The integrity of your physical, mental and emotional [unclear]. They give context about how these impacted the health of the victim, or [self-correction unclear].

**Kathleen** · This is the guidebook now? This isn't the example where you're identifying [the harm]?

**Peter** · This is the product of another region tasked with the same deliverable. Can you produce a codebook of the kinds of harms, reparations, restoration? This was their final output, their findings when they concluded that separate case.

**Kathleen** · How long is this?

**Peter** · Nine hundred pages.

**Kathleen** · Nine hundred pages of a codebook?

**Peter** · There's a lot more than that. It's the whole case, the process.

**Kathleen** · How long is the codebook?

**Peter** · Their definitions are three or four pages. There's a lot of context around the restorative justice process, its purpose and the dimensions and categories of pain. The literal definitions are just those pages. I just got this document a couple of hours ago. I agree that if there's a training signal from human annotations, that would be really helpful.

### 3. A held-out set and implicit harm

**Kathleen** · Examples could help you think about how to do it. For the model, are there enough for fine-tuning? There may not be. Are there enough for in-context learning, where you put multiple examples of what's needed in the prompt? Even that can improve performance. Finally, separate some out. If you're developing a model to do this, you need to measure how well it does.

Ideally you'd have, let's say, fifty examples where something in the text has been marked as harm, which you could use to evaluate the model. Fifty is small, but for a class you could do that. For a paper you'd want at least a hundred. Ideally more. [These are McKeown's estimates in the conversation.]

**Peter** · I think we will. We have about a hundred trial transcripts and there are mentions of harm throughout. I'd say roughly twenty to thirty times [unit unclear]. The approach is, “You did this to me,” and, “That's how it affected me.”

**Kathleen** · Is it said multiple times in different ways?

**Peter** · Yes.

**Kathleen** · That's very interesting too. Another method I thought of when I was talking to him, because it sounded like it could be so implicit, is whether you would use any of these NLI [natural language inference] techniques, which are intended to induce implicit meaning from explicit words.

**Peter** · That's helpful. I'll look into that. [Personal details omitted.] My colleague has been involved with the project for a year, and I want to make the most of the resources available.

### 4. Learning from Colombian legal Spanish

**Peter** · I was thinking about learning a representation reflective of harm. What if I took Colombian trial documents with different kinds of harm? In one example someone was murdered. In another someone was punched. Could I make a crude one-to-five scale of how similar those types of harm are? BERT-type pretraining on that text, then post-training on how similar the harms are. Pretrain for the language and context on Colombian Spanish trial data, and then use crude similarity based on broad types of harm. Even murder versus non-murder.

I might be able to do structured extraction where the word appears in the metadata. It's either there or in the text, or I could run it through an LLM. Assuming I could get it, would that be a useful way to build an encoder in the language and the domain, with a supervisory signal that might transfer if I didn't have the expert annotations for this dataset? That was my backup plan.

**Kathleen** · Where would the data you pretrain on come from? Or is it the same material?

**Peter** · I read the Spanish [ConfliBERT] paper, a language- and domain-specific adaptation of BERT. There's a lot of documentation from the broader criminal justice system in Colombia.

**Kathleen** · You'd use that?

**Peter** · That's what I thought might give me a transferable learning signal. It isn't a perfect match. This is restorative justice.

**Kathleen** · I think that would be good. One thing I thought you were saying was that you could start with the documents you already have. You'd want a training and a test set. Simply use the documents you have in training to fine-tune the model. It would be closer to the language you actually have, and it wouldn't need annotations.

**Peter** · It would be autoregressive, just learning the dialect. [Short exchange unclear.] I'm playing around with different things. If I can get annotated transcripts from this trial, that would be perfect.

**Kathleen** · You definitely need something. If you have nothing, no annotated statements, then you can't measure [how well the model does].
