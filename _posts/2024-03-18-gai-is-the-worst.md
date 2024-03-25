---
layout: post
title: Generative AI is The Worst and I Hate It
tags: gai
---

There are many reasons not to like Generative Artificial Intelligence (GAI), but let’s start with this: _It’s exhausting_. Each new day brings a fresh onslaught of news, hype, and scare-mongering. I try _really_ hard not to roll my eyes as friends and colleagues excitedly excrete meaningless word goop like “process mining”, “decision intelligence”, and whatever this is:
> "Composite AI refers to the combined application (or fusion) of different AI techniques to improve the efficiency of learning to broaden the level of knowledge representations" (Perri 2023).

## Non-Existent Intelligence

I try _really_, _really_ hard not to roll my eyes when I read statements like “GPT-4 exhibits many traits of intelligence” (Bubeck _et al._ 2023, p.4). GPT-4 is a Large Language Model (LLM). LLMs are a type of GAI that ingests human language and generates text. **All** LLMs are context engines with no more sentience than a calculator. Even the most advanced LLM is human-driven. When asked to produce human-useful forms of information, these “intelligent” LLMs confidently shovel out [fictitious legal cases](https://www.theguardian.com/world/2024/feb/29/canada-lawyer-chatgpt-fake-cases-ai), [accounts of imaginary events](https://www.vice.com/en/article/k7zqdw/people-are-creating-records-of-fake-historical-events-using-ai), and references to phoney information (Alkaissi and McFarlane 2023).

The companies developing these glorified word sequencers assure us that GAI will stop providing deluded answers once the models are fed enough data. I have only two issues with this assertion. The first issue is that the amount of data necessary to match every possible input is unimaginably vast. The second issue is that GAI is already running out of data. GAI’s ascension has scraped every data resource legally found online, including communities like [Reddit](https://www.theverge.com/2024/2/22/24080165/google-reddit-ai-training-data) and [Stack Overflow](https://www.wired.com/story/google-deal-stackoverflow-ai-giants-pay-for-data/). No data on the Internet is safe from GAI’s unquenchable maw. [Not even our blogs](https://www.404media.co/tumblr-and-wordpress-to-sell-users-data-to-train-ai-tools/). So now [we have to create this data _for_ GAI](https://www.theverge.com/features/23764584/ai-artificial-intelligence-data-notation-labor-scale-surge-remotasks-openai-chatbots). How did we let the future of technology become synonymous with the [infinite monkey theorem](https://www.theguardian.com/science/2023/mar/20/can-you-solve-it-the-infinite-monkey-theorem)? (Borel 1913).

![PNG image illustrating an error message on a computer](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/gai-error.png?raw=true)
##### Figure 1: Error message on a computer (Canva/NA n.d.).

## And What of the Humans

With every breathlessly excited hype piece that comes out of Silicon Valley, I remember the talented human designers I spoke to for last semester’s interview assignment. I think about the concerns designers have about GAI [stealing their work](https://www.newyorker.com/culture/infinite-scroll/is-ai-art-stealing-from-artists). And I worry about how their wages might be cut now that they have to compete with an influx of people using GAI as a ladder (Frey and Osborne 2017).

In return for our data and wages, we receive a “shocking” amount of AI-translated garbage when we open our web browsers (Thompson _et al._ 2024). GAI is making it cheaper to generate lower-quality content. [Search](https://www.theregister.com/2024/01/30/ai_is_changing_search/), [news](https://www.bloomberg.com/news/articles/2023-05-01/ai-chatbots-have-been-used-to-create-dozens-of-news-content-farms), [social networks](https://www.wired.com/story/tiktok-platforms-cory-doctorow/), and even [Wikipedia](https://www.vice.com/en/article/v7bdba/ai-is-tearing-wikipedia-apart) are all swimming against the tide of junkification.

No critique of GAI would be complete without some [Orwellian](https://www.george-orwell.org/1984) hand-wringing. Let’s just say I am less than excited about the prospect of tech giants [deciding the correct version of historical events](https://arstechnica.com/information-technology/2024/02/googles-hidden-ai-diversity-prompts-lead-to-outcry-over-historically-inaccurate-images/). But at this point, I’ll probably be happy if they just let me [sell my goldfish](https://twitter.com/Carnage4Life/status/1761788333422690621).

## Programming

I wonder if I feel so dismissive of GAI because of my experience using GAI for programming.

I’m a software engineer who became a manager. I like to think of myself as a programmer who dabbles in the bureaucracy of middle management (the opposite is much closer to the truth). As a hobby, I resolved to create a conversational work assistant using Retrieval-Augmented Generation (RAG). I read an enthusiastic blog post on the topic and had already dabbled with open-source LLMs using [Ollama](https://ollama.com/). The gist of the idea is simple: feed my documents into an LLM running on my home computer by chunking them into small pieces, allowing me to have a Q&A-style chat about the contents of those documents (Lewis _et al._ 2020).

I start where I always start. I think about the problem for a few minutes (longer than I want to, but less than I need to). Then, I try to type out a couple of lines that don’t break when I run them together. The process continues like this. Solve one problem and move on to the next one. When I can’t solve a problem, I poke around in the API docs and ask [Stack Overflow](https://stackoverflow.com/). To me, this is programming. Or, it was.

After doing this for a little while, I remember I have a GAI LLM at my fingertips. Programming, now, is to ask the LLM to solve the problem for me. Actually, that’s not true either. Programming, now, is to prompt the LLM to complete the entire task for me. It’s then my job to assess how (upsettingly) correct it is. It’s easy to dismiss GAI (see above), but I can’t overestimate the significance of this change.

The first time I used a computer was when my Dad came home with an [IBM PC](https://en.wikipedia.org/wiki/IBM_PC_Series) in the mid-nineties. He set up a numbered menu in [DOS](https://en.wikipedia.org/wiki/DOS). Type 1 for Pac-Man. Type 2 for [Trek](https://dosgames.com/game/ega-trek/). My mind was blown. I thought he was a hacker. By 1995 standards, he might have been.

I studied computer science at University. Programming made sense to me. Boolean logic. Ones and zeroes. Instruction→response. The logical determinism of code is comforting. Computers don’t create bugs. Humans only give computers incorrect instructions. Programming is an often frustrating profession with an unshakeably simple truth at its base.

I leaned into automation. I dove head-first into the world of [DevOps](https://books.google.ie/books/about/Accelerate.html?id=Kax-DwAAQBAJ&redir_esc=y). I took delight in building things that made other types of work obsolete. For years, I told my colleagues that our goal was to automate ourselves out of a job. By eliminating all rote tasks, I declared that “the business will celebrate our success and find another important problem for us to solve.” Of course, I was emboldened to make such a statement because I thought it was utterly unachievable. Now I wonder whether it is actually happening. Maybe this is where my hostility towards GAI comes from. What will become of this thing I’ve spent so much time on?

![PNG image illustrating a person's relection in a monitor displaying programming code](https://github.com/Sterling-Cooper/Sterling-Cooper.github.io/blob/main/_assets/gai-coding.png?raw=true)
##### Figure 2: Computer programming (Canva/LPETTET n.d.).

## The Way Out
```
“He says the best way out is always through.
And I agree to that, or in so far
As that I can see no way out but through” (Frost 1939, p.83)
```
I have changed my mind on GAI before and will no doubt [change my mind again](https://sterling-cooper.github.io/2024/03/25/gai-is-the-best.html). Let me know how GAI makes you feel today by leaving a comment. Regardless of how I feel on any given day, I find the idea that we might [pause GAI development](https://futureoflife.org/open-letter/pause-giant-ai-experiments/), or any other technological advancement, to be unrealistic. The best way out is through. On our way through, I hope GAI will give me some new problems to solve.

## References

Alkaissi, H. and McFarlane, S.I. (2023) ‘Artificial hallucinations in ChatGPT: implications in scientific writing’, _Cureus_, 15(2), available: [https://doi.org/10.7759/cureus.35179](https://doi.org/10.7759/cureus.35179).

Borel, É. (1913) ‘La mécanique statique et l’irréversibilité’, _J. Phys. Theor. Appl._, 3(1), pp.189-196, available: [https://doi.org/10.1051/jphystap:019130030018900](https://doi.org/10.1051/jphystap:019130030018900).

Bubeck, S., Chandrasekaran, V., Eldan, R., Gehrke, J., Horvitz, E., Kamar, E., Lee, P., Lee, Y.T., Li, Y., Lundberg, S., Nori, H., Palangi, H., Ribeiro, M.T. and Zhang, Y. (2023) ‘Sparks of Artificial General Intelligence: Early experiments with GPT-4’, _arXiv.org_, available: [https://doi.org/10.48550/arxiv.2303.12712](https://doi.org/10.48550/arxiv.2303.12712).

Canva/LPETTET (n.d.) _Computer programming code_ [PNG image], available: [https://www.canva.com/photos/MAED0z-nCdA-computer-programming-code/](https://www.canva.com/photos/MAED0z-nCdA-computer-programming-code/) [accessed 18 Mar 2024].

Canva/NA (n.d.) _Error message on a computer_ [PNG image], available: [https://www.canva.com/photos/MAC8RqH7mCg-error-message-on-computer/](https://www.canva.com/photos/MAC8RqH7mCg-error-message-on-computer/) [accessed 18 Mar 2024].

Frey, C.B. and Osborne, M.A. (2017) ‘The future of employment: How susceptible are jobs to computerisation?’, _Technological forecasting & social change_, 114(1), 254–280, available: https://doi.org/10.1016/j.techfore.2016.08.019.

Lewis, P., Perez, E., Piktus, A., Petroni, F., Karpukhin, V., Goyal, N., Küttler, H., Lewis, M., Wen-tau Yih, Rocktäschel, T., Riedel, S., and Kiela, D. (2020) ‘Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks’, _arXiv.org_, available: [https://doi.org/10.48550/arxiv.2005.11401](https://doi.org/10.48550/arxiv.2005.11401).

Perri, L. (2023) _What’s New in Artificial Intelligence from the 2023 Gartner Hype Cycle_, Gartner, available: [https://www.gartner.com/en/articles/what-s-new-in-artificial-intelligence-from-the-2023-gartner-hype-cycle](https://www.gartner.com/en/articles/what-s-new-in-artificial-intelligence-from-the-2023-gartner-hype-cycle) [accessed 18 Mar 2024].

Thompson, B., Mehak Preet Dhaliwal, Frisch, P., Domhan, T. and Federico, M. (2024) ‘A Shocking Amount of the Web is Machine Translated: Insights from Multi-Way Parallelism’, _arXiv.org_, available: [https://doi.org/10.48550/arxiv.2401.05749](https://doi.org/10.48550/arxiv.2401.05749).




