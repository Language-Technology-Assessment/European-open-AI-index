--- 
title: Openness as moving target
description: "Openness as moving target: definitions and licenses"
date: 06-11-2024
---
# Openness as moving target: definitions and licenses

For the longest time, open-source software was the key mental model for the notion of open source. Precise definitions vary, and there is a large crop of licenses that differ on the finer points of redistribution, attribution, and so on, but most people agree that open source means  that the _source_ of a piece software can be openly inspected, adjusted, and redistributed. Developers like open source because it allows them to poke around and see how things work. They can also contribute improvements and bug fixes. Users like open source because it provides a degree of transparency and security that is unmatched by a lot of software from proprietary vendors. As Linus' Law has it, many eyeballs make all bugs shallow.

Today, the advent of complex machine learning models considerably complicates the picture. What exactly is the _source_ of a large language model like [Llama](https://www.osai-index.eu/model/llama-3.1) or a text-to-image model like [Stable Diffusion](https://www.osai-index.eu/model/stable-diffusion)? Some argue it is at least the source code — the actual computer code written to train and fine-tune the model. Others argue that in addition, the training data is equally crucial. Without countless terabytes of text and imagery, usually scraped from the open web, none of these models would do anything. At the same time, the amount of computational power needed to even train such models is astronomical, and therefore only within the reach of a select few large companies. Is there a meaningful way in which such models can be reverse-engineerd or redistributed?

This is the problem of **openness as a moving target**. In today's complex sociotechnical landscape, single or simple definitions of "open source" won't suffice. Instead, we need more informed takes that allow us to distinguish the relevant _degrees_ and _dimensions_ of openness. One goal of the European Open Source AI index is to supply this information. The index is directly rooted in academic work on dimensions of openness in generative AI technology (Liesenfeld & Dingemanse, 2024). It aims to cut through the tangle of competing notions by recognising that openness is always a gradient and composite notion. What does that mean?

**Openness is gradient.** Some systems are more open than others. A commercial model provider like Meta (or Facebook AI Research) agressively markets its Llama models as "open source", but very little about Llama is actually open except for the model weights — the most inscrutable component. Smaller scale research-focused labs like AllenAI provide models like [OLMo](https://www.osai-index.eu/model/olmo-7b-instruct) that are much more open, as our index shows. The gradience of openness should make you wary of any simple claim of "open source AI". Inquiring minds want to know: _How open is it?_ 

::the-index
---
hideFilters: true
filters: 
  models: llama-3.1, olmo-7b-instruct
---
::

**Openness is composite.** Openness is composed of multiple elements. This means it is more like press freedom than like temperature. The World Press Freedom Index ranks countries by their press freedom, but this itself takes into account measures on multiple dimensions, including political context, sociocultural context, and legal framework. Likewise, the European Open Source AI index gathers information on the openness of generative AI systems in terms of three broad categories: availability, documentation, and access. Each of these in turn consists of multiple finer-grained features like source code and training data, technical and scientific documentation, and API and licensing. The composite nature of openness gives us tools to be concrete about what is open about a model and to what extent. It allows us to answer the question: _How_ is it open?

- Liesenfeld, A., & Dingemanse, M. (2024). Rethinking open source generative AI: open-washing and the EU AI Act. _The 2024 ACM Conference on Fairness, Accountability, and Transparency_ (FAccT ’24). doi: [10.1145/3630106.3659005](https://dl.acm.org/doi/10.1145/3630106.3659005) 
- Widder, D.G., Sarah West, & Meredith Whittaker. 2023. Open (For Business): Big Tech, Concentrated Power, and the Political Economy of Open AI. doi: [10.2139/ssrn.4543807](https://doi.org/10.2139/ssrn.4543807)


It means we must interrogate notions of openness and refine definitions of "open source".
