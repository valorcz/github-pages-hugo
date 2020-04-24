---
title: "2020-January"
author: "Vašek Lorenc"
---

# A Very Long Good Bye

>  _“I didn’t have time to write a short letter, so I wrote a long one instead.”_  
>  ― Mark Twain  
  
Good news, everyone! A new issue of my very irregular
(not-so-much-about-security-now) newsletter is out!
  
My original idea of publishing this every quarter (or so) was clearly too
optimistic, as you can see. Which leads to a huge problem -- there's a load of
links and texts I'd like to share with you, and the length of the text could be
demotivating, I know. On the other hand, you can always skim the text, check
for your favorite sections (if there are any), and maybe you'll find something
new you didn't know before. That would make me super happy, as that's the
purpose of these annoyingly long posts.

Also, plenty of the news aren't real news, as I started writing this in
November 2018.   

Happy reading!

## Randomness

This newsletter is usually organized in a random order, which gives randomness
the right to start this particular issue. Have you ever realized how important
the randomness is? It took me a while (and I needed help from my PhD
colleagues) to realize how critical component to the whole security field this
is. The past months were proving it a lot, so let's jump to our first section
and topics.

### The curious case of 7zip approach to randomness

[https://threadreaderapp.com/thread/1087848040583626753.html][2]

Not everything mentioned on Stackoverflow is perfect. Not everything that could
be found there is technically correct. And definitely not everything there is
well designed. _"Didn't review it but it should be fine."_ is a sentence you
don't want to hear when it comes to anything related to security. Especially if
it's about password protection of your favorite sensitive packed files. (If you
don't know what IV in that article stands for, it's Initialization Vector, the
thing used at the beginning of many cryptography primitives)

### Cracking passwords in 2 seconds

