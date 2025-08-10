---
title: Open-source enables oversight
description: (1/5) Part of a series of blog posts on the benefits of open-source AI.
date: 2025-08-14
author: Dick Blankvoort
status: unpublished
---
# On the benefits of open-source AI: open-source enables oversight
<author :author="author"></author>

In this first of a series of blog posts on the benefits of open-source AI, we explore how open-source AI enables greater oversight. We discuss key principles which allow open-source to enable greater oversight, the theoretical motivations behind the EU AI Act treating open-source models with lesser scrutiny, and lastly explore how releasing models in an open-source way makes it easier for watchdogs to investigate legal violations in a model's training.

### How OSAI enables oversight: base principles
**Open-source AI requires open data.** This means that any model seeking to describe itself as open must publish the data on which it is trained. The benefits for oversight are obvious, as it [allows for inspecting exactly on which material a model was trained and for ensuring that no copyright violations are associated with the training procedure](https://arxiv.org/abs/2311.03449).

**Open-source AI requires open training code.** This means that any model which describes itself as open-source, must publish its training code in such a way that the approach used to train the model can be fully reproduced. Thanks to this, it then becomes possible to double-check that no adverse procedures were involved in the training of the model, and the model is neither trained [with censorship in mind](https://acrlog.org/2025/07/21/we-couldnt-generate-an-answer-for-your-question/) nor [by stealing a proprietary model's code or data](https://techstartups.com/2025/02/03/did-openai-steal-deepseeks-code-o3-mini-reasoning-in-chinese-sparks-ai-theft-controversy-over-alleged-copy-and-paste/).

**Open-source AI requires clear documentation.** Lastly, open-source AI models must be published in such a way that both its data and training code are clearly documented. This prevents the mechanics behind a model's creation becoming [difficult to interpret based on a lack of good documentation](https://www.sciencedirect.com/science/article/abs/pii/S0164121225001207), and enables more straightforward oversight.

### The EU AI Act
The benefits of publishing a model as open-source under the EU AI act are often overplayed. It still requires model creators to disclose model architecture, weights, and training procedures. However, the act does allow [some lesser degree of scrutiny for models published under a free and open-source license](https://www.jdsupra.com/legalnews/the-eu-ai-act-open-source-exceptions-9085314/) by waiving the duty to maintain up-to-date technical information about the model. While it is difficult to speculate on the motivations behind this, one possible reason for treating open-source models in this manner is to incentivize model creators to publish models in the public sphere. Another reason is that models published under a free and open-license are by definition open to adoption by outside parties who, through adapting the model, will likely be able to exercise their own kind of scrutiny.

### Open-source enables insight: a practical example
Perhaps the most famous example of open-source status enabling greater oversight in the AI field is that of [LAION-5B](https://arxiv.org/abs/2210.08402). This dataset marketed itself as a large-scale fully-open image dataset for creating image diffusion models, which [enabled](https://github.com/CompVis/stable-diffusion) [widespread](https://arxiv.org/abs/2409.11340) [adoption](https://github.com/superhero-7/AltDiffusion) by model creators. The inherent openness of this dataset also enabled greater scrutiny, with the paper [Into the LAION's Den](https://arxiv.org/abs/2311.03449) pointing out many issues with the data contained in the set. In this way, the open-source status of LAION enabled the auditing of the pretraining data of major model creators.

### Conclusion
By publishing models in a more open manner, model creators enable greater oversight. Openness allows for a closer investigation of a model's inner workings, catching legal issues with the way a model is constructed and allowing model creators to be held to higher standards of accountability. This allows for more ethical AI for all.
