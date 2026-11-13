# Office hours with Zach Horvitz

**Meeting date** November 13, 2026. **Participants** Peter Driscoll, Zach Horvitz, and students whose names the supplied text does not establish.

**Recording times (New York)** · Clip A began at 3:55:17 p.m. and ran 27m 16s. Clip B began at 4:34:01 p.m. and ran 25m 59s. Both were recorded November 13, 2026. Times beside section titles give the start of the Superwhisper segment containing its first words. Offsets are relative to the corresponding clip. Some segments span pauses or more than one speaker.

[Summary and action items](summary.md) · [Exact source wording with marked redactions](source-transcript.md)

**Condensed reading edition.** Dialogue has been paraphrased for readability. For quotation and verification, use the [source transcript](source-transcript.md). This edition was edited from the supplied text. Each attachment matches the saved Superwhisper output for its recording by SHA-256. “Peter” and “Zach” identify turns inferred from the project description and the surrounding exchange. “Participant” marks an unidentified voice. “Student” identifies the person describing a project within that section. Whether the same student presented both topics in Part II is unclear. Bracketed notes mark uncertain wording, interrupted speech, and condensed asides. This public reading edition retains the academic discussions and marks omissions of personal side conversations and identifying details. The statements and preliminary findings below are the speakers’ accounts at the time of the meeting.

## Part I · Learning a representation of harm

<a id="a01"></a>
### A01 · A reading suggestion and the project setting · Clip A 00:00.192

