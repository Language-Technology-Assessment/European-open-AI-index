---
title: "Lumo: the least open 'open' model we've seen"
description: Proton sets a new record in open-washing
date: 2025-08-29
author: Mark Dingemanse
status: published
---
# Lumo: the least open 'open' model
<author :author="author"></author>
<date :date="date"></date>

Proton, the privacy-friendly internet service provider based in Europe, has jumped on the LLM bandwagon and released an LLM service [last month](https://proton.me/blog/lumo-ai) called Lumo. Besides touting its privacy features, Proton's PR focuses on open source:

> Unlike other AI assistants, my code is fully open source, so anyone can verify that it’s private and secure — and that we never use your data to train the model. ([source](https://lumo.proton.me/about))

Elsewhere on the Proton website, we find a claim that Lumo is "based upon open-source language models". A comparison table shows Lumo alongside some other LLM assistants, with a feature "Opens source code for the public" prominently checked for Lumo and DeepSeek. Factcheck: for [DeepSeek](https://osai-index.eu/model/deepseek-v3) that is definitely not the case; at best it is an open weights model and very little is known about its source code. Does Lumo fare any better?

![Comparison table from the Proton website](/images/lumo-screenshot-20250829.png "Lumo screenshot")

It turns out that Lumo hits a new record in openness: it is the least open "open" model that we have ever added to our index. One of our [reasons for inclusion](https://osai-index.eu/news/introducing-eu-osai-index) is an openness claim: a model provider that calls a model "open" or "open source" or a variation on that. Lumo is "open" in that sense (Proton calls it open source) but in no other way. Nothing about it is currently open.

Here is a comparison of the openness status of Lumo and two well-known other models in the space: DeepSeek (included in Proton's own comparison), and [OLMo](https://osai-index.eu/model/OLMo) from AllenAI, the current leading openness champion. 

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: OLMo,deepseek-v3,lumo
---
::

In the past, we've gotten model providers like [Mistral](https://osai-index.eu/model/mistral) retreat from using the term "open source" and instead use the more precise "open weights". But Proton will need to do more work to get there, as they don't even reach the middling openness levels of Mistral and other model providers evasive about training data.

On the sunny side: the only way from here is up. Literally disclosing anything, from training data to model weights to model architecture to data sheets, will be an improvement over the current status. We will be following its rise with great interest.  

It may be that Lumo is a bespoke fine-tuned version of an open weights model like Mistral, OLMo or Llama. It may be a wrapper for an API from Anthropic or another provier. It may be all of these things together in a trenchcoat. The point is: we would know if it were truly open source. 
