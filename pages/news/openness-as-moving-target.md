--- 
title: Openness as composite and gradient
description: "In which we introduce the European Open Source AI Index and explain how to follow a moving target"
date: 06-11-2024
---
# Openness as gradient and composite: Introducing the European Open Source AI Index

For the longest time, open-source software has been the key mental model for the notion of _open source_. Even if there was a large crop of licenses that differ on the finer points of redistribution, attribution, and so on, most people would agree that open source means the _source_ of a piece software can be openly inspected, adjusted, and redistributed. Developers like open source because it allows them to poke around to see how things work and contribute improvements and bug fixes. Users like open source because it provides a degree of transparency and security that is unmatched by a lot of software from proprietary vendors. As Linus' Law has it, many eyeballs make all bugs shallow.

Today, the advent of complex machine learning models considerably complicates the picture. What exactly is the _source_ of a large language model like [Llama](https://www.osai-index.eu/model/llama-3.1) or a text-to-image model like [Stable Diffusion](https://www.osai-index.eu/model/stable-diffusion)? Some argue it is at least the source code — the actual computer code written to train and fine-tune the model. Others argue that in addition, the training data is equally crucial. Without countless terabytes of text and imagery, usually scraped from the open web, none of these models would do anything. At the same time, the amount of computational power needed to even train such models is astronomical, and therefore only within the reach of a select few large companies. Is there a meaningful way in which such models can be reverse-engineerd or redistributed?

## Openness as a moving target

This is the problem of **openness as a moving target**. In today's complex sociotechnical landscape, single or simple definitions of "open source" won't suffice. Instead, we need more informed takes that allow us to distinguish the relevant _degrees_ and _dimensions_ of openness. One goal of the European Open Source AI index is to supply this information. The index is directly rooted in academic work on dimensions of openness in generative AI technology (Liesenfeld & Dingemanse, 2024; Solaiman, 2023). It aims to cut through the tangle of competing notions by recognising that openness is always a gradient and composite notion. What does that mean?

**Openness is gradient.** Some systems are more open than others. A commercial model provider like Meta (or Facebook AI Research) agressively markets its Llama models as "open source", but very little about Llama is actually open except for the model weights — the most inscrutable component. Smaller scale research-focused labs like AllenAI provide models like [OLMo](https://www.osai-index.eu/model/olmo-7b-instruct) that are much more open, as our index shows. The gradience of openness should make you wary of any simple claim of "open source AI". Inquiring minds want to know: _How open is it?_ 

::the-index
---
hideFilters: true
filters: 
  models: llama-3.1, olmo-7b-instruct
---
::

**Openness is composite.** Openness is composed of multiple elements. This means it is more like press freedom than like temperature. The World Press Freedom Index ranks countries by their press freedom, but this itself takes into account measures on multiple dimensions, including political context, sociocultural context, and legal framework. Likewise, the European Open Source AI index gathers information on the openness of generative AI systems in terms of three broad categories (each in turn composed of finer-grained features): availability, documentation, and access. Recognising the composite nature of openness makes it possible to be concrete about what is open about a model and to what extent. It allows us to answer the question: _How_ is it open?

Hovering over any model in our index will display the evidence we have of its openness across the three dimensions, further broken up into 15 features. You can also click "compare" to see multiple models side by side.

![Screenshot of OLMo openness features](/images/osai-index-olmo-openness-screenshot.png "OLMo openness features")

## Further reading

- Liesenfeld, A., & Dingemanse, M. (2024). Rethinking open source generative AI: open-washing and the EU AI Act. _Proceedings of the 2024 ACM Conference on Fairness, Accountability, and Transparency_ (FAccT ’24). doi: [10.1145/3630106.3659005](https://dl.acm.org/doi/10.1145/3630106.3659005) 
- Solaiman, I. (2023). The Gradient of Generative AI Release: Methods and Considerations. _Proceedings of the 2023 ACM Conference on Fairness, Accountability, and Transparency_, 111–122. doi: [10.1145/3593013.3593981](https://doi.org/10.1145/3593013.3593981)