[Source wording](source-transcript.md#a01)

**Participant** — Last week, on the paper that Jessica Dai did on the … [interruption]. The paper on the three years of ChatGPT, the retrospective on Reddit. It’s relevant. Learning an SAE, you get these topics, and then maybe you can use that to surface interesting things over time. I thought that was relevant for Peter’s [project].

**Peter** — I honestly didn’t make the connection, but thank you. I’ll look at it. I just wanted to run through where I’m at. It’s the same idea. We have these testimonies from these trials, and they’re …

**Participant** — Very cool domain.

**Peter** — One thing I didn’t highlight, which is really important, is that this is operating under this idea of restorative justice. It’s a different way of viewing justice, a different ethical framework. What is right, and what is a good outcome in these situations? It’s not focused on punitive corrections, right?

**Participants** — [Personal aside omitted.]

The reading mentioned at the opening is Jessica Dai and colleagues’ *Three Years of r/ChatGPT*. [ICML paper](https://proceedings.mlr.press/v306/dai26d.html)

<a id="a02"></a>
### A02 · What Peter means by a representation of harm · Clip A 01:59.192

[Source wording](source-transcript.md#a02)

**Peter** — It’s a distinct moral framework, which I hadn’t properly appreciated. That’s why the setting of the trials was different. You have the perpetrators with the victims. They’re talking it out in this dialogue, and it’s being transcribed. [Brief exchange unclear.] I was thinking about the ethical questions and the moral aspect of the semantics. I was reading about how LLMs understand concepts like what’s right and what’s wrong, and different moral frameworks.

I wanted to learn a good embedding of harm, a good representation from the data. Their mandate is to take all this information and produce a data-driven interpretation of what harm is, with categories and classifications. They don’t have nearly the manpower to go through all these cases. The judges want to point to specific evidentiary points to support their determinations and sentencing. More broadly, the way this is being conducted is a first globally, to have a restorative justice process for crimes on this scale, crimes against humanity for an entire country. They see it as a framework for other transitional justice courts trying to bring about peace. They want a robust analysis of their data for their case and for the future.

I’m coming in from the ML perspective. It’s an interesting embedding exercise, an encoder, and also, can an LLM do this well? I was thinking about it as a conditional semantic task. With two sentences, ordinary semantic textual similarity asks how similar they are. Conditional similarity gives you an additional condition, like the color of someone’s shorts. I have a proposal that makes it clearer. [Brief exchange unclear.]

<a id="a03"></a>
### A03 · The collaboration and the Colombian “false positives” cases · Clip A 04:49.192

[Source wording](source-transcript.md#a03)

**Participant** — [Question about Peter’s collaborators.]

**Peter** — I’m in engineering, in CS, but I’m doing it with SPS, their negotiation and conflict resolution [program].

**Participants** — [Clarification that the testimonies are from Colombia, the country.]

**Participant** — There are all these testimonies. It’s this massive dataset of transcripts. How do you find the types of harm in a large, unstructured dataset? What’s a more bottom-up way of thinking about the types of harm discussed? How do you cluster the things people are reporting in “harm space”? Can you do this in an unsupervised or weakly supervised way? It’s a very unique dataset. There’s some data they want to give you with annotations of types of harm, and you don’t have it yet?

**Peter** — We have definitions from the same type of case. We’re looking at crimes that the military committed against the civilian population. “False positives.” [A participant asks about the term.] They had quotas. They killed thousands of civilians and dressed them up as rebels. Homeless people, marginalized people, minorities, [wording about who would be missed is unclear]. The families have this terrible stigma afterwards because they were accused of having a rebel in their family, and they were totally innocent.

**Participant** — [Asks about the relationship between “false positives” and clustering.]

**Peter** — The Colombian civil war is the broad dataset, all these testimonies in different trials. We’re looking at the “false positives,” the cases where the military was intentionally killing civilians.

**Participants** — [Discuss the difference from the technical use of “false positive,” the targeting of Indigenous and poor people, and the inadequacy of that phrase for the killings.]

**Peter** — We’re trying to learn a good representation of harm from the data. We’re trying to find an unsupervised, semi-unsupervised way to pass the corpus through an encoder and have it discover a reasonable representation of harm itself in the embedding space. We’re trying to condition it on finding harm.

<a id="a04"></a>
### A04 · Using color as a control for conditional similarity · Clip A 08:34.192

[Source wording](source-transcript.md#a04)

**Participant** — And you’re not trying to cluster into different kinds of harm?

**Peter** — No, I am. That’s exactly what I am [trying to do]. Here’s the clustering that I produced. This is from the C-STS dataset, conditional semantic textual similarity. [The opening description of the encoder is unclear.] The colors are all over. The color represents that red, for example, was mentioned in the sentence. It’s very different data. It’s a control, a simple toy dataset, but it’s what people use in this learning task. One input pairs “shorts color” with a sentence about a man in red shorts entering water. Another pairs “color of clothing” with a sentence about a boy in a blue shirt jumping into water.

**Zach** — The confusing thing for me is that there are embedding approaches that condition on textual information. You can train an embedder to figure out similarity given information about the type of similarity you’re looking for. Here you care about one type of thing, the idea of harm. You care about one specific type of similarity and one specific type of clustering. It feels like you don’t really need a conditioning approach for this. You might be conditioning by fine-tuning on your data.

**Peter** — That’s basically what I’m doing. I was planning to take a typical encoder and fine-tune it on its ability to measure the rough similarity.

**Zach** — What this shows is that you don’t necessarily want an arbitrary off-the-shelf embedding model. You want to adapt it to your domain. One way of adapting would be prompting it. What kind of harm is being referenced here? The other way would be some sort of fine-tuning approach.

**Peter** — I wanted to illustrate that on this simple one. When I fine-tuned it on predicting a similarity score from one to five for sentences that reference color, it got this super clean clustering of the different colors themselves, which I thought was cool.

<a id="a05"></a>
### A05 · Supervision in the control and labels in the hearings · Clip A 11:15.192

[Source wording](source-transcript.md#a05)

**Participant** — So how do you [fine-tune] it?

**Peter** — I did L2 loss on the prediction of the similarity score between two sentences. Say one mentions red and the other has a guy with a green shirt. Those are different.

**Zach** — I’m curious where that supervision comes from.

**Peter** — Human annotations. They’re actually captions from the [dataset name unclear].

**Zach** — You take human data saying these things should be related and these things shouldn’t. And you have those labels now [for harm]?

**Peter** — It’s kind of a yes. We have some based on previous cases in different regions.

**Participant** — Specifically saying these two things are similar?

**Peter** — We have six types of harm. Emotional harm, physical harm, harm to property, harm to family, harm to spirit. And they have quotes from the cases saying this is this type of harm. [Peter says “six.” Five distinct examples are intelligible.]

<a id="a06"></a>
### A06 · A codebook baseline, an “other” category, and a small model · Clip A 12:19.192

[Source wording](source-transcript.md#a06)

**Zach** — If you have data and can train on it, that could work. If I were given this project and asked to figure out what kind of harm is in this dataset, I’d probably take the harm labels you have so far, with descriptions, and give them to a model. I’d include an “other” category. I’d ask it to go through the corpus and tag it. Then I’d look at everything that falls into “other.” What do those examples look like? I’d probably pass them through a language model and ask, “What categories would you create?”

Or, as an initial step, I’d run a summarization model over the transcripts. You get these much smaller texts, and you could do the same thing over those. Going from some labels to embeddings that capture the aspects you care about could really work. In general, one of the best things to do is rely on the ability of language models to generalize. Put it in context and see what it defines for you.

**Peter** — I know that’s going to win. That’s my hypothesis, too. I’m trying to build out an experimental design on a spectrum from unsupervised to basically strictly supervised. And from a lightweight, open-source encoder we can give them, to GPT [model name unclear].

**Zach** — A cheap thing to do would be to run a small language model over your dataset, extract labels and tags, and do something on top of that data. These systems are really good at reasoning over text. I get anxious when I go into an embedding space because these models are text-native. You’re trying to outperform systems that are very good at text-to-text reasoning. But it’s cool, you can try it. Will you be able to run this for the [midterm] report?

**Peter** — I think I’ll be able to. I have some data. I think I’ll be okay.

<a id="a07"></a>
### A07 · Embed the hearing text and compare summary prompts · Clip A 15:44.192

[Source wording](source-transcript.md#a07)

**Zach** — I’d hedge a little. Run the embedding approach, and also try running a small language model over these things and doing the embedding approach on top of that. How are you embedding this right now? Sorry, this is just colors. Have you embedded the transcripts yet?

**Peter** — I have not embedded the transcripts.

**Zach** — I would definitely do that. Embed the transcripts and see what the different off-the-shelf embedding models give you. Do you have the compute? How much data is it?

**Peter and participants** — [Several rough counts are exchanged, with conflicting units. Peter describes roughly 100 documents and says many run to around 100 pages.]

**Peter** — I could take the word “harm,” find about thirty similar words, and get the relevant sections quickly. [Clip A, 16:51.192–17:03.192. The method name was transcribed as “an MRI or something” and remains uncertain.]

**Zach** — I’d split them up. A caveat here is that I don’t know very much about the semi-supervised stuff, or what a lot of people are doing with it. I would get some of that data embedded and visualize the clusters from off-the-shelf models. You don’t even have to fine-tune. At the very least, get the text embedded, document the challenges and see how things are distributed.

I’d run a summarizer over the data. Try a harm summarizer as well. You can say, “Summarize this document.” You can also say, “Summarize the harms that are stated in this document.” Then cluster those. It would be interesting to compare those clusters to the ones you get without that preprocessing.

**Peter** — I’ve actually done a broad summarization over all the transcripts, in English.

**Participants** — [At Clip A, 18:17.192–18:27.192, the text renders the model name as “sole 6.1.” The model family is unclear. Personal account discussion omitted.]

**Zach** — If you have those summaries, I’d embed those immediately and see what it looks like. If you have the compute, ask the model to summarize the harms. Then do that same experiment and see if you get a different-looking result.

<a id="a08"></a>
### A08 · Exploration, expert labels, and the midterm · Clip A 19:05.192

[Source wording](source-transcript.md#a08)

**Zach** — Then you can incorporate human labels. There are two parts of the project. You have this amazing dataset. What can you learn from it? And then, how do you incorporate human labels into the learning task?

**Participants** — [Aside omitted.]

**Zach** — There’s a lot of literature on how you use limited human data to learn something you care about. Then there’s the more exploratory idea of what you can do with this dataset without much human labeling. If I were working on the project, I’d probably focus on exploration. Your proposal seems more focused on the semi-supervised approach. The challenge with your time and resources is finding a balance. You have some preliminary results for incorporating expert labels. Maybe do a little of both for the midterm if you can, but I would definitely see what you get without the labels. Then see if you can do a little better with the labels.

**Participants** — [Personal scheduling discussion omitted.]

**Peter** — I’ve pretty much charted out the summarization, having an LLM do it with relation to harm, and the encoder. I feel like I’ll have a cool product for the midterm report.

<a id="a09"></a>
### A09 · Restorative justice as a proposed ablation · Clip A 21:28.192

[Source wording](source-transcript.md#a09)

**Peter** — One final thing. The ethics of it are important. I found a paper where they fine-tune a model to use specific ethical reasoning frameworks. For example, citing Taoism as the reason something is right or wrong. It was called something like “moral …,” MET. I thought, without overcomplicating this, what if I took their methodology and ported it to my dataset as one ablation? [Clip A, 22:10.192–22:18.192. The ASR garbles the Qwen model size.] If I tell it, “This is restorative justice, that’s what we’re conditioning on,” and adapt how they construct the fine-tuning or ontology, how does that change the underlying representation? For example, when it summarizes, I’d tell Qwen, “I want you to use this restorative justice framework when you’re doing this.”

*Editorial reference.* The likely paper is *MET: Theory-Grounded and Culture-Aware Multilingual Moral Reasoning*. The authors evaluated MET-D with Qwen3-4B, Qwen3-8B and Gemma3-4B. Either Qwen size is consistent with the family mentioned here. [Paper](https://arxiv.org/abs/2607.11736)

**Zach** — It might be worth trying simply asking [model names unclear] what they think. But be careful. It’s easy to do experiments, and you only have limited time for class. You can keep working on this dataset outside class. At the very least, prompt the model with more information about how to think about this problem and see if the summaries change. One configuration is a summary of the document. Another says, “Focus on the harm.” A third says, “Focus on the harm and use this framework to think about harm.” My guess is that would give you better clusters without supervision. Then you can add supervision later.

**Peter** — I can see that. That would be very good to do.

<a id="a10"></a>
### A10 · A possible qualitative study and the immediate priority · Clip A 23:57.192

[Source wording](source-transcript.md#a10)

**Zach** — Separately, down the line, you could put a language model in the situation and ask how it reasons about a horrible thing that happened. That could be a qualitative study. People subject models to these really weird hypothetical situations. [Gives an example of a contrived moral dilemma.] Here you have a tricky situation where real harm happened, and systems are increasingly having to reason about policy. A different study, with much more effort and collaboration with your partners or NGOs, would be, how do models reason about this stuff compared with humans, lawyers, and others?

**Peter** — At the core, what I thought was cool was, if you make this as unsupervised as possible, what happens when the model comes up with very different definitions of harm than the ones the people at the JEP and UN have agreed on? There’s a framework, “these six kinds of harm.” It would be really cool to give it fewer [“training wheels,” probable reading] and let it learn. Maybe these categories are quite different from what people have come up with in the last ten or twenty years. That was an original motivation.

**Zach** — It’s so easy to want to do so many different things because there are so many cool things. [Personal anecdote omitted.] Focus for now on how you use these tools for discovery. To what extent does prompting a certain way, incorporating expert data, or incorporating moral frameworks improve the quality of the summary? Embed the data. See how different ways of summarizing before embedding change the distribution and the clusters. From there, I’d ask, how can I incorporate expert feedback? [Closing exchange partly unclear.]

**Participants** — Thank you so much. Thank you.

## Part II · Student research discussions

<a id="b01"></a>
### B01 · Predicting literal and figurative translation · Clip B 00:00.352

[Source wording](source-transcript.md#b01)

**Zach** — You can use the hidden states or the SAEs [sparse autoencoders] and think about a classifier. Can you predict what the model’s going to do before it does it? There’s evidence for this on other traits. I got interested in training a probe that predicts whether something is going to happen. I don’t think anyone’s looked at this specific case. You could sample ten or twenty times and tag whether the model’s answer is metaphorical.

**Student** — I could make a language model [judge], I guess?

**Zach** — You could probably make a judge for it. Spot-check it. It’s a class project. [Brief exchange about judges and publication.] Generate a bunch of outputs. Then ask whether you can predict the probability of a metaphorical response from the SAE [term unclear] or the hidden states directly. You can also see if it generalizes between languages, English or French, French and German, whatever the languages are.

**Student** — [Mentions languages including French and Korean. The full set and its direction are unclear.] Which is a better starting point? If I was just going to do SAEs, should I do hidden states?

**Zach** — I’d do hidden states too. SAEs might be more interpretable, but that information is also contained in the hidden state. I’d do both. It’d be cool to predict what the model’s going to do. What the model does is probabilistic, which would also be interesting to characterize.

<a id="b02"></a>
### B02 · A probabilistic target and a probe · Clip B 02:47.352

[Source wording](source-transcript.md#b02)

**Zach** — An interesting part is just the first part. You prompt the model. How consistent is the model’s distribution? You can also say, “When possible, use the figurative translation,” and do that for one or two models. [Brief interruption.] For the baseline first, given an input, can you predict the probability that the model will be metaphorical? Can you predict that from the input hidden states?

What I found worked well was ridge regression on the log probability. Over the summer I was trying to predict refusals using the hidden states, and that worked pretty well. [The description of how the idea originated is unclear.] Smooth the log probability of the behavior you care about and regress on that. From the hidden state, you predict the probability of the behavior. Does it generalize between languages? Does it work better with SAEs or without? For the first part of the class you can focus on classification before doing much steering.

**Student** — I think that makes sense.

<a id="b03"></a>
### B03 · Prompt interventions, steering, and novelty · Clip B 05:30.080

[Source wording](source-transcript.md#b03)

**Zach** — Another thing you can try is prompting, “Where possible, be literal,” or, “Where possible, be figurative.” Look at the effect that has on the distribution. You could construct steering vectors by prompting it to be metaphorical versus literal and computing the difference between the hidden states. That could be a way into steering or classification. Maybe use those states for your classifier. That’s more speculative. I think predicting the model’s behavior from the hidden states on this question is really interesting, and from there you could go into steering. Does that seem reasonable?

**Student** — Yes. [Asks about the novelty of the idea.]

**Zach** — I think so. I wasn’t familiar with the space. I asked a chatbot what existing paper was most similar, so take that with a grain of salt. With tools like SAEs and probes, I think there’s enough here to do work that diverges from existing work. There are different possibilities.

**Participants** — [A question about possible outcomes follows. The exchange appears to discuss reporting a negative result. Its exact wording is unclear.]

<a id="b04"></a>
### B04 · An interruption and midterm planning · Clip B 07:47.720

[Source wording](source-transcript.md#b04)

**Participant** — The FAA has grounded all flights nationwide.

**Participants** — [Participants discuss a breaking report about a communications outage. Unrelated speculation omitted.]

**Student** — For the midterm, what would be a good first thing to do? [Several words unclear.]

**Zach** — [Affiliation details omitted.] Use the resources you have for the class. You can move pretty fast.

**Participants** — [Side conversation about a separate submission omitted.]

<a id="b05"></a>
### B05 · Baseline rates and cross-language prediction · Clip B 10:07.320

[Source wording](source-transcript.md#b05)

**Zach** — Compute the basic statistics first. Given an input, what’s the distribution of figurative versus literal translations? How consistent is it for a model? Does it have a lot of probability mass on the literal version? Then, to what extent can you predict the probability of a figurative translation from the hidden state of the prompt, either from an SAE or from something built on the hidden state? Does that generalize between languages? That would be a good thing to run.

**Student** — Okay, perfect.

**Zach** — Then you can look at the correlation [with SAE features, exact wording unclear]. [They discuss time available.] From there you could try [an intervention on] the activation pattern as well. With baseline probabilities for these models, you can see how the probabilities shift.

<a id="b06"></a>
### B06 · Possible interventions and model choice · Clip B 11:51.112

[Source wording](source-transcript.md#b06)

**Zach** — Say you have a bunch of prompts with a bunch of continuations. Some are figurative and some literal. Maybe one in ten for a prompt is figurative by default. You could take those figurative samples and try to increase the probability of those sequences. [The name of the method is unclear.] What’s going on in the model when you do that? Can you find a region of the model handling it? Even asking the model to be figurative and seeing how that shifts things would be interesting. Get a baseline number and keep things similar [as you change the prompt]. If you have some good results and a clear direction, I think that would be enough.

**Student** — [Asks about the midterm and the available SAE/model combinations.] There’s a Gemma one. These are the ones that exist, which is why I picked them. [Another model name and some details are unclear.] The Gemma one is instruct. That’s what they had.

**Zach** — Those would be very different. [Discussion of instruction-tuned versus base models and how to prompt them.] I think I would get an instruction-tuned [model].

**Student** — Okay, so just the Gemma.

**Zach** — More results for one model can be better than a few results for lots of models. One model would be fine. Maybe two models would be nice, but …

**Participants** — [They check SAE availability for Llama, including a mention of Llama 3.1. Zach suggests using the hidden-state classifier where the SAE is unavailable. Exact model listings are unclear.]

<a id="b07"></a>
### B07 · Poetic constraints in reasoning · Clip B 15:08.864

[Source wording](source-transcript.md#b07)

*[In Clip B, the opening of the switch to poetic constraints is in the segment starting at 15:08.864. Its first explicit description of constraining the reasoning is at 16:30.768. The recording metadata gives no speaker identity at the transition.]*

**Student** — I’m a little stuck on constraining the reasoning chains. It’s not doing it super well. [Model and setup unclear.] Here are the prompts I have. Alliteration works fine. For anaphora, I chose to give it a phrase to use, because when I let it be free-form it didn’t follow it at all. If I give it a phrase, it does. For couplets, it’s not doing it. For [another device, possibly epistrophe], I also gave it a phrase.

**Zach** — That’s a finding. I’d try more models with exactly the same thing.

**Student** — I’ll try it on different models. Should I continue with the rest of the experiment if they’re not necessarily following instructions? The models are responding to the logic QA questions a lot worse than [another benchmark name unclear]. For a rhyme scheme, this is the reasoning chain it used, which doesn’t follow the rules at all. [A model suggestion is unclear.] Suppose I get mixed responses and alliteration works …

**Zach** — And does it lose performance?

**Student** — I haven’t done more than just two, so I don’t know if it improves performance. This is just testing whether the instructions themselves are followed.

**Zach** — Take the settings where you get the instructions to work, and then see [what happens to performance].

**Student** — The feedback on my proposal was to make it more robust, with a lot more poetic devices. But I feel this will axe a bunch of them. The main offenders are the line spacing [apparently in couplets] and syllable counts. It just doesn’t do it.

<a id="b08"></a>
### B08 · Adherence, accuracy, and a rewrite control · Clip B 19:42.656

[Source wording](source-transcript.md#b08)

**Zach** — It’s a negative result. It’s hard to control the models. You can report that. [A suggestion about another model and the cost of scaling up is unclear.] With a model that gives you its reasoning, you can look at the effect of the task on performance.

**Student** — Is it worth going through with the methodology if I might get a bunch of negative results?

**Zach** — You can look at the cases that actually follow the restrictions, and you can report the cases where this doesn’t work. Can you ask the model to generate the answer normally and then regenerate it using the constraint? That lets you see whether it can follow the constraint, period.

**Student** — I have a bunch of devices. If I run the model, make it reason normally, and then make it rewrite with each device, isn’t that a lot of test cases? For every question I’d be running it through eight devices and two datasets.

**Zach** — Pick a subset. Test whether the model can adhere to the constraint during reasoning, then have it rewrite its reasoning in that style and compare. The model struggling under these instructions is already a result. I’d do this for more than one model so you can include that result in your [midterm] report. Then look at the actual accuracy.

<a id="b09"></a>
### B09 · What belongs in the midterm report · Clip B 23:01.360

[Source wording](source-transcript.md#b09)

**Student** — What should I differentiate between what I report for my midterm report and everything after that?

**Zach** — Report what you’ve done.

**Student** — I have three more days.

**Participants** — [Personal administrative detail omitted.]

**Zach** — In your shoes I’d run this over multiple models and see what percentage of the time each follows the constraint. Then, in a setting where models follow the constraint pretty regularly, what’s the actual penalty to accuracy? How does it compare to no chain of thought? That’s the baseline. How does it compare to regular chain of thought? Document that.

**Student** — That was my question.

**Zach** — I would get multiple …

**Student** — Multiple models.

**Participants** — [Personal closing conversation omitted.]

