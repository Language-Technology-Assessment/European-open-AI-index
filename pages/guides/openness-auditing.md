---
title: "The benefits of open-source AI: open-source enables oversight"
description: (1/5) Part of a series of blog posts on the benefits of open-source AI.
date: 2025-12-29
author: Dick Blankvoort
status: published
---

In this first of a series of blog posts on the benefits of open-source AI, we discuss key principles which allow open-source to enable greater oversight. We subsequently discuss the theoretical motivations behind the EU AI Act treating open-source models with lesser scrutiny, and lastly explore how releasing models in an open-source way makes it easier for watchdogs to investigate legal violations in a model's training.

### How open-source AI enables oversight: base principles
**Open-source AI requires open data.** This means that any model seeking to describe itself as open must publish the data on which it is trained. This is crucial for oversight, as it [allows for inspecting exactly on which material a model was trained and for ensuring that no copyright violations are associated with the training procedure](https://arxiv.org/abs/2311.03449).

**Open-source AI requires open training code.** By publishing code in a clearly-readable manner, it becomes possible to double-check that the model is neither trained [with censorship in mind](https://acrlog.org/2025/07/21/we-couldnt-generate-an-answer-for-your-question/) nor [by stealing a proprietary model's code or data](https://techstartups.com/2025/02/03/did-openai-steal-deepseeks-code-o3-mini-reasoning-in-chinese-sparks-ai-theft-controversy-over-alleged-copy-and-paste/).

**Open-source AI requires clear documentation.** Lastly, open-source AI models must be published in such a way that both its data and training code are clearly documented. This prevents the mechanics behind a model's creation becoming [difficult to interpret based on a lack of good documentation](https://www.sciencedirect.com/science/article/abs/pii/S0164121225001207), and enables more straightforward oversight.

### The EU AI Act
It is often thought that the EU AI act contains a specific exception for open-source models. In reality, this is not the case. Though the act does allow [some lesser degree of scrutiny for models published under a free and open-source license](https://www.jdsupra.com/legalnews/the-eu-ai-act-open-source-exceptions-9085314/) by waiving the duty to maintain up-to-date technical information about the model, it still requires model creators to disclose model architecture, weights, and training procedures. One possible reason for treating open-source models in this manner is that models published under a free and open-license are by definition open to adoption by outside parties. These authors, through adapting the model, will likely be able to exercise their own kind of scrutiny. Another reason would be to incentivize model creators to publish models in the public sphere. 

### Open-source enables insight: a practical example
A famous example of open-source status enabling greater oversight in the AI field is that of [LAION-5B](https://arxiv.org/abs/2210.08402). This dataset marketed itself as a large-scale fully-open image dataset for creating image diffusion models, [enabling](https://github.com/CompVis/stable-diffusion) [widespread](https://arxiv.org/abs/2409.11340) [adoption](https://github.com/superhero-7/AltDiffusion) by model creators. The inherent openness of this dataset also enabled greater scrutiny. The open-source status of LAION enabled not only widespread adoption but [also the auditing of the pretraining data of a large number of major image models](https://arxiv.org/abs/2311.03449).

### Conclusion
By publishing models in a more open manner, model creators enable greater oversight. Openness allows for a closer investigation of a model's inner workings, catching legal issues with the way a model is constructed and allowing model creators to be held to higher standards of accountability. This allows for more ethical AI for all.
