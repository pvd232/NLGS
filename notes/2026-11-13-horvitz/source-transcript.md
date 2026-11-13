# Source transcript · Office hours with Zach Horvitz

**November 13, 2026** · [Condensed reading edition](transcript.md) · [Summary and action items](summary.md)

**Recording times (New York)** · Clip A began at 3:55:17 p.m. and ran 27m 16s. Clip B began at 4:34:01 p.m. and ran 25m 59s. Both were recorded November 13, 2026. Times beside section titles give the start of the Superwhisper segment containing its first words. Offsets are relative to the corresponding clip. Some segments span pauses or more than one speaker. Each attachment matches the corresponding saved Superwhisper text by SHA-256. Both recordings have timestamped speech-recognition segments and no speaker labels.

The following passages reproduce the wording and punctuation of the two supplied text files, in order. Apparent recognition errors, repetitions, false starts, and incomplete sentences remain. Bracketed redaction notices replace personal or identifying asides. Headings and paragraph breaks are editorial. The original files have no speaker labels or timestamps, so paragraph breaks do not establish a change of speaker. Section A covers Peter’s harm project. Section B covers the student discussions on translation and poetic constraints.

<a id="a01"></a>
## A01 · A reading suggestion and the project setting · Clip A 00:00.192

last week on the paper that Jessica Dye did on the... Hello? I have another question. Okay. Jessica Dye is like a paper on the three years of chat chat TV, whatever, retrospective on Reddit. She is kind of relevant about learning SAE and you get these kind of like topics and then you can maybe like use that to like, you know, surface interesting things over time.

I was like, yeah, that's something relevant for Peter's. Yeah, yeah, yeah. I honestly didn't make the connection, but thank you. I'll look at it. Definitely. I'll go look at it. No, no, I'm just... I just kind of wanted to just like run through just kind of where I'm at, basically. It's similar. It's the same idea. We have these like testimonies from these trials and they're...

Very cool domain. Yeah. And okay. So one thing that I didn't highlight, which is like really important, is that this is operating under this idea of restorative justice. And so it's like a different way of viewing justice. So it's kind of like a different ethical framework in ways. It's a different way for seeking like, you know, right. What is right and what is good outcome in these situations. And so it's not focused on like punitive corrections, right?

_[Personal side conversation omitted.]_

<a id="a02"></a>
## A02 · What Peter means by a representation of harm · Clip A 01:59.192

It's just like a distinct moral framework, which I hadn't like properly appreciated, basically. And so that's why the setting of the trials was different. You have like all the perpetrators with all the victims. And they're just kind of talking it out in this dialogue, right? And it's being transcribed. Then the AI. Yeah, yeah, yes. And so I was thinking like the ethical questions here are like interesting.

And like kind of the moral aspect of the semantics of like what is that about? And so I was reading into that like kind of like looking at like how LLMs understand concepts like what's right, what's wrong, different moral frameworks. And there's like... Yeah, I mean it is and it isn't because I wanted to learn a good embedding of harm, like a good representation from the data.

And I wanted to... that's kind of like their mandate is to take all this information and to produce like a data-driven interpretation of what harm is with categories and classifications. And ultimately, their like their interest in it is they don't have nearly the manpower to go through all these cases. The judges want to be able to like point to specific evidentiary points to support their determinations and their sentencing.

And more broadly, they kind of... the way this is being conducted is a first globally to have like a restorative justice process for like crimes of the scale, crimes against humanity for an entire country. And they see it as a framework for other transitional justice courts that are trying to like bring about peace after something terrible, right?

And so they want to put this forth like to be like a framework, like the UN's use and other people. And so they want to like robust kind of like analysis of their data for their case and future. And so we're coming in and I'm coming in from the ML perspective of, oh, this is kind of like an interesting embedding exercise encoder and also just LLM.

Can an LLM do this well? And so, yeah, learning that representation of harm, I was thinking, okay, like this is like a conditional semantic task where you have like, you know, two sentences, normal semantic textual similarities, just how similar they based on the context. Conditional would say, okay, given an additional semantic condition of like typically like, I don't know, color of shorts or like colors, color of shorts would be like a condition that like canonically this stuff is evaluated on. And I can actually show you, I have like a proposal that makes it more clear. Just like am I right out of what I mean by that? I guess you know my people are shining on us. Oh, absolutely not.

<a id="a03"></a>
## A03 · The collaboration and the Colombian “false positives” cases · Clip A 04:49.192

