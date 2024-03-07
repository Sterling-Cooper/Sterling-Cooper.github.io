---
layout: post
title: The Language of Learning
tags: agentive-language fundamental-attribution-error
---

As part of my research project (EL6013), I am exploring how to learn from failure. During this MA, our class have delved deep into writing style, tone, and how readers engage with our text. Much of what I have discovered about the language of learning is interesting in this context.

## Learning From Failure

I should explain why I’m interested in failure! My background is in software engineering. I have spent the last ten years developing and deploying services for a significant Software as a Service (SaaS) company. SaaS providers build software models of interrelated, increasingly automated services. These services run online in the cloud. Customers expect modern online systems to run 24 hours a day, 365 days a year. These expectations have only accelerated the complexity of this software. Given the pressures on these systems, it is impressive that they function effectively most of the time. However, they do fail, often in unexpected and unusual ways.

I am increasingly surprised by how our industry reviews these failures. The software industry often focuses on collaboration, positive culture, and employee well-being. Yet, rather than embrace the opportunity to learn, the default response to these failures is often to seek blame. Wondering why this is the case, I re-read the documentation for an existing review process. Terms like “corrective action”, “nonconformity”, "verdict", and “review board” suddenly struck me as ominous, perhaps even punitive. This thought led me to consider how terminology influences the outcome of a review. Can language explain our tendency to assign blame?

![PNG image representing blame by illustrating a shadow pointing at a businessman](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/language-blame.png?raw=true)
##### Figure 1: Shadow pointing and blaming (Canva/vchal n.d.).

## Human Factors

Some exploration in this area led me to the work of UAB’s [Crista Vesel](https://www.uab.edu/engineering/asem/people/faculty-directory/crista-vesel), a human factors and linguistic specialist. Professor Vesel's research on the importance of language in safety systems seems to resonate with this very question. Reassuringly, she explains that it’s a natural human instinct to want to know who or what was responsible for an action. In linguistic terms, this “assignment of action is called agency” (Vesel 2020, p.34). An agent of an action is the doer of that action.

| Language | Example |
| --- | ----------- |
| Agentive | “Sam made an error.” |
| Non-agentive | “An error was made.” |

This definition of agency reminds me of DuBay’s golden rules of documentation writing. Namely, to “use simple sentences, active voice, and present tense” (DuBay 2004, p.2). Students of last semester’s Principles of Technical Communication module (TW5221) will see the connection between **agency** and writing in the **active voice**. The active voice clearly identifies the action and who is performing that action.

| Voice | Example |
| --- | ----------- |
| Active | “Sam made an error.” |
| Passive | “An error was made.” |

By its nature, the active voice adds agency. As well as injecting purpose, the "active voice apparently conveys a sense of control and causation that is lacking in the passive voice" (Knobloch-Westerwick and Taylor 2008, p.732). But, this can also have the effect of administering judgement—knowingly or unknowingly.

## Fundamental Attribution Error

Lee Ross coined the term “fundamental attribution error” (Ross 1977, p.187) to describe how that judgement is introduced. It refers to how much a given action reflects something about the agent’s personality, as opposed to the various situational factors influencing the agent (Ross 2018).

“Sam made an error” illustrates fundamental attribution error. This statement does not consider whether Sam had incorrect instructions, was under extreme stress, or many other possibilities. What it achieves is to imply that Sam is the kind of person that makes errors. We, as readers, might think to ourselves, “I would never do that.” And so, by making a value judgement on Sam’s character, we create a separation between ourselves and Sam. And as a result of that separation, it becomes easy to **blame Sam**. Again, I now understand this is a natural instinct ([and to some degree a by-product of the English language](https://www.youtube.com/watch?v=I64RtGofPW8&t=3270s)), but assigning blame has consequences. One of these consequences is that it separates us from the network of conditions surrounding an event. It's crucial to surface these circumstances if we want to learn from the episode.

As a student of failure, I find this hugely interesting! If you can think of other examples of terminology influencing outcomes please do leave a reply. I’m no stranger to writing an incident review, but I now have another layer of considerations regarding the language I use. [I've written previously about my eagerness to write in the active voice](https://sterling-cooper.github.io/2024/03/04/challenges-of-internal-documentation.html). But I also need to be keenly aware of the purpose of my writing. I must balance my urge to improve readability with the proper use of agency. I still need to master the language of learning!

## References

Canva/vchal (n.d.) _Shadow pointing and blaming_ [PNG image], available: [https://www.canva.com/photos/MADT7bBwrDc-shadow-pointing-and-blaming-businessman/](https://www.canva.com/photos/MADT7bBwrDc-shadow-pointing-and-blaming-businessman/) [accessed 11 Mar 2024].

DuBay, W.H., (2004) _The principles of readability_, Impact Information, available: https://files.eric.ed.gov/fulltext/ED490073.pdf [accessed 11 Mar 2024].

Knobloch-Westerwick, S. and Taylor, L.D. (2008) 'The Blame Game: Elements of Causal Attribution and its Impact on Siding with Agents in the News', _Communication research_, 35(6), 723–744, available: [https://doi.org/10.1177/0093650208324266](https://doi.org/10.1177/0093650208324266).

Ross, L. (1977) ‘The Intuitive Psychologist And His Shortcomings: Distortions in the Attribution Process’, _Advances in Experimental Social Psychology_, 10(1), 173-220, available: [https://doi.org/10.1016/S0065-2601(08)60357-3](https://doi.org/10.1016/S0065-2601(08)60357-3).

Ross, L. (2018) ‘From the Fundamental Attribution Error to the Truly Fundamental Attribution Error and Beyond: My Research Journey’, _Perspectives on psychological science_, 13(6), 750–769, available: [https://doi.org/10.1177/1745691618769855](https://doi.org/10.1177/1745691618769855).

Vesel, C. (2020) ‘Agentive Language in Accident Investigation: Why Language Matters in Learning from Events’, _Journal of chemical health & safety (Online)_, 27(1), 34–39, available: [https://doi.org/10.1021/acs.chas.0c00002](https://doi.org/10.1021/acs.chas.0c00002).
