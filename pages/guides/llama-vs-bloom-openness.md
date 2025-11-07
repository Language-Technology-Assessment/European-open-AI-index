---
title: Llama and BloomZ: shades of openness
description: Comparing two models that claim to be open
date: 12-10-2024
author: Mark Dingemanse
---
# Llama and BloomZ: shades of openness
<author :author="author"></author>
<date :date="date"></date>

Generative AI models have many moving parts. This guide provides a survey of the most important openness dimensions by discussing two models both self-billed as "open source". **BloomZ** was introduced by the BigScience Workshop team in May 2023 as an early open source large language model; **Llama 3.1** (Llama for short) was introduced by Facebook Research as “the next generation of our open source large language model”. However, a glance at the openness scores below shows that the models differ quite a lot in terms of overall openness.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: llama-3.1, bloomz
---
::


Hovering over the openness indicators below makes visible the 14 dimensions by which we judge model openness. In this guide, we summarise the dimensions in terms of three areas: availability, documentation and access.

## Availability
When it comes to open _code_, we find that BloomZ makes available source code for training, fine-tuning and running the model, while for Llama none of the model's source code is made available, only scripts for running the model are shared. The _LLM data_ underlying the base model is documented in great detail by BloomZ, while for Llama only the vaguest details are provided in a corporate preprint: “a new mix of data from publicly available sources, which does not include data from Meta's products or services”. The statement is clearly designed to minimise legal exposure. 

Both systems make available _model weights_, though for Llama access is restricted through a consent form. The training data for instruction tuning (RL data) is described and documented by BloomZ as consisting of xP3 (Crosslingual Public Pool of Prompts); for Llama, the corporate preprint notes that fine-tuning was done based on “a large dataset of over 1 million binary comparisons based on humans applying our specified guidelines, which we refer to as Meta reward modeling data”, and which remains undisclosed. (The same preprint mentions that for evaluation, Meta did build on several RLHF datasets openly shared by others.) Model weights for the instruction-tuned version (RL weights) are made openly available by BloomZ, while for Llama they require an access request.

## Documentation
The BloomZ code is not just available, it is also _well-documented_. For Llama on the other hand, no no documentation of source code is available (as the source code itself is not open). _Model architecture_ is described for BloomZ in multiple scientific papers and supported by a github repository of code and recipes on HuggingFace; for Llama, the architecture is described in less detail and scattered across corporate websites and a preprint.

BloomZ's multiple _preprints_ document data curation and fine-tuning in great detail; in contrast, Llama's single preprint offers fewer details and appears strategically vague on crucial details (for instance, training datasets and instruction tuning). The scientific documentation of BloomZ also includes multiple _peer-reviewed papers_, including one of the very few scientifically vetted sources of data on the energy footprint of training large language models. No peer-reviewed papers providing scientific documentation or evaluation of Llama are known currently.

The two systems also differ in terms of the sytematicity of documentation, as measured by the availability of  _model cards_ and _data sheets_: industry-standard models for providing metadata on architecture, training, and evaluation. For Bloom, these system cards provide basic details alongside extensive cross-references to other documentation on training data, training approach, model architecture, fine-tuning and responsible use. In contrast, the Llama model card only provides minimum detail and none whatsoever on training data. A data sheet is only available for BloomZ. This means that for Llama, there is no documentation of training datasets whatsoever — a prime example of a strategy [described](https://arxiv.org/abs/2311.03449) by Birhane et al. as a tactical template of “(non)declaring the training dataset information”.

## Access
Access presents a mixed picture for both of the models. Both are  primarily intended for local deployment, and are additionally available through various application programming interfaces (_APIs_). 

Neither model is fully released under an OSI-approved open source license, but the licensing details are interestingly different. The BloomZ source code is released under Apache 2.0, a maximally open license with a minimum of restrictions. The model weights on the other hand are released under the Responsible AI License ([RAIL](https://www.licenses.ai/)). Llama releases no source code, as we saw above; meanwhile the model weights are released under a bespoke "Meta Community License".

Both licences aim to restrict harmful use cases, but there is a key difference in the constraints they put on representing model outputs. RAIL stipulates that a user may not “generate content without expressly and intelligibly disclaiming that the text is machine-generated”. the Meta Community License for Llama on the other hand stipulates that a user may not “represent that Llama 2 outputs are human-generated”. This is a much lower bar, because it leaves open a wide swathe of use cases where there may not be the explicit claim of human-generated output, but merely a strong implication. 

## In closing
This brief guide offers a walkthrough of the main dimensions of openness. As we see, the open source claim of BloomZ is well-founded. Llama on the other hand really [cannot be called](https://spectrum.ieee.org/open-source-llm-not-open) "open source" under any reasonable definition of the term. It is at best **open weights**, and is closed in almost all other aspects. Llama, in all currently available versions, is a prime example of a model that claims openness benefits by merely providing access to its most inscrutable element: model weights. 

The models can also be [compared side by side](https://www.osai-index.eu/compare?models=bloomz,llama-3.1).

This guide incorporates some text and data from the following paper:

* Liesenfeld, Andreas, and Mark Dingemanse. 2024. ‘Rethinking Open Source Generative AI: Open-Washing and the EU AI Act’. In The 2024 ACM Conference on Fairness, Accountability, and Transparency (FAccT ’24). Rio de Janeiro, Brazil: ACM. doi: [10.1145/3630106.3659005](https://dl.acm.org/doi/10.1145/3630106.3659005)