[https://link.medium.com/4h2AkytYHT][3]

Achieving confidentiality could be difficult in eGov world, especially if you
need to distribute something to people who don't have their passwords set or
the technology doesn't support custom passwords. But you can choose a scheme
that's good enough, like 
`first_four_letters_of_name_in_uppercase + year_of_birth`. 
Basically there are 4 uppercase alphabets & 4 digits involved,
which means 2821109907456 combinations; and it would take 90 years to crack the
password if we try 1000 combinations per second. However, not all combinations
were born equal, which you can observe immediately. And the article describes
it even better.

### Beat slot machines by science

[https://www.wired.com/2017/02/russians-engineer-brilliant-slot-machine-cheat-casinos-no-fix/][4]

Honestly, I am not sure whether I shared this (rather old) story with you before or not. It's my favorite story about the importance of good randomness, with a grain of brilliant reverse engineering, some casinos, slot machines, Russians, 1 Czech guy (yay!), and the high-level information that a good cryptologist joining the dark side could earn huge money. Last, but not least, it's very well written, so please, if you have some time, read it.

## Incident Response

### When your external communication sucks

[https://techcrunch.com/2018/12/03/marriott-data-breach-response-risk-phishing/amp/][5]

Incident response is a tricky area – company management wants updates immediately and often, the team needs to process gigabytes/terabytes of data, situation is usually complicated with inter-personal relationships in a company, lots of stress everywhere. Plenty of things can go wrong.. and as you can guess, it's sometimes very obvious. Let's see how NOT to communicate with publicwhen an incident happens.

## Disk Encryption

### Google disk encryption function

[https://security.googleblog.com/2019/02/introducing-adiantum-encryption-for.html][6]

AES is an encryption standard. The encryption standard, and for many security professionals, it's the only encryption standard. But in security, it's rarely 'one size fits them all'. And because I have a friend who worked hard in the field of disk encryption, he spoke highly about the new function introduced by Google. I think it's good to know about options, especially if we are supposed to design our solutions well.

## Programming

Not sure I should keep the section here, as some of the interesting articles and blogposts weren't much about security, yet I found them worth reading and sharing.

### A fork() in the road

[https://www.microsoft.com/en-us/research/uploads/prod/2019/04/fork-hotos19.pdf][7]

It was sad to see how little I knew about fork() implementation. Copy-on-write? Sure, I knew. File handles? Yes, I was aware. Threads? Hmm, not so much. The overall design of fork() on the modern systems? Not at all. Least privilege principles violated by fork() are obvious when mentioned specifically, but not always obvious. The mere complexity of fork() for contemporary applications like Chrome, Apache or PostgreSQL was unexpected. The linked article sums it up very nicely -- the origins of fork(), the identified problems, complexity issues, possible solutions to it (I've learned about spawn()). And it also emphasized the fact that if you want to implement fork() in your OS kernel, you may end up designing the whole kernel around it.

### Sheng, a small but fast Deterministic Finite Automaton

[https://branchfree.org/2018/05/25/say-hello-to-my-little-friend-sheng-a-small-but-fast-deterministic-finite-automaton/amp/][8]

Since I learned about finite automata theory during my university studies, I got super excited about it. While theoretical at first sight, the possible applications were endless (regexes, iptables, utf-8 validation, credit card protocols, game engines; you name it). "Sheng" is just another DFA, yet I enjoyed reading the article, as it's very technical (CPU instructions, L1 cache) and the Sheng's focus is on simplicity.

### How We Wrote a Self-Hacking Game in C++

[https://link.medium.com/91oDdU8TAU][9]

I can probably say it safely now, as it's been decades since it happened -- I learned x86 assembly mostly because I wanted to understand how games were written (a kind of reverse engineering) and along the way, I also learned how to make effective cheats and/or copy-protection bypasses. Ahem. You know it now. Yet it was a great lecture -- learning how others wrote a code and being able to craft tiny patches changing the behavior of the game just slightly enough to give me an edge. And now, it seems there's a game encouraging everyone to do exactly this! The article is about the initial idea and the C++ implementation of such a game.

### HTTP security headers

[https://www.netsparker.com/whitepaper-http-security-headers/][10]

NetSuite, as a web-application company, is built around HTTP(s). Our application engineers are amazing in understanding all the details of the HTTP traffic, various headers and their uses, and sometimes we need to understand those too. This article is just a brief overview of some interesting/important headers. Not all of the mentioned headers are valid anymore, as web is a fast moving landscape ([https://ordina-jworks.github.io/security/2018/02/12/HPKP-deprecated-what-now.html][11])

## Books / Generic Wisdom

### Algorithms to Live By: The Computer Science of Human Decisions

[https://www.amazon.com/Algorithms-Live-Computer-Science-Decisions/dp/1627790365][12]

During World War II, researchers at the Center for Naval Analysis faced a critical problem. Many bombers were getting shot down on runs over Germany. The naval researchers knew they needed hard data to solve this problem and went to work. After each mission, the bullet holes and damage from each bomber was painstakingly reviewed and recorded. The researchers poured over the data looking for vulnerabilities. The data began to show a clear pattern -- most damage was to the wings and body of the plane. The solution to their problem was clear. Increase the armor on the plane's wings and body.

But there was a problem. The analysis was completely wrong. Before the planes were modified, a Hungarian-Jewish statistician named Abraham Wald reviewed the data. Wald had fled Nazi-occupied Austria and worked in New York with other academics to help the war effort. Wald's review pointed out a critical flaw in the analysis. The researchers had only looked at bombers who’d returned to base. What was missing from the data? Every plane that had been shot down and never made it back to the base.

We call it a "survival bias" now.

And the book contains a lot of other useful examples (sorting, selection algorhitms, overfitting, ...). Just avoid reading its Czech translation, it didn't go well and plenty of the used terms have verymisleading, too creative translations.

### The Intelligence Trap: Why Smart People Make Dumb Mistakes

[https://www.amazon.com/Intelligence-Trap-Smart-People-Mistakes/dp/0393651428/][13]

_Jack is looking at Anne but Anne is looking at Goerge. Jack is married but George is not. Is a married person looking at an unmarried person? (Yes/No/Cannot be determined)._

Can you answer the previous question? And is your answer right? Because the intuition in this part usually doesn't work, and finding the right answer usually takes more thinking than it seems.

But the book has a plenty of other great examples when our intelligence comes to wrong conclusions. Why smart people make dump mistakes? In other words, why a high IQ in itself is not enough to guarantee success in any area of life? Even a nobel prize awareded person can still believe in flath earth, or any other nonsense.

If you trust your brain a lot, and it never failed you in the fields it was trained on, why should it be failing in other areas, right? 

### Weapons of Math Destruction

[https://www.amazon.com/Weapons-Math-Destruction-Increases-Inequality/dp/0553418831/][14]

Machine learning is a tool, and as a such, it can be used in good ways and horrible ways. This book describes how good intentions and poorly designed models (can) lead to horrible results. We could probably put a tagline to it: _M__achine_ _L__earning__: Tested on humans_.

### Mental Models I Find Repeatedly Useful

[https://link.medium.com/TWCYY48W0S][15]

### Claude Shannon: How a Genius Solves Problems

[https://link.medium.com/kLiVKtlelS][16]

Not a book, actually, just an article I found when I was searching some extra information about Claude Shannon. And yet I find the article well written (and relatively short), so if you are not familiar with Mr. Shannon and his work, this could be a good start.

## Linux / Other

### LD\_PRELOAD: The Hero We Need and Deserve

[https://blog.jessfraz.com/post/ld\_preload/][17]

LD\_PRELOAD is a powerful mechanism many Linux people used for some reason (either legit or less legit). To check some very cool use-cases, follow the links, it's very inspirational! Things like influencing random-number-generators (RNGs) for poor SSH key generation, convincing programs to work with unsupported environment, enabling rapid-fire in Quake3 Arena, disabling SSL certificate validation.. Endless possibilities!

### TCP BBR + DCTCP

TCP BBR: [https://blog.apnic.net/2017/05/09/bbr-new-kid-tcp-block/][18] and [https://link.medium.com/deFX8IC2KU][19]

DCTCP: [https://www.kernel.org/doc/Documentation/networking/dctcp.txt][20]

There's only one TCP we use in networks, right? It starts with the three way handshake, and it continues with some packages; and the transmissions in confirmed. It's designed so well, that it can handle variability in the bandwidth, it can deal with errors, it's basically pretty awesome. And the original design is very generic, which brings some sub-optimal performance in many specific situations.

TCP congestion control/algorithms represent one huge family of how TCP performance can be improved under specific conditions. TCP BBR is one example, DC-specific TCP (or DCTCP, as it's being referred) is another example.

### TLS Fingerprinting

[https://link.medium.com/Cd29DgPDwT][21]  
[https://engineering.salesforce.com/open-sourcing-ja3-92c9e53c3c41][22]

HTTPS and it's end-to-end encryption makes our IDS probes almost irrelevant (especially with TLS 1.3), and it's one of the reasons why a visibility into a network traffic becomes more and more challenging. Various papers and mechanisms were designed to deal with the increasing complexity (starting with basic netflow analysis, more complex statistical approaches, ending with machine learning).

But a smart idea can be a huge life savior – what if you start focusing on a moment when a TLS connection is being established, for example, which ciphers are supported by a client? What if you design a standardized way of making this a signature (a fingerprint)? Could it identify a potentially malicious clients? You bet 

### eBPF, XDP

XDP == Express Data Path, a lot of hardware offloading. Extended Berkeley Packet Filter (eBPF), a generalized concept of including a bytecode from userspace to kernel in a safe way. Why should we bother? Well, we'd love to use it one day for our Suricata deployments! Don't get confused, it's not only about packets, it's way more flexible. Generally, it's a great technological improvement that started in 1992.

*   [https://thenewstack.io/linux-technology-for-the-new-year-ebpf/][23]
*   [https://qmonnet.github.io/whirl-offload/2016/09/01/dive-into-bpf/][24](a lot of links, even from 2019)
*   [https://blogs.igalia.com/dpino/2019/01/07/introduction-to-xdp-and-ebpf/][25]
*   [https://sematext.com/blog/linux-kernel-observability-ebpf/][26]
*   And the whole great thread starting at [https://twitter.com/qeole/status/1101450782841466880][27]

And don't get mistaken – eBPF is a whole new approach to many other topics in Linux world. Performance measurements (I’ll hopefully mention it in some further newsletters), security policies enforcement (e.g. you can check and enforce encryption algorithms used by applications/system); the replacement for iptables (and for nftables a direct successor to iptables) will use eBPF.

It's very likely we'll see eBPF mentioned in the projects we've been using – Suricata team adopted these some time ago, Illumio and Tanium may have started updating their products to leverage it as well.

### SSH News

Signed SSH certificates

*   [https://www.vaultproject.io/docs/secrets/ssh/signed-ssh-certificates.html][28]

CASSH: SSH Key Signing Tool

*   [https://link.medium.com/FgMEFRA5vS][29]

## Blockchain

### Once hailed as unhackable, blockchains are now getting hacked

[https://www.technologyreview.com/s/612974/once-hailed-as-unhackable-blockchains-are-now-getting-hacked/amp/][30]

**Lessons learned:** if you call something unhackable, make sure people can't hack it.

The huge advertised benefit of crypto currencies (also the reason for them for being invented) was the lack of a central authority. It was the community, whoever got engaged to the crypto project, and the mathematics making sure everything is sound and no one could cheat. The blockchain, the history of all transactions, is validated by multiple entities at the same time, so whoever would like to cheat (like double-spending a coin) would have to gain a majority in the system, to convince the rest of the validation group about the attacker's source of truth. And gaining that majority is economically inefficient.. for some crypto coins.. but not for all of them.

_"In total, hackers have stolen nearly $2 billion worth of cryptocurrency since the beginning of 2017, mostly from exchanges, and that’s just what has been revealed publicly."_

## Machine Learning

### word2vec

[https://skymind.ai/wiki/word2vec][31]

{{< hint info >}}
_"King" -"Man" + "Woman" = "Queen"_  
_"Library" - "Books" = "Hall"_  
_"President" - "Power" = "Prime Minister"_  
{{< /hint >}}
  
The equations above look unexpected, yet they make some sort of sense, don't they? Call me Cpt. Obvious, but I learned about "word2vec" just recently. First, it was because it was invented by another Czech guy working at Google and I saw an interview with this guy accidentally; second because it's an incredible mechanism and I found it difficult to believe it really works. word2vec is an algorithm that transforms words into vectors ("word embedding algorithm"), so that words with similar meaning end up laying close to each other. That enables plenty of algorithms to work with words efficiently. Btw, it wasn't really clear from the beginning why the word2vec math works so greatly that it allows the math over words, and other teams spent time explaining it ([https://p.migdal.pl/2017/01/06/king-man-woman-queen-why.html][32])

### GAN: Generative Adversarial Networks

[https://link.medium.com/5T14H12cQT][33]

If it's adversarial, then it needs to be related to security somehow, right? I guess that's not how English works, even though it'd make the language more foreigners-friendly :) Back to the topic though -- you've surely heard of "deepfake" (aka real-time facial reenactment, [https://www.youtube.com/watch?v=gLoI9hAX9dw][34]). All these were created by GANs, Generative Adversarial Networks, which you can read more about in the linked article. The process of training a GAN is taken from game theory called the minimax game, that's where the "adversarial" comes from. One neural network generates content, the other network tries to distinguish whether the given content is real or fake.

Are all the GANs inherently evil? Not at all, it's just a tool. On the good side, you can for example improve game textures with GANs ([https://www.extremetech.com/gaming/282695-modders-are-using-ai-to-overhaul-old-games-textures-with-gorgeous-results][35]), giving games like Doom 2, Morrowind or Max Payne remastered graphics in almost no time (well, not entirely true, but it definitely saves a lot of human effort). Next step could be the remaster of 3D models to make them more detailed. Or this [https://tcwang0509.github.io/pix2pixHD/][36] project, in which you start with Microsoft Paint and end up with a photo-realistic image.

Related Links:

*   [https://thispersondoesnotexist.com/][37]
*   [https://www.thiscatdoesnotexist.com/][38]
*   [https://thisresumedoesnotexist.com/][39]
*   [https://stackroboflow.com/][40](this StackOverflow question does not exist)

### ZeroAlpha

[https://www.nytimes.com/2018/12/26/science/chess-artificial-intelligence.html][41]

Computers have been winning games of chess for years now, by leveraging many various strategies, past game recordings, handful of heuristics, etc. But what if the only thing you give to the ML algorithm is just the rules?  
  
I'll quote the article here, as it left me speechless:

> _Most unnerving was that AlphaZero seemed to express insight. It played like no
> computer ever has, intuitively and beautifully, with a romantic, attacking
> style. It played gambits and took risks. In some games it paralyzed Stockfish
> and toyed with it. While conducting its attack in Game 10, AlphaZero retreated
> its queen back into the corner of the board on its own side, far from
> Stockfish’s king, not normally where an attacking queen should be placed._
> 
> _Yet this peculiar retreat was venomous: No matter how Stockfish replied, it
> was doomed. It was almost as if AlphaZero was waiting for Stockfish to realize,
> after billions of brutish calculations, how hopeless its position truly was, so
> that the beast could relax and expire peacefully, like a vanquished bull before
> a matador. Grandmasters had never seen anything like it. AlphaZero had the
> finesse of a virtuoso and the power of a machine. It was humankind’s first
> glimpse of an awesome new kind of intelligence._

### Data sets

Just a link here, it's been a lot of my text already.

[https://www.altexsoft.com/blog/datascience/best-public-machine-learning-datasets/][42]

### CyberSecurity ML 101

[https://towardsdatascience.com/machine-learning-for-cybersecurity-101-7822b802790b][43]

If nothing I wrote above made sense to you and besides my English it was mostly
because you didn't understand the terms, don't worry -- there's this page where
you can read some basic definitions and get some initial pointers as well as
ideas for using ML for network and endpoint protection, application security,
and user and process behavior.

Also, you can combine it
with [https://www.youtube.com/watch?v=aircAruvnKk][44] video (_But what \*is\* a
Neural Network? | Deep learning, chapter 1_, by 3Blue1Brown channel) which I
recommend as well

## Demoscene

[http://www.lofibucket.com/articles/64k\_intro.html][45]

And my favorite personal topic (more on the programming side), so just a brief
annotation taken from the article:

> "The demoscene is about producing cool real time works (as in “runs on your
> computer”) called _demos_. Some demos are really small, say 64 kilobytes or
> less, and these are called _intros_. The name comes from “crack intros”. So
> an intro is just a demo that’s small.
>
> I’ve noticed many people have interest in demoscene productions but have no
> idea how they are actually made. This is a braindump/post-mortem of our
> recent 64k intro _Guberniya_ and I hope that it will be interesting to
> newcomers and seasoned veterans alike. This article touches basically all
> techniques used in the demo and should give you an idea what goes into making
> one. I refer to people with their nick names in this article because that’s
> what _sceners_ do."

[1]: https://confluence.corp.netsuite.com/display/~vlorenc/INDEX%3A+Security+Newsletter
[2]: https://threadreaderapp.com/thread/1087848040583626753.html
[3]: https://link.medium.com/4h2AkytYHT
[4]: https://www.wired.com/2017/02/russians-engineer-brilliant-slot-machine-cheat-casinos-no-fix/
[5]: https://techcrunch.com/2018/12/03/marriott-data-breach-response-risk-phishing/amp/
[6]: https://security.googleblog.com/2019/02/introducing-adiantum-encryption-for.html
[7]: https://www.microsoft.com/en-us/research/uploads/prod/2019/04/fork-hotos19.pdf
[8]: https://branchfree.org/2018/05/25/say-hello-to-my-little-friend-sheng-a-small-but-fast-deterministic-finite-automaton/amp/
[9]: https://link.medium.com/91oDdU8TAU
[10]: https://www.netsparker.com/whitepaper-http-security-headers/
[11]: https://ordina-jworks.github.io/security/2018/02/12/HPKP-deprecated-what-now.html
[12]: https://www.amazon.com/Algorithms-Live-Computer-Science-Decisions/dp/1627790365
[13]: https://www.amazon.com/Intelligence-Trap-Smart-People-Mistakes/dp/0393651428/
[14]: https://www.amazon.com/Weapons-Math-Destruction-Increases-Inequality/dp/0553418831/
[15]: https://link.medium.com/TWCYY48W0S
[16]: https://link.medium.com/kLiVKtlelS
[17]: https://blog.jessfraz.com/post/ld_preload/
[18]: https://blog.apnic.net/2017/05/09/bbr-new-kid-tcp-block/
[19]: https://link.medium.com/deFX8IC2KU
[20]: https://www.kernel.org/doc/Documentation/networking/dctcp.txt
[21]: https://link.medium.com/Cd29DgPDwT
[22]: https://engineering.salesforce.com/open-sourcing-ja3-92c9e53c3c41
[23]: https://thenewstack.io/linux-technology-for-the-new-year-ebpf/
[24]: https://qmonnet.github.io/whirl-offload/2016/09/01/dive-into-bpf/
[25]: https://blogs.igalia.com/dpino/2019/01/07/introduction-to-xdp-and-ebpf/
[26]: https://sematext.com/blog/linux-kernel-observability-ebpf/
[27]: https://twitter.com/qeole/status/1101450782841466880
[28]: https://www.vaultproject.io/docs/secrets/ssh/signed-ssh-certificates.html
[29]: https://link.medium.com/FgMEFRA5vS
[30]: https://www.technologyreview.com/s/612974/once-hailed-as-unhackable-blockchains-are-now-getting-hacked/amp/
[31]: https://skymind.ai/wiki/word2vec
[32]: https://p.migdal.pl/2017/01/06/king-man-woman-queen-why.html
[33]: https://link.medium.com/5T14H12cQT
[34]: https://www.youtube.com/watch?v=gLoI9hAX9dw
[35]: https://www.extremetech.com/gaming/282695-modders-are-using-ai-to-overhaul-old-games-textures-with-gorgeous-results
[36]: https://tcwang0509.github.io/pix2pixHD/
[37]: https://thispersondoesnotexist.com/
[38]: https://www.thiscatdoesnotexist.com/
[39]: https://thisresumedoesnotexist.com/
[40]: https://stackroboflow.com/
[41]: https://www.nytimes.com/2018/12/26/science/chess-artificial-intelligence.html
[42]: https://www.altexsoft.com/blog/datascience/best-public-machine-learning-datasets/
[43]: https://towardsdatascience.com/machine-learning-for-cybersecurity-101-7822b802790b
[44]: https://www.youtube.com/watch?v=aircAruvnKk
[45]: http://www.lofibucket.com/articles/64k_intro.html