So I guess the high level, by the way, Peter, right? Yeah, is that you have a pretty cool, I guess you're actually with which would score you with your with like not with the like you're like doing like you're like a Oh, yeah, I'm doing I mean, I'm an engineering and I'm CS, but I'm doing it with SPS.

They're negotiation and conflict resolution like to. Okay, so you're working with this collaboration with these guys. And then they they are like they have this like, yes, it's from Columbia. Yeah, the country. Yeah, yeah, country. And they have all these like testimonies, like it's conversations between like, I guess, gang members and defect people who are like victims of these gang members.

And it's this massive data set of transcripts. And I guess they're interesting in like applying AI capacity to try to understand aspects of this. And so there's like an interesting question of like, oh, like you have a large unstructured data set. How do you find like, what are these like, what are the types? How do you have like, what's like a more like bottom up way of thinking about like the types of harm that are discussed in this data set?

Like, how do you like, how do you like kind of cluster in like harm space, like these different types of things people are reporting? And so this question like, okay, well, how do you use AI and do this and like some sort of like how like unsupervised or like, like a weekly supervised sort of way? And I think, yeah, I was gonna say the high level is a really cool data set that you have access to.

It's like very unique. You just released this, right? And there's like some data they want to give you with annotations of types of harm. And then you don't have it yet, though. Yes, we have definite we have definitions from other from the same type of case. So we're looking at crimes that the military committed against the civilian population.

False positives. They have this policy up. False positive positives. And so far as like that they killed someone who does that? Yeah, they had quotas. Think about how the police have quotas. I was actually just picture with them. And they just killed thousands of civilians and just dressed them up as rebels and just like homeless people, marginalized people, minorities, Native Americans, people that would be missed.

That specific type of. False positive positives. Wow. Yeah, it's insane. Oh my God. Yeah, it's pretty. And then the stigma, the families have this terrible stigma after because they were accused of like having a rebel in their family and like totally innocent. You know, like everyone just arbitrarily, you know, the general general's just kind of wanted to like lose themselves.

All this data. Like a relationship between the false positives and like clustering. So this is the Colombian Civil War. It's kind of like the broad data set. All these different testimonies in these different trials that are being conducted. We're looking at the false positives, which is the cases where the military was intentionally killing civilians. And we are trying to learn is a very different setting for the idea of false positive.

Like I'm like, yeah, it's not a false positive. It's just like it's like the military. It's like genocide. Yeah, I mean, it's like they're just targeting like basically indigenous and poor people. Yeah, it's really not. And anyways, we're trying to learn a good representation of harm from the data. So we're trying to find like an unsupervised semi unsupervised way, pass all this corpus through like an encoder and have it discover a reasonable representation in like the really just the embedding space of the encoder of harm itself, which is kind of like we're trying to condition it on finding harm.

<a id="a04"></a>
## A04 · Using color as a control for conditional similarity · Clip A 08:34.192

And you're not trying to cluster into different kinds of harm. No, I am. That's exactly what I am. What's the. Yes, yes, I have like an illustration here, which kind of helps. It helped me, honestly. So here's the clustering that I produced. Right. And so this is from the CSTS dataset, conditional semantic textual similarity. And what you're seeing here are fine tune, just regular, twin embedding encoder embedding model.

Right. And the colors are all over. And what the color represents is that red was mentioned in the sentence. Right. This color was mentioned in the sense of very different data. Yeah. Yeah. Very different. It's a control. It's like a very simple like toy dataset. But it is like what people use in this like learning task. And so kind of what this represents is so, for example, one input one input pairs shorts color.

That would be like the condition with a sentence about a man in red shorts entering water. Another pair is color of clothing with a sentence about a boy and a blue shirt jumping into water. I mean, I guess what's kind of. Yeah. So I guess the confusing thing for me, though, about that is so like I know that there is like a bunch of embedding approaches that condition on textual information.

I think that's like a thing that you can do that you can train and better like figures out embedding similarity given like some other information about the type of similarity you're looking for. But I guess what's interesting here is like you have a dataset that's like one you have care about modeling one type of thing, which is like you care about kind of capturing this idea of like harm.

And so it's like you don't actually have a embedding model that you want to use for a bunch of different tasks. It seems like you have an embedding model. You care about one specific type of similarity and one specific type of clustering. So it feels like you don't really need a conditioning approach for this. You like are conditioning by like maybe fine tuning on your data in some sort of way.

Yeah. Yeah. Yeah. That's basically what I'm doing. I'm just taking a typical encoder and was planning to fine tune it on its ability to. Yeah, I guess. Measure the rough similarity. I guess a nice point that's made by this is that like you don't want to just necessarily just use an off the shelf like arbitrary embedding model.

