---
layout: post 
title: Working In Public
---

## What's the best incentive structure for free and open source software? 

*Working in Public* is a book about open source software. It's by Nadia Eghball (I've mispelled her names a few times in this review, surely). In a nutshell, it tries to answer why people make open source software, why it's valuable, and how we might want to structure our incentive structures to support it. If one is to value a book based on how much, if at all, it can change your mind (borrowing that from a [Patrick Collison interview with Tyler Cowen](https://www.youtube.com/watch?v=Mk2VnlSz1Kc), then I suppose this book was decent. It was more informative than anything, this beigna  topic I hadn't thought much about until now. But it was a thoroughly entertaining read, so I'd certainly recommend it to anyone with some sort of interest in software or software adjacent-topics. And I'd doubly recommend it to anyone that thinks that open source software is not important or not complicated. 

The jumping off point of this work is basically this - since Github came around, it's become easier than ever to share and consume open source software. The "platform model" has done with software the same thing that Twitter and Instagram have done with the content of creators - by making material so easy to share to such wide audiences, we've created a network of economies and relationships where most of the content is produced by a small group of dedicated producers, for free, for an incredibly large group of consumers. As one reddit user pointed out, it turns out that most of the content on the internet is made by people who, for whatever peculiar reason, spend a majority of their time making content on the internet. 

