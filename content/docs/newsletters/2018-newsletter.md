---
title: 2018-November-Newsletter
---

# Long time, no see…

It’s been a while since I shared any news from the outer world. Doesn’t necessarily mean I stopped reading or caring about the world or you, it just was a difficult year for me. But it’s time to restart this activity, hopefully with more feedback this time! :)

Before we really start, I’d like to thank Shawn McGhee and Marek Kumpost for their suggestions, corrections and help with this. All the typos and grammar mistakes are mine though.

Take a sip from your morning coffee and let’s dive into my notes!

## The Death of Expertise

As a first story, I’d like to share an article that resonated with me strongly – [The Death of Expertise](http://thefederalist.com/2014/01/17/the-death-of-expertise/). Why? Because many and many of the article paragraphs actually expressed my observations. Like this one:

> In politics, too, the problem has reached ridiculous proportions. People in political debates no longer distinguish the phrase “you’re wrong” from the phrase “you’re stupid.” To disagree is to insult. To correct another is to be a hater. And to refuse to acknowledge alternative views, no matter how fantastic or inane, is to be closed-minded.

Please, read the article too. I consider it worth every minute of your precious time.

And now, let’s get to the less serious stuff!

## Dealing with Time is Easy, Right?

Every security analyst has to deal with time, from time to time (silly joke, I know). There is a general agreement that UTC solves the known issues of dealing with various timezones and daylight savings. But honestly, what do _you_ know about the time? Could you remember the rules for the leap years? Does GMT have daylight savings?

There are way more interesting glitches in the whole ‘people dealing with time’ problematics. Let me quote one paragraph here:

> Beyond that, though, there’s also a lot about time itself that is properly hilarious, and it’d be a travesty to not talk about the country that recently decided to skip a certain day, or that the Unix epoch isn’t technically the number of seconds since January 1970, or that February 30 happened at least twice in history.

Has it caught your curiosity? Good! Continue with reading at [UTC is Enough for Everyone, Right?](https://zachholman.com/talk/utc-is-enough-for-everyone-right).

I remember that some are not much into reading, so don’t worry, I got you covered – Zach gave a speech at a conference and it’s available on YouTube: [Closing Keynote by Zach Holman on "UTC is Enough for Everybody, Right?](https://www.youtube.com/watch?v=aEvB98CstOk)

## Machine Learning

### Machine Learning’s ‘Amazing’ Ability to Predict Chaos

In new computer experiments, artificial-intelligence algorithms can tell the future of chaotic systems. Not sure whether it’s scary or fascinating (both, probably?), but the article goes through some basics of chaos theory and shows how the machine learning predicted one chaotic system way better than any other technique.

> After training itself on data from the past evolution of the Kuramoto-Sivashinsky equation, the researchers’ reservoir computer could then closely predict how the flamelike system would continue to evolve out to eight “Lyapunov times” into the future, eight times further ahead than previous methods allowed, loosely speaking. The Lyapunov time represents how long it takes for two almost-identical states of a chaotic system to exponentially diverge. As such, it typically sets the horizon of predictability.

Go ahead and get scared too!

*   Link: [Machine Learning’s ‘Amazing’ Ability to Predict Chaos](https://www.quantamagazine.org/machine-learnings-amazing-ability-to-predict-chaos-20180418/#comments)

### Machine Learning failures

No matter how awesome and powerful the machine learning technology is, it can fail. And it can [fail hilariously](https://twitter.com/Smingleigh/status/1060325665671692288)!

> I hooked a neural network up to my Roomba. I wanted it to learn to navigate without bumping into things, so I set up a reward scheme to encourage speed and discourage hitting the bumper sensors. It learnt to drive backwards, because there are no bumpers on the back.

More examples can be found in this shared [Google Drive document](https://docs.google.com/spreadsheets/u/1/d/e/2PACX-1vRPiprOaC3HsCf5Tuum8bRfzYUiKLRqJmbOoC-32JorNdfyTiRRsR7Ea5eWtvsWzuxo8bjOxCG84dAg/pubhtml).

### Big Data Random Links

The links below are not really random, but I don’t want to spend much time talking about them – they are both about using Jupyter Labs or Jupyter Notebooks for data analytics. There are many reasons for doing so, nicely explained in the first linked article, so I’ll just emphasis one of them – repeatability of the analysis process. It’s very useful for anyone else validating your research, and it can be used for teaching and trainings as well.

*   [Why Jupyter is data scientists’ computational notebook of choice](https://www.nature.com/articles/d41586-018-07196-1)
*   [Interactive notebooks: Sharing the code](http://www.nature.com/news/interactive-notebooks-sharing-the-code-1.16261)

And it can be integrated with many other data analysis systems too!

### Machine Learning Courses

Quick list of the great resources to ML:

*   [Machine Learning, by Andrew Ng](https://www.coursera.org/learn/machine-learning) – recommended by a friend of mine!

Other great course:

*   Advanced stuff: [Neural Networks for Machine Learning, by Geoffrey Hinton](https://www.coursera.org/learn/neural-networks) – the links seems to be broken now, but it’s more like an internal error on Coursera side, as it's still listed as available.

Btw, did you know that a huge deal of DNA analysis is about statistics and probability? [Bayes’ theorem to convict a murderer](http://www.wall.org/~aron/blog/bayes-theorem/)!

## Programming

Our company has an incredible number of developers. Very smart developers. It’s always easier to deal with them if you know how they think. Therefore, I dedicate a portion of my spare time to teach people programming; both at work and at the university in Brno. I know it could be observed as a non-necessary skill for a security analyst, but it also provides grounds that prove to be useful for many other fields. And I believe we need to train people for problems that do not exist yet.

### How to think like a programmer

And what could be a better opening than a famous quote?

> “Everyone in this country should learn to program a computer, because it teaches you to think.” — Steve Jobs

We often need to deal with complex systems – and the complex systems bring a lot of complex problems. It’s easy to get overwhelmed by these and that’s where the programming skills (or some algorithmic thinking) could be a huge benefit and an ally. Problem solving is a skill; and as such, it can be learned and trained.

*   Link: [How to think like a programmer — lessons in problem solving](https://medium.freecodecamp.org/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2)

And as a side note, for the real programmers in the audience – we all know that the syntax doesn’t matter, as we all can write Fortran code in any language! (The following article is almost as old as I am, but it’s still good! :))

*   Link: [Real Programmers Don’t Use PASCAL](https://www.ee.ryerson.ca/~elf/hack/realmen.html)

### What’s a Sparse Merkle Tree?

Blockchain technologies are still popular, even though the payment systems are bit declining these days. However, there is still a lot to be learned from all the principles leveraged within the cryptocurrency designs. Sparse Merkle Trees are one of them. Good stuff! Hashes included!

> If you’ve been around the Ethereum research community lately, you might’ve heard of something called a sparse Merkle tree. They might sound scary, but they’re really quite simple. This post will explain exactly what a sparse Merkle tree is, why they’re cool, and what they’re currently being used for.

*   Link: [What’s a Sparse Merkle Tree?](https://medium.com/@kelvinfichter/whats-a-sparse-merkle-tree-acda70aeb837)

## Vulnerabilities

Vulnerability management is a fast moving work, dealing with all the new vulnerabilities as fast as possible. No way I could cover all the latest announcements – and I don’t have any aspirations to do so, we have a specialized team for this. But how about some retrospective? What if we look more into what now seems to be a more generic problem?

### CPU Vulnerabilities Summary & History

Designing a piece of silicon that’s as huge and complex as current processors is unimaginable for me. I have absolutely no clear idea about how anything of this complexity could be designed at all. And we have seen recently that doing the design right is not easy for the huge and skilled companies either.

Let me quote one nice tweet here:

> Allow me to summarize x86 side channel attacks:
> 
> *   Spectre v1: speculation is insecure by design
> *   Spectre v2: secure branch prediction matters
> *   Meltdown: Intel are dumbasses
> *   L1TF: Intel are monumental, inexcusable dumbasses
> *   PortSmash: hyperthreading is insecure by design

And there’s more:

> CacheBleed, MemJam, PrefetchSideChannel, TLBleed, RetSpectre, Other Spectre variants, various attacks on L1, L2, L3 cache. Various attacks on arithmetic units are all serious x86 side channels.

*   Link: [https://twitter.com/marcan42/status/1058404388794847232](https://twitter.com/marcan42/status/1058404388794847232)– and it’s worth reading through the whole thread.

But are these vulnerabilities indeed so novel and surprising?

Most of the world got suddenly scared by the new attacks popping out of nowhere. Was it unexpected, though? The novel part of it was to have a working exploit, definitely – that finally got the companies addressing the issues and brought it into more public audience. However, the problem (side-channel attacks on CPUs) has been observed and reported years ago. Like here: [Side channel attacks: Intel vs. AMD](http://www.daemonology.net/blog/2006-04-20-side-channel-intel-amd.html), in the article from 2006! Also, notice the differences in the communication and approaches between Intel and AMD.

Last, but not least, side-channel attacks; they are an amazing security-research field. So let’s use some Wikipedia definition here just to give you some brief idea should you need it:

> In [computer security](https://en.wikipedia.org/wiki/Computer_security "Computer security"), a side-channel attack is any attack based on information gained from the [implementation](https://en.wikipedia.org/wiki/Implementation "Implementation") of a computer system, rather than weaknesses in the implemented algorithm itself (e.g. [cryptanalysis](https://en.wikipedia.org/wiki/Cryptanalysis "Cryptanalysis") and [software bugs](https://en.wikipedia.org/wiki/Software_bug "Software bug")). Timing information, power consumption, [electromagnetic](https://en.wikipedia.org/wiki/Electromagnetic_radiation "Electromagnetic radiation") leaks or even [sound](https://en.wikipedia.org/wiki/Acoustic_cryptanalysis "Acoustic cryptanalysis") can provide an extra source of information, which can be exploited.

### Super-Micro Story

One reading pertinent to the CPU vulnerabilities could be about the Super Micro company and the mystery of an extra chip on their mother boards. You’ve read it and many other pertinent articles too, so I’d rather ask you – what do you think of the story? Is it real? Is it not?

*   Link: [Decoding the Chinese Super Micro super spy-chip super-scandal: What do we know – and who is telling the truth?](https://www.theregister.co.uk/2018/10/04/supermicro_bloomberg/)

Experts are not convinced much, more reading can be found at:

*   Link: [Investigating Implausible Bloomberg Supermicro Stories](https://www.servethehome.com/investigating-implausible-bloomberg-supermicro-stories/)
*   Link: [@KimZetter Twitter Thread](https://twitter.com/KimZetter/status/1054457602761838594)

## Interesting Books

One year is such a long time I don’t really remember every interesting book I’ve read, so this is mostly taken from my Goodreads list. Feel free to find me there, I’d like to know more about your books too :)

### The Phoenix Project: A Novel About IT, DevOps, and Helping Your Business Win

Our company is perfectly organized and with rock-solid processes, indeed. But there are companies less lucky than ours and they had to get over various IT issues. They had fought the battles the new companies can learn from – and this book is exactly about the IT management.

Personally, I didn’t like how everything was easy in the book (I’ve spent too much time in corporates), but the overall inspiration is still useful.

*   tl;dr: Implementing SixSigma methodology in IT is helpful, even though some may find it unlikely and difficult to believe.
*   Link: [The Phoenix Project: A Novel About IT, DevOps, and Helping Your Business Win](https://www.goodreads.com/book/show/17255186-the-phoenix-project "The Phoenix Project: A Novel About IT, DevOps, and Helping Your Business Win")

### The Signal and the Noise: Why So Many Predictions Fail - But Some Don’t

Being in security usually means someone will eventually ask you for metrics and predictions. And we all know that _“… it is very hard to predict, especially the future…”_ (Niels Bohr).

Been there, done that, I assume, right? The book I am about to recommend deals with the predictions and what could impact their accuracy. All supported by real stories and past events, illustrating why the lack of data can be as dangerous as the sh\*t load of rubbish data.

*   tl;dr: Read it. It’s fun and it’s useful. You may understand better why Bayes’ Theorem is so important. Has chapters about poker, stock market and weather forecasting!
*   Link: [The Signal and the Noise: Why So Many Predictions Fail - But Some Don’t](https://www.goodreads.com/book/show/13588394-the-signal-and-the-noise)

### The Best Sci-Fi in Years? The Three-Body Problem!

I have no idea how to write a proper book review (you may have noticed that already :)), so just quickly – for many years, I was looking for a good, scientific sci-fi story. The Martian by Andy Weir was great, creating such a great story with a minimalistic, scientific approach. The Three-Body Problem is different. It covers hundreds of years, it’s both technical and psychological, it tries to discover the behavior of humankind under different conditions; and it’s Chinese. It really feels unlike anything I’ve read before, and I loved the books, the whole trilogy!

*   Link: [The Three-Body Problem](https://www.goodreads.com/book/show/20518872-the-three-body-problem)

## Concluding Words

It’s my hope you found at least one bit interesting. Way too many articles and links didn’t make it to this issue (like my notes and links to Riemann hypothesis and why is it important and whether the proof was or wasn’t accepted by the experts), but I believe there will be more newsletters sent soon.

I’d like to repeat why I think this is important for our team. I quoted this in the past, so this is just a reminder:

> _“Knowledge and productivity are like compound interest. \[…\] The more you know, the more you learn; the more you learn, the more you can do; the more you can do, the more the opportunity – it is very much like compound interest. I don’t want to give you a rate, but it is a very high rate. Given two people with exactly the same ability, the one person who manages day in and day out to get in one more hour of thinking will be tremendously more productive over a lifetime.”_

*   Link: [You and Your Research](http://www.cs.virginia.edu/~robins/YouAndYourResearch.html)

And let me ask you a rhetorical question – how much of the _“one more hour of thinking (one hour of learning)”_ we can do during our BAUs? How much have we planned for it?

Last, but not least – please, help me to make this newsletter better! Your help, links, topic and editing suggestions, any corrections… they will be appreciated and you’ll get a credit. And you'll gain instant fame! :)
