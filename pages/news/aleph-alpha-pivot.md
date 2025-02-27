--- 
title: "Luminous: the language model that wasn't"
description: In which we trace the silent demise of a hyped German large language model
author: Mark Dingemanse
date: 2025-02-17
status: published
---
# Luminous: the language model that wasn't
<author :author="author"></author>

At the European Open Source AI Index we take an interest in large language models that bill themselves as open, so we perked up when German AI company Aleph Alpha [described itself](https://aleph-alpha.com/aleph-alpha-raises-a-total-investment-of-more-than-half-a-billion-us-dollars-from-a-consortium-of-industry-leaders-and-new-investors/), in a VC funding round, as "committed to reproducibility, excellence and sharing innovation through open source."

The Aleph Alpha website long advertised a language model called "Luminous". We had contemplated adding this model to our own index, but had not been able to locate it! The company website did offer quite some [documentation](https://docs.aleph-alpha.com/docs/Deprecated%20Luminous/Deprecated-Luminous/Deprecated-Luminous/) but finding the model itself was proving quite elusive.

Based, presumably, on this same documentation, Stanford FMTI _did_ include Aleph-Alpha's Luminous model, and in fact listed it near the top of its index, where it stayed at least until May 2024:

![FMTI scores showing Aleph Alpha's Luminous model at third place](/images/fmti-total-scores-may2024.png "FMTI Scores May 2024")

Aleph-Alpha managed to collect half a billion of VC funding in 2023, and the company was much hyped in Europe, where it leaned into a reputation as a home-grown alternative to ChatGPT along the same lines as French-made Mistral. [Positioning itself](https://aleph-alpha.com/aleph-alpha-raises-a-total-investment-of-more-than-half-a-billion-us-dollars-from-a-consortium-of-industry-leaders-and-new-investors/) as a key player in "global AI race", it certainly profited handsomely from the hype and general nervousness of markets surrounding AI offerings.

But in September 2024, Aleph-Alpha announced a major pivot away from creating their own models. As founder Jonas Andrulis [told Bloomberg](https://archive.ph/fbUK2), 

> “The world changed. Just having an European LLM is not sufficient as a business model. It doesn’t justify the investment.”

The model details for Luminous are now shown as "deprecated". In the absence of any demos or documentation, we're left wondering whether Luminous was ever a functioning LLM at all. It was certainly not a transparent one. One possibility is that it was built on top of some other provider's white-label LLM service. 

Recently, a new Aleph-Alpha model dubbed [Pharia LLM](https://huggingface.co/Aleph-Alpha/Pharia-1-LLM-7B-control/blob/main/README.md) has made an appearance. It appears this model is an outcome of Aleph-Alpha's [partnership](https://aleph-alpha.com/aleph-alpha-and-silo-ai-enter-a-strategic-partnership-to-advance-open-source-ai-and-enterprise-grade-solutions-in-europe/) with Silo AI, a private AI lab "building market leading open source LLMs". We'll be keeping our eyes peeled for new developments.
