--- 
title: Introducing the European Open Source AI Index
description: "In which we introduce the European Open Source AI Index and explain how to follow a moving target"
author: Mark Dingemanse & Andreas Liesenfeld
date: 2025-02-24
status: published
---

# Introducing the European Open Source AI Index
<author :author="author"></author>
<date :date="date"></date>

New generative AI models are popping up everywhere and claims about openness abound. When we launched [Opening Up ChatGPT](https://opening-up-chatgpt.github.io/) in July 2023, it was the first global openness index for instruction-tuned large language models. Soon it featured over 50 models from >25 model providers. However, not everyone likes looking at enormous tables with more models and features than you can handle. Often, what people need is specific guidance on the [best models to use in education](https://www.osai-index.eu/guides/open-llms-education), a comparison [Llama versus Bloom](https://www.osai-index.eu/guides/llama-vs-bloom-openness), or just a quick list of [all models that provide source code as well as scientific documentation](https://www.osai-index.eu/the-index?type=text&preprint=1&trainingcode=1).

We designed the European Open Source AI index to facilitate this form of flexible information sharing. You can check out a growing number of [guides](https://www.osai-index.eu/#guides), or sift through the [model index](https://www.osai-index.eu/the-index) using fulltext search and a comprehensive set of filters. We welcome your requests for guides and your suggestions for new models to include or data points to update. [See here](https://www.osai-index.eu/contribute) for how to contribute.

Read on to learn about about how to navigate today's Open Source AI landscape. Or just start exploring the index on your own. 

Happy browsing!

## Why openness needs a rethink

For the longest time, open-source software has been the key mental model for the notion of _open source_. Even if there was a large crop of licenses that differ on the finer points of redistribution, attribution, and so on, most people would agree that open source means the _source_ of a piece software can be openly inspected, adjusted, and redistributed. Developers like open source because it allows them to poke around to see how things work and contribute improvements and bug fixes. Users like open source because it provides a degree of transparency and security that is unmatched by a lot of software from proprietary vendors. As Linus' Law has it, many eyeballs make all bugs shallow.

Today, the advent of complex machine learning models considerably complicates the picture. What exactly is the _source_ of a large language model like [Llama](https://www.osai-index.eu/model/llama-3.1) or a text-to-image model like [Stable Diffusion](https://www.osai-index.eu/model/stable-diffusion)? Some argue it is at least the source code — the actual computer code written to train and fine-tune the model. Others argue that in addition, the training data is equally crucial. Without countless terabytes of text and imagery, usually scraped from the open web, none of these models would do anything. At the same time, the amount of computational power needed to even train such models is astronomical, and therefore only within the reach of a select few large companies. Is there a meaningful way in which such models can be reverse-engineered or redistributed?

## Navigating the Open Source AI landscape

Today, **openness is a moving target**: single or simple definitions of "open source" won't suffice. Instead, we need more informed takes that allow us to distinguish the relevant _degrees_ and _dimensions_ of openness. One goal of the European Open Source AI index is to supply this information. The index is directly rooted in academic work on dimensions of openness in generative AI technology (Liesenfeld & Dingemanse, 2024; Solaiman, 2023). It aims to cut through the tangle of competing notions by recognising that openness is always a gradient and composite notion. What does that mean?

**Openness is gradient.** Some systems are more open than others. A commercial model provider like Meta (or Facebook AI Research) agressively markets its Llama models as "open source", but very little about Llama is actually open except for the model weights — the most inscrutable component. Smaller scale research-focused labs like AllenAI provide models like [OLMo](https://www.osai-index.eu/model/olmo-7b-instruct) that are much more open, as our index shows. The gradience of openness should make you wary of any simple claim of "open source AI". Inquiring minds want to know: _How open is it?_ 

Here are two models at opposite ends of our openness scale. Both bill themselves as "open source". Only one of them is. In views like this you can also click "compare" to see multiple models side by side. Here's a direct link to [compare Llama 3.1 and OLMo 7B](https://www.osai-index.eu/compare?models=olmo-7b-instruct,llama-3.1). 

::the-index
---
hideFilters: true
filters: 
  models: llama-3.1, OLMo
---
::

**Openness is composite.** Openness is composed of multiple elements. This means it is more like press freedom than like temperature. The World Press Freedom Index ranks countries by their press freedom, but this itself takes into account measures on multiple dimensions, including political context, sociocultural context, and legal framework. Likewise, the European Open Source AI index gathers information on the openness of generative AI systems in terms of three broad categories (each in turn composed of finer-grained features): availability, documentation, and access. Recognising the composite nature of openness makes it possible to be concrete about what is open about a model and to what extent. It allows us to answer the question: _How_ is it open?

Hovering over any model in our index will display the evidence we have of its openness across the three dimensions, further broken up into 15 features. Here's a grid view of OLMo-7B's openness features:

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: OLMo
---
::

## Further reading

- Liesenfeld, A., & Dingemanse, M. (2024). Rethinking open source generative AI: open-washing and the EU AI Act. _Proceedings of the 2024 ACM Conference on Fairness, Accountability, and Transparency_ (FAccT ’24). doi: [10.1145/3630106.3659005](https://dl.acm.org/doi/10.1145/3630106.3659005) 
- Solaiman, I. (2023). The Gradient of Generative AI Release: Methods and Considerations. _Proceedings of the 2023 ACM Conference on Fairness, Accountability, and Transparency_, 111–122. doi: [10.1145/3593013.3593981](https://doi.org/10.1145/3593013.3593981)