It's like this idea here that you want to somehow like adapt it to your domain. Yeah. So one way of doing adaptation would be prompting it. Like kind of harm is being referenced here. Absolutely. And the other way of doing it like some sort of like fine tuning approach. Yeah. Yeah. Yeah. That's how I'm planning on doing it. I just wanted to illustrate like in this really simple one that when I just fine tuned it on predicting the score one to five similarity of different senses that in some way reference color. It just got this super clean clustering of like the different colors themselves, which I thought was cool.

<a id="a05"></a>
## A05 · Supervision in the control and labels in the hearings · Clip A 11:15.192

So what how do you find it? So I just had it. I just did like L2 loss on the prediction of the similarity score between two sentences, which were let's say red and green. One sentence says a red kid. The other sentence has like a guy with a green shirt. And you're like, oh, those are different. And then where do you.

How do you. So I guess what the I'm curious where that supervision comes from. Human annotations on like they're actually captions from the M. This data set. OK. That's what they are. The idea is you take some human data of like like these are like these things should be related. And you think shouldn't. Yes. Shouldn't show. Rough.

Yeah. I see. So you and you have you having those labels now. It's kind of a yes. I mean, ultimately, we we have some based on previous cases in different regions. And it's specifically to saying like these two things are similar. Yeah. Like they're like we have six types of harm. Right. Harm. Emotional harm. Physical harm. Harm to property. Harm to family. Harm to spirit. And then they have like quotes from the cases of like that. It's this is this type of harm.

<a id="a06"></a>
## A06 · A codebook baseline, an “other” category, and a small model · Clip A 12:19.192

It makes sense. I mean, if you have the data and you can train on the model and the data in some way, it seems like that could work. I would say like my like with. I think the way that I would probably I was just given this project like out of the blue. I know it's like tasked with like saying, oh, like kind of like figured out what kind of harm is in this data set.

I would probably like take what I would probably do is I would probably take the like the harm labels that they've given you so far with some descriptions with the harm tales. And I would probably like just like give those to a model. And and then I would also have like an other category. And I would say like, hey, can you just go through this entire corpus and just tag it.

And I would just like look at all the things that fall into the other category. And then I would like the one they gave us in the other. Yeah. And then like do some analysis and like what those look like and then see if I could like I would probably pass those through a language model and be like, what like what categories would you create?

That's probably like that's like the or like maybe as an initial step to make things easier for me, I would probably run a summarization model over every all the transcripts. And then you get these much smaller texts, lower dimensional. And then I would do the same thing over that or maybe something like this over that. But I think that like the I think the idea of doing something like this, where you go from some labels to like some like really good embeddings that capture like the like the aspects of that like embedding space that you kind of care about, I think that like that could really work.

I will say like in general, like one of the best things to do is just like rely on the ability of language models to generalize. And so I'm kind of like, oh, we should dump it into the context. Yeah, I don't know where your data set and see what it defines for you. Yeah. I mean, I know that's gonna win.

That's my hypothesis, too. Okay, it's gonna be the winner. I just am trying to, I guess build out a good experimental design that tries kind of on a spectrum from unsupervised to like basically strictly supervised. And then from encoder, right, really lightweight, can pass it all through easily open source can give them this tool to like GPT Astra, you know, I guess my sense is like a really cheap thing to do would be like to run like an LM just like over like a small language model, SLM, you got an SLM over your data set and just like get extract out some like labels and tags, and then do something on top of that data.

Like I think that like the it's interesting, we're at a point in time where we have these systems that are really good about reasoning over text data. And so I feel like it's sometimes a bit like I feel a bit anxious whenever I'm going into a betting space where I'm like, oh my god, these models are like, they're like text native, they know all about the world of text.

And when you go into an event space, you're trying to find your own things. It's like you have to kind of like the goals. I mean, you have this, trying to outperform these systems that like are really good at text to text reasoning. I see. I will say like it's cool, you can try it. I think that like, I mean, you have data for the final product with the mission report. Are you going to be able to run this for the mission report? I think I'll be able to. Yeah, like it's I mean, I have some data. Yeah, yeah, I think I'll be okay.

<a id="a07"></a>
## A07 · Embed the hearing text and compare summary prompts · Clip A 15:44.192

So I feel like wait, if I were in your shoes, I would use out hedge a little bit. And I would like run the embedding approach. And then I also try running a like a small language model over these things. And also doing the embedding approach on top of that. And do both of those. I mean, how are you how are you embedding this right now?

