---
title: Open-source enables academic liberty
description: (2/5) Part of a series of blog posts on the benefits of open-source AI.
date: 2025-08-14
author: Dick Blankvoort
status: unpublished
---
# On the benefits of open-source AI: open-source enables academic liberty
<author :author="author"></author>

In this second post, we discuss how releasing models in an open-way can benefit academic liberty. We do this by discussing the converse, how (partially) closed models can hurt academic liberty, and subsequently discussing how open-source AI circumvents these flaws.

Back in August of 2021, OpenAI [released its text-to-code model Codex](https://openai.com/index/openai-codex/). Powering GitHub Copilot, this closed-source model saw heavy use in academic circles. [Nearly a hundred papers adopted it for their research](https://www.aisnakeoil.com/p/openais-policies-hinder-reproducible). It came as a shock, then, when in March of 2023 OpenAI announced that it would be discontinuing the Codex model. As a closed-source model, this meant that the model would no longer be able to be used in any capacity, meaning that all the papers based on it would no longer be reproducible. [This highlights the core weakness of relying on closed-source models for one's research](https://www.nature.com/articles/s42256-023-00783-6), as it means that, without proper warning, external parties can sabotage the reproducibility of a researcher's paper in key ways. Clearly, in order to ensure that research is reproducible it is necessary to employ open-source models.

What's more, the AI space _can not_ be fully investigated by only looking at proprietary models. Though it may be tempting to look at only GPT-4 to investigate, for instance, model agreeability, this approach ignores the large variety of LLM techniques and implementations currently out there. The AI space is broad and ever-evolving, and a thorough approach necessitates a broad overview not just based on closed-source APIs, but on open-source local models.

By allowing researchers to maintain their own copies of models for their research, open-source AI provides a critical safeguard for the reproducibility of papers. Though there is some limited role for API-based research on proprietary models, for most research applications open-source models provide an avenue for research which allows for greater academic liberty and a broader utility.