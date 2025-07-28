--- 
title: "BERT: The original sin of open-washing large language models"
description: "Already in 2018 Google's pioneering LLM 'BERT' was marketed as open source, leading an entire field down a dubious path."
date: 2024-12-19
---

# BERT: The original sin of open-washing large language models


In late 2018, before large language models (LLMs) became mainstream, Google released a large language model bound to shake up the natural language processing (NLP) research community. 
The model dramatically improved the state-of-the-art for many benchmarks in the field, trailblazing the upcoming explosion of interest in LLMs. 
An awe-struck resarch community celebrated what the model could do and marvelled at the new "transformer" machine learning architecture it was build on.
BERT even spawned a new scientific field dedicated to the study of it, [BERTology](https://aclanthology.org/2020.tacl-1.54/). 
Amidst the buzz, few asked what data it was trained on or whether is was really "open source" as [Google claimed](https://research.google/blog/open-sourcing-bert-state-of-the-art-pre-training-for-natural-language-processing/).

Google's BERT continues to shape research in NLP to this day. 
The paper that introduced it became the most cited scientific publication in the field with [over 125.000 citations](https://aclanthology.org/N19-1423/). 
A host of popular spin-off models were built on top of the original, providing BERT-based technologies for domains as diverse as Biology (BioBERT), Science (SciBERT), Finance (FinBERT) or Medicine (Med-BERT). 
In short, with the help of BERT, Google shaped the course of an entire scientific discipline for years to come. 
Here's why this still matters today. 

We still don't know exactly how "open source" BERT was built. 
Dazzled by it's technological marvels, even the scientists that introduced the field of BERTology that examines what BERT can do did not ask how it was built. 
[Their work](https://aclanthology.org/2020.tacl-1.54/) doesn't mention terms such as "training" or "data". 
The authors of BERT themselves vaguely stated in their paper that the model was trained on English Wikipedia and a now defunct corpus of English novels called the [book corpus](https://en.wikipedia.org/wiki/BookCorpus). 
Even before the release of BERT, these datasets were in use by Google's "Brain" division for research purposes. But the use of the book corpus, a collection of self-published books, for AI training violated the publisher's Terms of Service and [records of correspondance between journalists and Google](https://www.theguardian.com/books/2016/sep/28/google-swallows-11000-novels-to-improve-ais-conversation#comments) show that critical questions regarding the legitimacy of using this data were brought to Google's attention as early as 2016.
Since BERT was released in 2018, neither Google's [press release](https://research.google/blog/open-sourcing-bert-state-of-the-art-pre-training-for-natural-language-processing/) nor any other official source has clarified what data was used in the BERT model.

The field of open source AI still suffers from a lack of transparency when it comes to sharing training data and since 2018 many other genAI heavyweights have followed Google's lead of obfuscating open weight and open source. As the first LLM that was highly influential in science despite deliberate nondisclosure of it's training data, **BERT was the original sin of open-washing that lead an entire scientific community down a dubious path**. 
And the dazzled NLP research community failed to call the adverse effects of this practice on science out. 
BERT should be remembered both as a milestone in the history of NLP as well as the first testament of adverse effects of overclaiming transparency in the field of generative AI. 
Open-washing in as old as LLMs are.


::the-index
---
hideFilters: true
filters: 
  view: grid
  models: BERT
---
::
