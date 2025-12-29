---
title: Open-source alleviates reproducibility issues
description: (2/5) Part of a series of blog posts on the benefits of open-source AI.
date: 2025-12-29
author: Dick Blankvoort
status: published
---
# The benefits of open-source AI: open-source alleviates reproducibility issues
<author :author="author"></author>

In this second post about the benefits of open-source AI, we discuss how releasing models in an open way can alleviate reproducibility issues. We do this by discussing the example of Codex, a model whose closed-source nature rendered many studies irreproducibe, and subsequently touch on issues of broader ecological validity and research trends.

### Codex
Back in August of 2021, OpenAI [released its text-to-code model Codex](https://openai.com/index/openai-codex/). Powering GitHub Copilot, this closed-source model saw heavy use in academic circles. [Nearly a hundred papers adopted it for their research](https://www.aisnakeoil.com/p/openais-policies-hinder-reproducible). It came as a shock, then, when in March of 2023 OpenAI announced that it would be discontinuing the Codex model. As a closed-source model, this meant that the model would no longer be able to be used by any researchers, resulting in sudden loss of reproducibility of all papers based on it. This highlights the core weakness of relying on closed-source models for one's research, as it means that, without proper warning, external parties can sabotage the reproducibility of a researcher's paper in key ways. Clearly, therefore, in order to ensure that research is reproducible [it is necessary to employ strictly open-source models wherever possible](https://www.nature.com/articles/s42256-023-00783-6).

### Current research trends
Current research trends see a drastic increase in the popularity of using (LLMs-as-judges)[https://arxiv.org/abs/2412.05579]. Along with [other obvious weaknesses inherent to such an approach](https://arxiv.org/abs/2410.20266), many researchers choose to use closed-source models for their evaluations in this work, often incorporating multiple different closed-source LLMs. This renders such research uniquely vulnerable to the reproducibility issues mentioned above. Whenever one of the closed models used in evaluation is deprecated, as most recently exemplified by [Claude Opus 3](https://platform.claude.com/docs/en/about-claude/model-deprecations), there is a necessary clamor to keep such models around in order to preserve reproducibility of research, something which is inherently against the business interests of model creators. 

### Ecological validity of a proprietary-only approach
Regarding the generalizability of one's research, it is worth noting that the AI space _cannot_ be globally investigated by only looking at proprietary models. Though it may be tempting to look at only GPT-5.2 to investigate, for instance, model agreeability, this approach ignores the large variety of LLM techniques and implementations used by model creators. The AI space is broad and ever-evolving, and a thorough, ecologically valid approach necessitates a broad overview not just based on closed-source APIs, but also on open-source local models.

### Conclusion
By allowing researchers to maintain their own copies of models for their research, open-source AI provides a critical safeguard for the reproducibility of papers. Though there is some limited role for API-based research on proprietary models, for most research applications open-source models provide an avenue for research which allows for greater academic liberty and a broader utility.