Sorry, this is just colors. Have you embedded the transcripts yet? I have not embedded the transcripts. Okay, so I would definitely do that. Yeah. And I would just like, I would embed the transcripts, and then see what these different embedding that you picked off the shelf embedding models give you. And then I would try the following, which is I would generate you have and you have compute to do this.

I think it's this will be pretty, I think this will be pretty how much data is it? It's 1000. Yeah, it's like a lot. It's like, I don't it's not that much. I think it's like easy. So a lot of these documents, they're like 100 pages. Oh, okay. We only have like 100 of them. So it's not that bad.

And you always like, like 1000 pages, and different documents. If I really wanted to, I could just take like the word harm, find like 30 similar words, and then just get the relevant sections right really quickly with like an MRI or something. Well, I would what I would do is I would like try with me split them up.

And I would like run also caveat like this is like, I don't know very much about like, like the semi supervised stuff or like a lot of people are doing with this sort of stuff. But I would say that like, I would like yes, like just try and get some of that data embedded and like visualize what you find in terms of clusters from like off the shelf, like you don't even basically have to fine tune.

I would try to fine tune in a better for for excuse me, you know, many days, but like I would just at the very least get all that text embedded in some sort of way and like document challenge with that and look at what how things are like distributed. And I would also just try how are you I would run a summarizer over like the data just to also try running a harm summarizer over it.

And I would be like, prompt you can just you can say summarize this document. You can also say like you prompt them on be like, hey, summarize the harms that are stated in this document and run that over and then do clustering on that. And I would like that would be a really nice baseline. Right. And I would also be kind of interesting to see what that cluster looks like compared to the cluster you get when you don't do that kind of pre processing. That'd be my sense. Yeah, actually, I actually have I've done that just a broad summarization over all the transfer. Yeah, so I do have that. Yeah, in English.

_[Account and usage discussion omitted.]_

I would consider if you have those summaries, I would just embed those immediately and see what it looks like. And I would also try one if you have the compute for it, I would actually ask the model to summarize the couple of document like summarize the harms. Yeah. And then do that same experiment and see if you get like a different kind of like looking thing.

<a id="a08"></a>
## A08 · Exploration, expert labels, and the midterm · Clip A 19:05.192

And then you can also do some cool stuff like incorporating human labels and everything. But like, there's like, there's two parts of this project, which is you have this amazing data set, like what can you learn from it? And then there's this interesting question of how do you incorporate like human labels into a into this learning task?

_[Recording aside omitted.]_

But my sense is like these two problems here. And I think it's what's there's a lot of literature on I think, like semi supervised learning and stuff. When you have some like early, I was confused, it would be supervised. But like, you have like, there's there's some rich body of work on like, you have limited human data, you like then use it in some way to like make, make your like, to learn something you care about.

And then this idea of whoa, I have an amazing data set, I want to do some cool stuff with it. That doesn't require like that much human labeling. And it's more like it's more exploratory. And frankly, if I were working on this project, I would probably focus on this thing. But your proposal right now, I think is more focused on this thing, which is a sort of semi supervised sort of a sort of approach.

I mean, a challenge for you given the amount of time you have, and resources you have is finding the balance between these two things. I mean, we have some preliminary results for this kind of thing, like for this idea of like, how do you incorporate expert labels. So I would maybe do a little bit of both for your for your midterm project, if you can, but I would definitely like, see what you get without the labels. And then maybe see if you can do a little better with the labels. I think it's my kind of sense. Okay. I don't know.

_[Personal scheduling discussion omitted.]_

I feel like when I sit down, and I like, I had the experiments I want to do like reasonably, like everything we've discussed the summarization, the having an LLM do it with relation to harm, the encoder, I've like pretty much chartered out. So I feel like I'll have like, a cool product for the midterm report.

<a id="a09"></a>
## A09 · Restorative justice as a proposed ablation · Clip A 21:28.192

Okay, I have one final thing. So the ethics of it are like important. And there's like kind of literature on this. And I found this cool paper where they basically fine tune a model to use like specific reasoning frameworks, ethical, like like using like, Taoism, right, like citing Taoism is like why you said this is right or wrong and how right.

And it was called like moral and whatever, MET. And I was like, Oh, this is really cool. So my thought was without overcomplicating this, if I could just take like their exact methodology, because they train Quinn 3.827 B, same thing as me, I take their methodology, just port it to my data set, maybe as one ablation and say, Okay, if I tell this thing, this is restorative justice, that's what we're conditioning on and kind of like adapt that framework to the way that they construct their like fine tuning or like ontology, and see how it changes the underlying, like representation, for example, when it summarizes

