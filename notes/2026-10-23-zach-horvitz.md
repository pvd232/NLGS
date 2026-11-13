# October 23, 2026 · Office hours with Zach Horvitz

**Participants** · Peter Driscoll and Zach Horvitz  
**Project** · Learning a representation of harm in JEP testimony

## Summary

The strongest result the two could imagine was a group of passages that revealed an interpretable kind of harm missing from the codebook. Expert review would determine whether the proposed category deserved a code. While waiting for annotations, Zach suggested clustering testimony directly and then repeating the exercise with summaries conditioned on harm.

| Research question | Comparison raised in the meeting |
| --- | --- |
| Do the clusters capture distinctions experts recognize? | Compare clusters against expert codes and examine differences among annotators. |
| Does summarization help? | Cluster original passages and harm-focused summaries. Standardized descriptions might make recurring consequences easier to recognize. |
| Can a model suggest a missing code? | Inspect passages grouped under “other.” Compare codes proposed from a transcript in context with codes proposed by a model that can retrieve similar examples. |
| What justifies additional modeling? | Identify a recurring failure, make a small change and check whether it fixes that failure. |

**Follow-up proposed in the discussion.** Peter would check how the earlier justice codebook was validated. Zach offered to read the proposal. The modeling ideas were suggestions. The conversation records no results from running them and gives no deadline.

**Call to action for the experiment.** Select one set of passages, retain links from every summary back to its original text, and take one candidate cluster to the experts with examples showing why it might merit a code. This is an editorial recommendation grounded in §§1–3.

## Edited transcript

Peter supplied the meeting date retrospectively. Local recording metadata confirms October 23 at 3:44 p.m. New York time and a clip length of 13m22s. This reading edition follows the source text uploaded November 4, 2026 (New York time), verified byte for byte against the saved machine transcript. It begins mid-discussion and cuts off mid-sentence. The source has no timestamps or speaker labels. Attribution follows the exchange where the role is clear. Punctuation and obvious recognition errors have been edited, repeated fragments condensed and uncertain language marked. The public edition marks one omitted personal aside.

### 1. Getting started before the labeled data arrive

**Peter** · Let me just get the first three. You said one would be to embed the data and then cluster it?

**Zach** · First, I guess you're probably waiting on data, but I'd try to get some labeled data with the codes and see how well the models can match them [last word unclear]. You have multiple experts annotating the codes as well, so you have some sense of how variable that is.

**Peter** · Yeah, of course.

**Zach** · While you wait for that, an interesting question would be, what can you do in an unsupervised way? I'd explore a few different embedding approaches and see what clusters you find. There are these text-conditioned [unclear]. You cluster and think about what clusters you're seeing. Do they capture the types of things the codes correspond to? Then I'd run a small language model over the entire dataset, generate harm summaries and try clustering those.

**Discussion, speaker change uncertain** · A conditional summarization? What would I condition on explicitly? The harm. Say, “Summarize the harm” that's here. You summarize and then you cluster. That might be a quick intervention.

**Peter** · That makes sense. I thought about that when I read the paper on summarizing with a perspective in mind. That's a conditional transformation of the data, somewhat similar to my task.

**Zach** · And you have expert ratings, right?

**Peter** · Yes.

**Zach** · With expert ratings, could you train an embedding model to do better? There might be something there in supervised learning, but I think the best thing you can do is go simple first. What story can we tell? You have a novel dataset and a novel setting. That gives you flexibility over method novelty. Try things and see what really works.

### 2. Looking for a new code

**Discussion, speaker change uncertain** · To what extent can [system name unclear] find reasonable codes an expert would agree with? Take samples tagged as “other” and explore that tag. Have it go through those and ask, “Are we missing something here?” Have it try to formulate ideas and see what the experts think of them. Can it infer new categories within “other”? Explore that on the data and on the harm summaries. “Describe the harm that's discussed in this document.” A conditional summary like that would probably make the clustering easier.

**Peter** · I almost think of summarization as compression, like dimension reduction. You're getting rid of some of the noise and making it more useful.

**Discussion, speaker change uncertain** · It wouldn't just be shorter. It would be standardized. [Unclear reference.] See what later work has been done. People are thinking about doing data analysis with these models. The coolest thing would be finding something. Your north star for this project is finding a code.

**Peter** · That's what I thought from the beginning. We think this is harm, and it turns out there's a new category that we learn organically. You have to make it interpretable. You have to get it back out of the embedding space and be able to say, “This makes sense.” In the single-cell world you have a lot of data and you're trying to discover what cell types exist. A lot of fruitful work came out of clustering and investigating those clusters. That's my frame of reference. If we could find a new code and the experts agree, that would be really cool.

### 3. Giving a model access to the corpus

**Discussion, speaker change uncertain** · There's work searching for the kinds of inputs that break models. They use something like a topic model and have it summarize the types of problems it's seeing. How do they find categories? Their category construction might be relevant. [Unclear discussion of searches and reinforcement learning.] They prompt a language model to synthesize the common properties of the high-scoring things. Actually, this part doesn't sound very relevant. The question is, how do you give a model a more global notion of the dataset when you have too many input tokens?

You could give it the descriptions or put transcripts into the model's context and ask, “What are the categories of harm that you see here?”

**Peter** · That's what I saw as the baseline. If you ask an LM to discover the codebook, what does it give us? They did a pilot with the same idea, but for justice. What notion of justice do you witness in this case? How is justice represented in this corpus? How did the victims see it, how did the perpetrators see it? What are the different types of justice? They passed the corpus through an LM. I'll have to double-check with them how the codebook was validated. [Reference to a human check unclear.] That was the previous pilot on justice. They haven't done it for this one yet.

**Zach** · What we talked about is still valid. Take descriptions of the data, cluster them, and see what clusters exist. Beyond putting everything into context, give [system name transcribed as “Astra”] access to the embedding model and the dataset. Let it propose queries, try things and search. Would it find different queries or codes from what was originally found? It could run a Python script, submit a query to the dataset, find the most relevant samples or search for samples most related to one another. An intervention could be to change how you expose the information to the model. Does giving it access to retrieval help it find better codes?

### 4. What would make a paper?

**Zach** · There are a lot of possibilities. I'll go through your proposal. [Unclear.]

**Peter** · [Personal reflection omitted in the public edition.] I will come to office hours. I have a tendency to brainstorm on my own.

**Zach** · Think about the minimum amount of ML and modeling you need to unlock rich insights about this dataset. What does it tell you about the current failures of models? I'm curious about the failure modes. A cool paper would document them. The best papers give you a dataset, find failure modes on it, and then do some minimal intervention that fixes one.

**Peter** · I saw that on conditional semantic textual similarity. A paper [author unclear] examined the dataset and found, let's say, ten percent of the questions were flawed because the semantic condition was binary. Say you're conditioning on the number of pets. That's true or false. A four or a three is invalid. It's either a five or a one on the [scale name unclear]. That was an intervention on the dataset. They said, “This is obviously a flaw in it.” It's a bit nebulous because it's … [source ends].
