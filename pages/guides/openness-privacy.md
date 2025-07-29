---
title: Open-source affords privacy
description: (3/5) Part of a series of blog posts on the benefits of open-source AI.
date: 2025-07-16
author: Dick Blankvoort
status: unpublished
---
# On the benefits of open-source AI: open-source affords user privacy
<author :author="author"></author>

## Introduction
In this third post about the benefits of open-source models, we discuss how designing models with open-source in mind benefits the privacy of end users. We investigate privacy concerns with current AI models, and dig into the communities within FOSS which hold privacy to the highest regard.

## How open-source AI safeguards privacy
The most obvious way in which open-source AI safeguards privacy is through allowing users to create local copies. By running models locally, users can ensure that models do not pass on information about their conversations to third parties, and it allows them to fully customize their conversation flows. Critically, this means that users can pass sensitive information to the models, both in conversations and in model contexts, without risk of that sensitive information being recorded elsewhere.

## Privacy concerns in current AI models
For the converse, proprietary models can offer no easy verifiable guarantee that data stays private between users and the model. What's worse, most private entities seem happy to gobble up as much chat information as they can, as it allows them to design more capable instruction-tuned models. [ChatGPT is even mandated to maintain all conversations indefinitely](https://www.geeky-gadgets.com/chatgpt-privacy-risks-explained/). Some end users seem happy to [share even the most sensitive sensitive data with these models](https://tech.co/news/samsung-restricts-generative-ai-use). But from a data privacy perspective, the practices of proprietary model owners can best be described as nightmarish.

For tips on how end users can interact with proprietary models in way which preserves privacy as much as possible, see [this post from Privacy Not Included](https://www.mozillafoundation.org/en/privacynotincluded/articles/how-to-protect-your-privacy-from-chatgpt-and-other-ai-chatbots/).

## The FOSS community and privacy as an inalienable right
The concept of open-source arises from the FOSS community, where privacy is held as a fundamental and inalienable right of users. This has led to many open-source AI initiatives which seek to safeguard user privacy in fundamental ways. [Various](https://github.com/nomic-ai/gpt4all) [projects](https://venice.ai/) exist which seek to provide users with a privacy-first LLM interaction experience, and when data is shared it is usually done [with user consent in mind](https://huggingface.co/datasets/allenai/WildChat-1M). In this way, the FOSS community sets a great example for how privacy-preserving AI should be done.

## Conclusion
Open-source models offer users privacy in a way which closed-source models often cannot and fundamentally _will not_ do. As such the privacy-conscious user benefits greatly from open-source initiatives. The FOSS model-developing community represents a great example of how to do privacy-conscious model implementation well, and its projects provide a blueprint for doing privacy-conscious open-source well.