it, right, I'd have Quinn, and I tell Quinn, Hey, I want you to use this restorative justice framework when you're doing this. Yeah, see how it changes how it like, exactly. Yeah, I thought that'd be one cool interpretation. In general, would be like, ask these cases and just straight up like asking like quad or asking chat, like, what do you think?

Like interesting question is like, there's this idea of how do you like surface types of harm and everything. And I think that like, it might be worth trying that, you'd be careful because it's so easy to do experiments. And it's like, there's like so many things you can do, and you only have limited time for the class.

I mean, you have this data set, you have these resources, you can really just keep working on this outside the class. In the class, you have limited time, given like schedules and work, but like, you have to be careful. But I do think it'd be kind of interesting to explore, at the very least, like, yeah, people are just prompting soul with more information about how to think about this problem and see if the summaries change.

So there's like summaries of documents is one, one kind of configuration. There's like summaries of documents, where you say, hey, focus on the harm. And maybe a third configuration is focus on the harm and use this framework to think about harm. And I would guess that actually probably be better than the other three in terms of what you actually get in terms of clusters, with like no supervision. And then you can add a supervision later, make people look better. But I feel like, perfect. Yeah, I can see that. That would be very good to do.

<a id="a10"></a>
## A10 · A possible qualitative study and the immediate priority · Clip A 23:57.192

But yeah, separately down the line, I think it'd be kind of cool to like just like straight up like, put the language LM means the situation was like, oh, yeah, there's like this whole horrible thing that happened. Like, how does the model reason about it? That'd be a whole very interesting qualitative study. And in terms of like, people, I think people would be very interested, I think, in how like, this category of thing right now people do where they like subject these models are really weird situations, they're like, I'll look what it did, like they give it like a knife and have a baby and like you have to stab the baby, it's fake and then pull stab the baby or something.

Like, yeah, there's all these weird like things like this, right. But I think what's really interesting about this is that this is a very tricky situation where there's like a lot of like, like real harm happened. And we're at a point now in time where these systems are increasingly having a reason about like policy and so forth.

And so a different type of study that might take a lot more effort and a lot more collaboration with your collaborators who are like, I mean, even like people who are like the NGOs involved and so forth would be like, how do the models reason about this stuff versus like, versus like humans versus like lawyers versus like, you know, how they go.

That'd be a really cool evaluation to run in general. Yeah, I mean, that was at the crux at the very core. What I thought was cool about this would be like, if you try to make this as unsupervised as possible, what happens when the model comes up with like very different definitions of harm than the ones that like all the suits in the HEP in the UN have like kind of agreed on, you know, like this like framework and it's like, okay, these six kinds of harm, that would have been really cool to be like, well, like, you know, basically giving it less training meals

and letting it just learn like, these are quite different than like what you guys have kind of come up with in the last, you know, 10, 20 years of just like, yeah, academic type. So that, I'm saying that was kind of like an original motivation. Yeah, I guess you need to be very careful because this is like,

_[Personal aside omitted.]_

It's like so easy to want to do so many different things because it's so many cool things. Like when your project is lamer, it's easier to like to do it because it's like, gosh, I'm just making, I'm making a table versus like, I could like be like solving it.

_[Personal anecdote omitted.]_

But anyway, I think that like the, if you're careful, I think a really cool, you could use really cool stuff there. I think focusing for now on like, how do you use these tools for like discovery and like the extent to which like prompting them all a certain way or like incorporating expert data or like incorporating like moral frameworks improves the quality of the summary that you get.

And then I would focus on like, tossing the data, embedding it, seeing how different types of like, ways of like summarizing and then before you embed change the distribution. And then like, the clusters and then from there I would maybe say, how can I incorporate expert feedback? Can I get a look there? I think I need to find out something. Perfect. But you're probably going to be like, yeah. Thank you so much. Thank you. Yeah.

<a id="b01"></a>
## B01 · Predicting literal and figurative translation · Clip B 00:00.352

You can use the hidden states, you can use the hidden states or you can use the SAEs and think about classifier and this question of can you predict what the model is going to do before it does it and there's plenty of evidence you can do this for other traits I got really interested over the summer, I was like oh I can train a probe that predicts whether or not this thing's going to happen this thing's going to happen I don't think anyone's looked at this specifically

what you could do is you could say you could sample like 10 times or 20 times and you could actually have a way of tagging whether or not the model is you could have a way of saying is this metaphorical or not