So what does that mean? Open source software and the ethos thereof have been a thing for decades. Linux, Python, Javascript, cURL -- all of these projects built by a small handful of people in service of pure love of producing and an allegiance to the idea that information should be free -- ["free as in freedom, not as in beer"](https://www.gnu.org/philosophy/free-sw.en.html#:~:text=Roughly%2C%20it%20means%20that%20the,as%20in%20“free%20beer.”). What does the platform model change? 

Fundamentally - it changes little about the distribution of who makes software. Egball argues (and I'm inclined to agree, given the evidence she presents) that this is more a peculiar function of humans than of anything else (30% of all english wikipedia articles were written by one man, for example). But what it _does_ do is make the attention of those developers imminently more accessible. 

### "information wants to be free"
Most of the intro to the book was new to me, but more like the trivia sort of new , not the conceptual sort. The first theoretical contribution i found useful was a brief exposition on software as a commodity, which, for whatever reason, I haven't done much thinking about. It makes sense, but working through it for the first time was fun. The basic premise: 

> If goods are non-rival, then charging a per-unit price to users artificially restricts distribution: to truly maximize social welfare you need a system that supplies everyone whose willingness to pay for the good is greater than the marginal cost of producing another copy. And if the marginal cost of reproduction of a digital good is near-zero, that means almost everyone should have iit for almost free. 
> 
> However, charging price equal to marginal cost almost surely leaves the producer bankrupt, with little incentive to maintain the product except the hope of maitenance fees, and no incentive whatsoever to make another one except that warm fuzzy feeling one gets from impoverishing oneself for the general good. 

For a good that's non-rivalrous (e.g., two users can consume as cheaply as one)  and non-excludable (the producer cannot control the distribution of the good), code in its static state doesn't lend itself easily to being analyzed economically. It's more of a public good than anything. 

Now, of course, there's some clear differences. Code doesn't scale like breathable air scales. At a certain threshold, it is actually quite expensive to host and share even static software (although, I suppose breathable air ceases to scale at some point, if you go high enough. or deep enough. luckily [hopefully?], we probably won't have to worry about extra terrestrial economics for a little while). The platform model of github has merely outsourced those infrastructural costs to a level of abstraction that gives the good the veneer of true zero-marginal cost. 

The main contribution (in my view) of Egball's book is a framework for thinking about open source code as *public infrastructure*. Something which does have significant cost, especially at scale, but one sufficiently abstracted away from the consumer such that it doesn't really factor into microeconomic decisions. The maintainer of an open-source project "pays" the marginal costs of Github's cloud hosting, security, and maitenance in the same way that a truck driver pays for a municipal bridge. And the value of that project, just like the value of the bridge, is a direct function of its active dependencies -- irrespective of its cost of construction or maitenance. The cost of maintaining existing infrastructure isn't necessarily a measure of the value of transportation capital to the economy. as the economy and population change, so does the value of the infrastructure. 

There's a few caveats (like substitutability) which factor into the model, but that's more or less the jist. The value of open source code -- which can be reproduced for effectively zero marginal cost -- is a function of the following counterfactual: 
1. If it didn't exist, how much would it cost to reproduce it? 
2. How much money/time does the code save us? 
3. What does the code allow us to do whcih we otherwise could not? 

The last piece of the puzzle is to assert that despite the fact that static open source code has zero marginal cost, that sort of code is not valuable. Why? Because code is only non-rivalrous when there is zero maintenance costs, and code can only have zero maintenance costs when it's static. And, almost by definition, code of any notable value is always under maitenance: 
1. If it's valuable, that means (see above) that, in one way or another, there's a nontrivial amount of other projects that depend on that code
2. That code maintains zero marginal cost **if and only if** it is in a *static state* e.g., it's a binary file sitting somewhere to be downloaded for free 
3. If it's in a static state, then it will not be updated 
4. If it's not updated, then it it will eventually fall behind phase with its dependencies 
5. If it no longer supports its dependencies, then it will cease to be valuable. 

So we want to study valuable open source code, and we know that those sorts of projects are the ones that are actively maintained. We also, know, then, that, economically speaking, valuable open source code is a commons -- like a forest. It's non-excludable, since we can't really control who shares the product with whom, but it *is* rivalrous, since code is expensive to maintain. 

What, then, is expensive about maintenance? On the face of it, it's pretty trivial. It's the time for the maintainers of the project to review pull requests, moderate discussion boards and bug reports, and educate new users and contributors. This is sort of what I've seen as the most common point of entry for an analysis of open source software, from which the conclusion is typically something like "ok, we just need to pay maintainers to do maintenance". 

But that's a limited view of the systems we're looking at. First of all, it's lazy thinking. It attempts to solve a broad problem (which isn't even a problem, in a lot of cases) with two few parameters and too limited a model of the dynamics at work. Second, it betrays a fundamental misunderstanding of why people write open source software in the first place. There's all sorts of ancillary benefits, but, ultimately (and, though I agree, this is mostly backed anecdotally and generally presented without proof) people make open source code *because they like to code*. Not because they like providing feedback on pull requests and answering "how-to" questions. And that's why it works! Passionate individual contributors produce a shockingly significant portion of publicly available software (the first thirty pages of the book are filled with evidence on that), and at least part of the success of open source software is in allowing those contributors to make what they enjoy making, and freely share what they've made. 

So what is it that's expensive about maitenance? Well, it *is* the time for maintainers to do maintenance. It really is that trivial. But, more specifically, it's the *opportunity cost of their attention*, which is *demanded* by users to whom the maintainers are now beholden, and would otherwise be used to contribute to the project. So Egbal sort of asserts that, well, the most efficient way to economically support open source is to address this attention issue. How? By providing some sort of incentive structure to maintain the **value** of the software, on the one hand (by supporting the **production of code**), and limit the **costs** of maintaining the software, on the other, by constraining the supply of user demands. I found two particular points pretty compelling here: 

#### 1. Induced Demand 
The relationship between maintenance work and the available attention of the maintainer seems to have a sort of induced demand effect, like highway traffic -- that's why the "pay maintainers to maintain" and "hire more moderators" approaches don't really work. It turns out that the more attention (in gross) you divert to fielding maintenance issues, the more the proportion of your attention you spend fielding maintenance issues. One quote bears writing down (and, personally, shouting from the rooftops at my office to anyone who'll listen): 

> The threat of induced demand explains why the solution to managing extractive contributions is not always to add more contributors, but to draw clearer boundaries between which types of tasks are worth allocating **anyones** attention to and which can be safely ignored. Rather than asking "How do we do **everything** that's required of us?", the better question is "How do we assess what's most important to do?"

#### 2. *Extractive contributions*
Are attempts at contributions to a project (well-intentioned or not) that cost more than they provide in value. They're a reality. And given the induced demand phenomenon, the only way to protect the attention of the maintainers such that the project can continue to flourish is to eliminate them as much as possible. 

What Egbal eventually sort of advocates for is a sort of "club" model, where open source projects are available for anyone to view and use, but only serious contributors, which pay some sort of price (either through labor or cash), are able to participate and contribute. She acknowledges the potential conflicts with the ethos of open source, but I'll concede that I think those concerns are pedantic more than anything, and these restrictions are ultimately in service of protecting the real ethos of open source, which is the freedom of coders to produce what they want, when they want, and for whomever wants it -- free as freedom, not beer. 

I'm sure there's a broader conclusion to be made here on the type of thinking that the author is putting on display, which I suppose is probably the main element of value I got from the book. Her solution (which, again, is limited, because what we're implicitly calling a "problem" isn't really, generally speaking, a problem) is grounded in a construction of the fundamental economic bricks and social mortar that come together to make the world of open source. 
### Closing thoughts? 
If I had to leave my review with any sort of original idea, I'd say that Eghbal may have underrepresented the analogy between Github:code and a platform like spotify and the content hosted there. I think there's a similar type of relationship between producer and consumer (excluding big-name artists with record deals) with the notable caveat that spotify is missing the maintenance costs of collaboration that an open source project has. At minimum, the analogy works because every spotify "project" is the work of an individual contributor, or, at least, every spotify artist only has one person with "commit privileges". And the analogy holds up in the economic sense; music on spotify is non-excludable (mostly), and just as tenuously non-rivalrous. Once music is made, the cost of distributing it on spotify to more users is effectively zero, until one factors in the hidden social cost of reputation and the expectation for reproduction. You don't "maintain" a spotify album, but if you want to grow your following there's a tacit assumption that you'll produce more music and cultivate some sort of public presence. I consider those costs that a musician is beholden to by their listeners to be analogous to the costs that coders are beholden to by their users and contributors. 

To the extent that the analogy works at all, I think it may pose an interesting model for monetizing open source software. If we want to incentivize maintainers to continue their work-- which we should-- a platform like Github could follow spotify and allow every user to view and use Github-hosted code for free, and raise funds via a subscription, which would give payers the option to contribute, comment on, and make requests to projects. Might work, though there's definitely a potential problem with the platform (rather than the developers themselves) controlling who has access to the developers attention.

All in all, I'm (regrettably) not really involved enough in the production of open source software to have gained any sort of immediate or material value from reading this book. I'll admit that most of the enjoyment I got was in the intellectual exercise of thinking through the macro and microeconomics of software production, which was relatively new to me. The history of the open source movement was pretty compelling, and I wish that the author touched on some of those topics more, though I did come across the following links in the notes, which I hope to read soon: 
- [Coase's Penguin - Linux](https://www.benkler.org/CoasesPenguin.PDF)
- [Open Source is not about you](https://gist.github.com/g1eny0ung/9e7d4d0f72547a8d156452e76fa8f7a3)
- [The death and life of great american cities](http://www.petkovstudio.com/bg/wp-content/uploads/2017/03/The-Death-and-Life-of-Great-American-Cities_Jane-Jacobs-Complete-book.pdf) (not about open source software, but a tangentially related work on city planning and problems therein, especially as they pertain to the planning of cities as static. Got it from the note on software as infrastructure.)