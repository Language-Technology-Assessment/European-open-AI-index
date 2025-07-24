--- 
title: "BERT: The original sin of open-washing large language models"
description: "Already in 2018 Google's pioneering LLM "BERT" was marketed as open source, leading an entire field down a dubious path."
date: 19-12-2024
---

# BERT: The original sin of open-washing large language models


In late 2018, before large language models (LLMs) became mainstream, Google released a large language model bound to shake up the natural language processing (NLP) research community. 
The model dramatically improved the state-of-the-art for many benchmarks in the field, trailblazing the upcoming explosion of interest in LLMs. 
An awe-struck resarch community celebrated what the model could do and marvelled at the new "transformer" machine learning architecture it was build on.
BERT even spawned a new scientific field dedicated to the study of it, [BERTology](https://aclanthology.org/2020.tacl-1.54/). 
Amidst the buzz, few asked what data it was trained on or whether is was really "open source" as [Google claimed](https://research.google/blog/open-sourcing-bert-state-of-the-art-pre-training-for-natural-language-processing/).

Google's BERT continues to shape research in NLP to this day. 
The paper that introduced it became the most cited scientific publication in the field with [over 125.000 citations](https://scholar.google.com). 
A host of popular spin-off models were built on top of the original, providing BERT-based technologies for domains as diverse as Biology (BioBERT), Science (SciBERT), Finance (FinBERT) or Medicine (Med-BERT). 
In short, with the help of BERT, Google shaped the course of an entire scientific discipline for years to come. 
Here's why this still matters today. 

We still don't know exactly how BERT was built. 
Dazzled by it's technological marvels, even the scientists that introduced the field of BERTology that examines what BERT can do, did not ask how it was built. 
[Their work](https://aclanthology.org/2020.tacl-1.54/) doesn't even mention terms such as "training" or "data". 
The authors of BERT stated in their paper that the model was trained on English Wikipedia and a now defunct corpus of English novels called the [book corpus](https://en.wikipedia.org/wiki/BookCorpus). 
Both datasets were already used by Google's "Brain" division in NLP research before the release of BERT and [records of correspondance between journalists and Google](https://www.theguardian.com/books/2016/sep/28/google-swallows-11000-novels-to-improve-ais-conversation#comments) show that critical questions regarding the legitimacy of using the around 10.000 novels that make up the bookcorpus for AI training were brought to Google's attention as early as 2016.
Since BERT was released in 2018, neither Google's [press release](https://research.google/blog/open-sourcing-bert-state-of-the-art-pre-training-for-natural-language-processing/) nor any other official source has clarified data use in the BERT model.

[This practice is a problemtic precedent for Open Source AI because...]

As the first LLM that was highly influential in science despite deliberate nondisclosure of it's training data, **BERT was the original sin of open-washing that lead an entire scientific community down a dubious path**. 
As a publisher, Google actively marketed the model as open-source without providing sufficient information how it was built. 
And as a dazzled audience, the research community failed to call out the adverse effects on a lack of transparency for too long. 
BERT should be remembered both a milestone in the history of NLP as well as the first testament of the adverse effects of overclaiming transparency in the field of generative AI. 
Open-washing in as old as LLMs are.


::the-index
---
hideFilters: true
filters: 
  view: grid
  models: BERT
---
::

Refs:
https://en.wikipedia.org/wiki/BERT_(language_model)
https://en.wikipedia.org/wiki/BookCorpus
https://research.google/blog/open-sourcing-bert-state-of-the-art-pre-training-for-natural-language-processing/
https://huggingface.co/datasets/defunct-datasets/bookcorpusopen