I could make a language model, I guess you could probably make a judge over it that's fine, yeah kind of is always like oh, all the judges are like that's the idea a human is a judge, it's way worse sometimes I mean it's going to like spot check it and it's a class project yeah maybe before you publish it but like yeah,

I would do that because I would generally like 10 and or maybe I would do like the 11 but I would show you a bunch of outputs and then what I would try doing is can you predict the probability of a can you predict the probability of a metaphorical or not metaphorical response from the lead of the SAEs or from the hidden states directly right, and you can basically just see if you can do it

and now you can also see if it generalizes between languages if you have English or French or French to like French and German whatever these terms are, you can see if you can predict this as a feature across like different

I think I'm using the German point on French and Korean yeah, why not, that'd be kind of cool because it might turn out that if you use the SAEs or if you use just n states you can kind of predict like in some sort of like cross label way whether or not it's going to do one thing versus the other that would be great I think it would make more sense if it's not a very safe SAE is that kind of like for which one is kind of like more of a better starting point

if I was just going to do SAEs, then should I do n states?

I would do n states too because I think that like SAEs are like oh it might be more interpretable but like that information is also contained in the hidden state as well so I feel like I would do both yeah, I would probably do both of them but my sense would be really cool to see if you could basically predict what the model is going to do but the point I remember is that what the model is going to do is going to be kind of probabilistic so that would also be really cool to characterize as well

<a id="b02"></a>
## B02 · A probabilistic target and a probe · Clip B 02:47.352

I think an interesting part of this project would be just like the first part which is you prompt the model like how consistent is the model with distribution

and you could also run an experiment where you say be metaphorical then you add to the prompt you can be like when possible you can use the figurative translation and you could like for every for the model, for different models for one or two models, for each one of the models because they both have like free trade that's pretty easy beautiful but I was going to say like for I don't know what weird motivation about flights being called I don't know but it the

I think it would be really really cool to predict like for those two models you say okay can you predict what the probability is of them all being metaphorical and not metaphorical just baseline first given like given how much an input I think there's a few questions one is like do you predict using like infinite instates pretty well and particularly can you predict the probability that it will like go to use behavior

actually what I found works really well is doing a ridge regression on the log probability of something kind of works yeah I was like I was messing around with this over the over this summer for like refusal I was trying to predict perfusals using the instates and that worked pretty well but like you can train over you can like I think specifically you can like if you like smooth

_[Personal attribution omitted.]_

smooth log prop of the behavior you care about and then we'd progress on that

and then so the idea is you predict from that instate like the probability of that that behavior and then there's this question of like does that generalize between languages there's also a question of does it work better for SAEs and for non SAEs

and you don't even really need to do much steering for this project at first you can at least focus on the first part of the class you can focus on just classification I think yeah that makes sense just be loaded on time hey you can predict this stuff and then

<a id="b03"></a>
## B03 · Prompt interventions, steering, and novelty · Clip B 05:30.080

another thing you can try doing is that you prompt and you prompt with like you know you say where possible be literal or where possible be figurative and you can look at the effect that has on its distribution

another thing you can do is you can construct steering vectors I think by prompting it to be metaphorical versus not and then it's calculating the difference between those problems or something

so probably something you can prompt and say the instruction is here's a language be metaphorical here's a language be literal you can compute those in the states and the difference between the two of them that could be a way of opening steering but also classification because you could actually maybe like dot you know like you could use those in the states to kind of predict as your classifier that's maybe more out there or maybe less out there I don't know even sure but like there's lots of stuff you can do

I think the idea of can you predict the model's behavior from the in states on this question is really interesting and then from there you can go into like steering that would be my sense but also I'm I don't know does that seem reasonable to you?

yes okay I also just wanted to say that this is like a novelist that sounds like it would be I think so I'll tell you I didn't but I will say I wasn't familiar with the space literally it was like hey chat what paper is the most similar to this that exists I found that so I maybe take you with a grain of salt but no I think it is cool

I also think that like because there's a new toolkit in terms of like SAEs or even some of the stuff like probes and everything I feel like you could probably do a lot of really cool work that diverges from existing work I think there's enough here and you have new conclusions as well like I think there's a lot of different possibilities

yeah do you think that you're dancing to like this here like you know the result or like the normal I think a negative result is the slow result so okay yeah I was like ooh I don't want to like Yeah, I would say it was a slow result. And then in terms of like, how are they asking the base lines I think?

<a id="b04"></a>
## B04 · An interruption and midterm planning · Clip B 07:47.720

The FAA has grounded all flights nationwide.

_[Unrelated discussion of breaking news omitted.]_

