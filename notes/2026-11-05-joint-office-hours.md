# November 5, 2026 · Joint office hours on annotating harm

**Participants** · Peter Driscoll, Kathleen McKeown, Peter Dixon and Valentina Velasquez  
**Project** · Learning a representation of harm in JEP testimony

## Summary

The group worked through what an expert-labeled example would contain. A useful example could be a short phrase or two sentences that identify a harm, paired with a label. About fifty such spans was suggested as a starting target for a class project. Existing material from a related case could provide examples. The discussion also identified two distinctions worth preserving when the source permits it.

| Distinction | Why the group cared |
| --- | --- |
| A crime and the harms arising from it | One legally defined crime can produce several harms. Keeping separate labels allows the researcher to pool them later or evaluate whether the model distinguishes them. |
| Shared event and differing perspectives | A victim and a perpetrator may describe the same event differently. Linked passages make it possible to examine semantic similarity and divergence on the same case. |

**Next steps discussed.** Look for passages that already carry labels in court material. Identify the span and harm type first. Consider adding speaker role, an event link, and separate crime and harm labels where available. A generic LLM that proposes and applies a codebook was discussed as a baseline against expert annotations. No one reported completing these steps or committed to a deadline.

**Call to action for the team.** Take one labeled court example, mark the exact text covered by its label, and decide whether the recorded category is a crime, a harm or both. Check the typology against the underlying court document before adopting its list. These are editorial next steps drawn from §§1, 3 and 4.

## Edited transcript

Peter supplied the date and participant list. Local recording metadata confirms November 5 at 12:04 p.m. New York time and a clip length of 15m28s. This reading edition follows the original text uploaded November 9, verified byte for byte against the saved machine transcript. It begins mid-discussion. The text supplies no per-turn times or speaker labels. The dialogue uses functional labels where two or more participants could have made a turn. Short repetitions and obvious recognition errors have been edited. Uncertain terms are marked.

### 1. What is a labeled example?

**Discussion** · If there were a bit more [data], he could use it either for fine-tuning or for providing examples in context, what's called in-context learning.

**Participant, addressing Kathleen** · It would be great if you could describe a bit more what you mean when you say annotated text about harm. Clearly labeled, maybe by us or someone else? Text that shows that what is described here is harm X and what is described there is harm Y? Or can it be more [unclear]?

**Kathleen** · Ideally you would underline certain passages. They could be short phrases, a full sentence, even two sentences. Identify those pieces of text, then label them with the kind of harm. What you use for harm is probably a topic of discussion. The ones Peter showed me last night had murder as one type. You could categorize them as murder, threats, assault or whatever you have. You could also label who was the object of the harm and who caused it. That's more work, and you probably don't need to do that for this project.

**Participant** · We can look to see if that already exists. We have our corpus, these long recorded testimonies. Does the text need to come from that corpus, or can we draw on texts where the court has done this work for a different but related case?

**Kathleen** · You can do either. He could use them to provide examples to the model, and he could test how well the model identifies them. For a class you don't need as many as you probably would to publish. I would aim for about fifty examples of labeled harm, fifty sequences of text where you label one harm or another. If you already have them for other court cases, he can use those.

### 2. Two perspectives on the same event

**Participant** · Could you describe the way [the court] has defined harm according to the *auto* [court order] that we discussed? I'm curious if there is a second dimension that's important to consider.

**Participant describing the corpus** · There is a second dimension. We describe harm for two actors, victims and perpetrators. Their approaches differ depending on whose narrative of harm you're looking at.

**Discussion** · Is it the same narrative, and can you identify who the perpetrator is and who the victim is?

**Participant describing the corpus** · The transcripts are labeled, so we know when the victim is speaking, when a perpetrator is speaking and when a judge is speaking.

**Discussion** · Are you assessing narratives for both actors? Are you concerned about when they describe the harm differently? Are there examples where the perpetrator describes what happened and the victim of that perpetrator describes what happened? Or are they totally separate?

**Participant describing the corpus** · There will be examples like that. In each hearing the perpetrators and the indirect victims get together. Most of the direct victims died. They are talking about the same cases.

**Kathleen, attribution inferred** · Ideally you'd want to know that this stretch of text was described by the perpetrator, and who the victim was. Then you'd want the corresponding section described by the victim and the identity of the perpetrator so you could link them.

**Peter Driscoll, attribution inferred** · Could we use this, or at least [unclear], to our advantage as a regularizer? If we're conditioning specifically on what the harm was and its nature, the underlying harm that occurred is the same.

**Discussion** · Yes and no. It could help you learn semantic similarity between stretches of text about the same harm. It could also be that victims and perpetrators describe it differently. They have different perspectives.

They will. You could try it both ways. You could use this to help learn the semantics of a specific kind of harm, and later look at divergence in how the two accounts describe it. The current project is concerned with identifying similarities. The divergence would be an interesting follow-up.

### 3. Crimes and harms

**Participant** · What about the difference between the words “crime” and “harm”? These court cases have a clearly delineated set of crimes that they're investigating. Each crime can have different harms associated with it. Do we need to do anything in the model to make that distinction? Those words can be conflated, and it's important to keep them apart.

**Kathleen, attribution inferred** · If you have that information, it would be helpful to annotate it separately. One is a crime and one is a harm. Models could later look at distinguishing them. For this project, you could count them together, giving you more data. But if you know the difference during labeling, it will be easier to keep that information now than to go back through everything later to label crimes.

**Participant** · We're focusing on harm because the court we're working with is interested in these narratives of harm beyond [unfinished].

**Kathleen, attribution inferred** · It's partly your decision. If you're never going to look at crimes, you could label both as harms. But if you distinguish them, Peter can still count them together for this model and you'll have the information later if you want it.

### 4. The court's typology and the model comparison

**Participant describing the court framework** · The court came up with a typology we could use as initial labels, based on judicial documents and studies by specialized units in the court. They talk about five dimensions. They describe moral harm. They describe harm to physical, mental and emotional integrity, harm to the body and mind. Harm to the life plan. Harm to property and the deepening of economic vulnerability. Social, cultural and territorial harm. And harm to civic trust and [wording unclear] under the rule of law.

*Editorial note.* The speaker says “five” and names the groupings above. A later speaker says “five or six.” The transcript alone cannot settle how the judicial documents group them.

**Kathleen, attribution inferred** · Ideally you would label that. In the example Peter showed me last night it was at the top. In some ways the example was already labeled in the document.

**Peter Driscoll, attribution inferred** · There are guidelines and codebooks that have been extracted. The annotations would be really helpful. One of our baselines would be an off-the-shelf LLM going through the text, coming up with a codebook and applying it. We'd compare that to the expert annotations too.

**Discussion** · If you label crime, harm, and the five or six perspectives, for modeling you'd have a choice. You'd get more data if you counted everything together as harm. If you had enough data you could test whether the model distinguishes different kinds of harm.

**Peter Driscoll, attribution inferred** · Some of the work we've done in class concerns steering models and using supervised fine-tuning to influence their reasoning. There was a paper [title unclear in the source] on theory-grounded, culturally aware multilingual moral reasoning. [Repetition in source.]

**Kathleen** · I have a bunch of people waiting, so I'm going to have to stop. I think this gives you enough to get started. [Closing invitation partly unclear.]

**Participants** · Thank you again, Kathy. We really appreciate it.

**Kathleen** · I'm interested in it. Good luck. I'll be interested to see how it comes back.

**Participants** · Thank you so much. Thank you. Bye.
