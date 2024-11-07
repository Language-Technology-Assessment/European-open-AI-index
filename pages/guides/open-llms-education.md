---
title: Best models for education
description: Which open source LLMs afford responsible use in education and teaching?
---

Proprietary generative AI models like ChatGPT are easy to access, but designed in ways that make transparent and responsible use impossible. Widely advertised "open" solutions like Llama are open in weights only, providing no access to training code or to the all-important instruction-tuning data. This guide offers some recommendations for models that can be used in open scholarship and teaching.

::the-index
---
hideFilters: true
filters: 
  models: olmo-7b-instruct, amber, pythia-chat-base-7B
---
::

One of the most important LLM-related skills students need today is _critical AI literacy_. Anyone can follow a 10 minute Youtube tutorial on prompt engineering, or read the latest research papers on jailbreaking ChatGPT, Gemini, or similar proprietary models. But for critical AI literacy, more is needed. It should be possible to inspect the training data of a model; to understand how exactly its fine-tuning makes it appear so docile and helpful; and to test prompts and output in easily accessible ways.

The Venn diagrams of truly open models and models with utility in education overlap to a large degree, but not fully. For instance, a model like BloomZ is admirably open on all fronts, but at 175B parameters it can also be prohibitively heavy to deploy in an educational setting. Three models stand out currently for their high degree of openness, exemplary documentation, and ease of access for demonstration purposes: **OlMO Instruct** by Allen AI, **Amber Chat** by LLM360, and **Pythia Chat** by TogetherComputer. All three are small to mid-range models that nonetheless provide the basic behaviour that users have come to expect from instruction-tuned LLMs.

These 7B models are relatively "small" in terms of parameters, but make up for it in terms of openness and accessibility. Running the largest models typically takes a lot of compute, which is why they tend to be provided only through (paid) APIs. Smaller models are easier to deploy in educational and research settings. The three models featured in this guide stand out in terms of the available documentation and code for doing so, as well as in being relatively light weight and easily deployable locally.

## How to deploy open source LLMs locally
There are countless guides online for running LLMs locally using command line tools. Depending on the educational setting and the level of students, this may be all you need. Since command line users are typically savvy enough to figure out their preferred setup, we won't provide instructions here. All three models highlighted here can be easily run through [ollama](https://github.com/jmorganca/ollama/tree/main?tab=readme-ov-file#ollama) or llama.cpp. 

There are also some solutions for educational settings more geared towards point-and-click interfaces. We can recommend [LM Studio](https://lmstudio.ai/), available for Mac, Linux and Windows, as a quick way to get you started. LM Studio makes downloading models very easy: you can search for model names, pick the version you want, and download it. After downloading, the model becomes locally available.

![Screenshot of LM Studio downloading OlMo](/images/lmstudio-olmo-screenshot.png "LM Studio screenshot")

LM Studio offers tools for a range of users, from novices to developers. For novices, it will be useful to play with some basic settings like temperature and top n sampling, and to test the effect of different system prompts. 