Yeah, my last name was just for the, um, for the midterm. Do you think they'd be like a good start to like, first thing, to like, the first thing?

_[Student affiliation details omitted.]_

Yeah, I feel like, yeah, you gotta use the resources as soon as you have this class. I think, um, because of that, you can move pretty fast.

_[Personal and separate submission details omitted.]_

<a id="b05"></a>
## B05 · Baseline rates and cross-language prediction · Clip B 10:07.320

I think, um, yeah, I think that for you, I would recommend that I would just, like, run, I would compute that with those base stats.

Base stats first, where I would say, can you, like, basically, I would look at, like, the core, I would look, I think it would be really cool to look at, or you can give an input, like, the distribution of figure- not figurative, like, how, like, how consistent that is for a model. Like, does the model have, like, a lot of mass over the literal version of figurative translations?

And then, like, um, the extent to which you can predict that probability of, like, what it's gonna be figurative or not from, from the, in-state of the prompt. Either an essay you took of the prompt, or of a, like, or something that's stripped off of the in-state.

And there's also a question if that generalizes between languages as well. I mean, that's a really, that'd be a really good thing to run.

Okay, perfect. I think you can do that. And then you can do the correlation of, like, what, like, the essays, like, but it's kind of cool. Yeah, I think it would be cool. I think that'd be my sense. And then maybe it would, like, run more.

You have, like, you have some time for the ultimate weekend plan. The list. Yeah. Yeah. No. Yeah, yeah, yeah, yeah. But I would try to do perfect. I think, like, the, I think there'd be some really cool, I think, yeah, you could try a bunch of different things.

But from there you could also try the idea activation pattern as well. And what's cool is you have these baseline probabilities for these models. So you can see what, how do they shift? And you can probably just mention, isn't that cool?

<a id="b06"></a>
## B06 · Possible interventions and model choice · Clip B 11:51.112

I think another thing you can try. Yeah, I think one thing, one thing that's kind of cool is if you have a bunch of these two different information props where you have a bunch of continuations, and some of them are figurative, and some of them are literal.

So for every single prop you have, say, like, it turns out like one in, like, 10 is, like, figured it by default. And you can try doing, maybe you can try, like, hitting those, like, figurative samples and, like, trying, I think it's the chart methods that come, just kind of, like, you can increase the probability of those sequences and then see what happens, like, what's going on in the model when you do that. Like, you take your degree and out of probability, you get that continuation as, like, figurative.

Can you use that to, like, find the, um, can you just, like, find the region of the model that's handling this or something?

Yeah, absolutely. Um, but yeah, I think it's a lot you can do. I think I also, yeah, prompt the model to be, I think, quite a bit much in tight numbers, so probably the model thing, like, to figure out how to be figurative and also, like, just, like, maybe asking them how to be figurative and seeing how that shifts things would be really cool. So, like, just being able to base that number and then keeping it pretty similar and not just to be really neat. And that would be enough for me.

I think so. I think, like, if you have, like, some good results there on putting things and you have a clear direction, I think that would be enough. Um, also? I hope each one I need one. I don't know. I don't know. I just don't, like, I feel like as long as, like, I feel like, I think we are going to be able to do a lot of things. I think it's going to be harder on me on the proposal to find out in the terms of reports on the proposals, like, we'll work together and then we'll do some work on that. So, like, take good results there or whatever. Um, but I think it's, I think you could have time to just pull that up.

And then I just wanted to, like, I could say, so, the SAE, there's a gemma, like, these are just the ones that exist, so that's why I picked, like, a version of things like gemma or something and find something, like, what would you, oh yeah, I have quandary and gemma and string. But the gemma one is, like, instruct the clients to make models, because that's just, like, what they had.

Oh, those would be very, very different. Yeah. Actually, I would limit the instructions. Okay, so. How do you, like, prop the model, do, like, both of these shots, one thing? Yeah. I think I would get a instruct in.

Okay, so just the gemma. Yeah, because they use both of them, too, that'd be fair. I think more results for a one model is better than maybe lots of, like, results for them. So, I think, like, the less results for, like, you know, models. I think it'd be, like, one model would be fine. Um, but, yeah, a lot of SAEs, too. Maybe it should. I'm gonna charge a llama. I think maybe two models would be nice, but. Oh, it looks like they have this by what? Llama base. Oh, if it's community choice, llama 3.1, maybe it's--

In the setting for the SAE aren't available, you could just use the class five instance. Okay. Which is, um, the option. Okay.

<a id="b07"></a>
## B07 · Poetic constraints in reasoning · Clip B 15:08.864

Yeah, I'm kind of I'm a little bit stuck to constraining their reasoning changes and it's not doing it super well and I'm just using the time for finding 78 truck as you just need to ask it to you here like yeah, okay,

so here are the prompts that I have like for example for alliteration I don't know if it's a problem with like the way that I'm like some of them were finding alliteration

Yeah, so like for alliteration it works fine for anaphora I chose to just like use like give it a phrase to use because when I let it be free form it didn't follow it at all Yeah, but if I give it a phrase it does it for a couplets it's not doing it for a pistol PA also gave it a phrase

So it's like finding your thoughts, so I mentioned that It's a finding your results like okay, I do models around, but I would put more models around I would like try to see if we could put more models with the exact same thing

Okay, I'll try it on different models then But I'm wondering for like the rest of the experiment in and of itself should I continue just going through with this considering that they're not necessarily following instructions or

Like I'll show you the models are responding to the logic QA it like questions a lot worse than The GSM and T1 so if it's a rhyme scheme right this is like this is the reasoning change for using Which is just not at all Not at all to the rules versus You have a question? I would use you before because I think that is a model Yeah, I would try that out

But yeah, so suppose I get like mixed responses right like alliteration works alliteration is fine

And it loses the performance?

I haven't done more than just two So I don't know if it's improving the performance or not but this is just like testing to see whether the Instructions themselves follow through

yeah, so I would I think you just say is like take the settings when you do Get the instructions to follow through and then see that if that goes for me

Okay, because I know the feedback you gave me for My proposal either you or whoever Yeah, okay, the people you gave me was to make it a more robust thing and I like a lot more Poetic devices, but I feel like this is gonna axe a bunch of them because so far like well to be fair The main offenders right now are there's no line spacing for public this down That's just refuses to do it and if your syllable counts it can't count it just refuses to

<a id="b08"></a>
## B08 · Adherence, accuracy, and a rewrite control · Clip B 19:42.656

Yeah, so it's a negative It's like this face the fact that it's hard to like control using any models You can point this as a negative result and then I think what you do is you try to be for oh Okay, I would I would like And it may rest large scale evaluation on GP for the GPO is an expensive model, right?

But there's a model that gives you its reasoning So you can kind of go see the effect of this tax on the performance.

Yeah Do you think it's worth it for me to go through with this kind methodology? Even though I might end up with just a bunch of negative results

What should I have you can just filter down the cases where I actually follow the follow the restrictions you can report that This doesn't really work. You can report that you get late. It was like the model had it didn't really actually like

Um, I actually question. Can you actually also have the model? just like can you just ask the model to like generate the answer normally and then regenerate in Using that using the constraint so many of you should see is like in the model follow the constraint period

I see Like if I had if I have a bunch of these devices that I'm testing out and if for all of these I guess I Run the model make it reasonably and then make it rewrite in any of these That not be what's right?

So if I take the case where I want to model to reason normally and then rewrite it a year into one of these devices would that not be like a lot of test cases because I'm running for every question I'm running it through like eight of these devices and then It's for two data sets

I would also use pick some picks subset of these tests Kind of cool to actually just test with them all can actually adhere to constraint so you can say during the reasoning and now Regenerate the reasoning that you have a journey the reasoning and then have it rewrite it in that style And then you can look at like how that compares I think that would be what we do.

But I think, yeah, I think you- this is already a cool result, like the model, I think this, this result has been, I think some of the people, you have a sex finding that, like, the model, when you're trying to control a champ bot, and you just take ways, it doesn't like- it's not like you do it.

But I would do this for more than one, I would have that result for more than one model, you can include that in your mission report. Okay. But then I would like, then look at the actual accuracy and stuff. Right?

<a id="b09"></a>
## B09 · What belongs in the midterm report · Clip B 23:01.360

Okay, yeah, so what do you think I should differentiate between what I report for in my midterm report versus everything after that? Well, you should report what you've done. So, yeah. But I have like three more days.

_[Personal administrative details omitted.]_

I think that in your shoes I would do, if I would run this over multiple different models, and I would see what percent of the time it falls in constraint, and then in a setting where models do fall in constraint pretty regularly, what's the actual penalty to accuracy? Okay. How does it compare to no chain of thought? Right. Right, that's the baseline. How does it compare to, how does it compare to regular chain of thought and just like document that? Okay. And I feel like that's a very useful thing to do. Okay, that was fun. That was my question. Yeah. I would just like, I would just get multiple- Multiple models. Well, I'll look on that for you. I know.

_[Personal closing conversation omitted.]_
