---
title: Open-source enables academic liberty
description: (2/5) Part of a series of blog posts on the benefits of open-source AI.
date: 2025-07-16
author: Dick Blankvoort
status: unpublished
---
# On the benefits of open-source AI: open-source enables academic liberty
<author :author="author"></author>

## Introduction
In this second post, we discuss how releasing models in an open-way can benefit academic liberty. We do this by discussing the converse, how (partially) closed models can hurt academic liberty, and subsequently discussing how open-source AI circumvents these flaws.

## Practical example: OpenAI's Codex
Back in August of 2021, OpenAI [released its text-to-code model Codex](https://openai.com/index/openai-codex/). Powering GitHub Copilot, this closed-source model saw heavy use in academic circles. [Nearly a hundred papers adopted it for their research.](https://www.aisnakeoil.com/p/openais-policies-hinder-reproducible). It came as a shock, then, when in March of 2023 OpenAI announced that it would be discontinuing the model. As a closed-source model, this meant that the model would no longer be able to be used in any capacity, meaning that all the papers based on it would no longer be reproducible. [This highlights the weaknessess of relying on closed-source models as the core of one's research](https://www.nature.com/articles/s42256-023-00783-6), as it means that, without proper warning, external parties can sabotage the reproducibility of a researcher's paper in key ways.
<!-- TODO very matter-of-fact. Improve flow. -->

## (The dangers of proprietary LLMs more generally)
The AI space cannot be investigated fully by only looking at proprietary models. Though it may be tempting to look at only GPT-4 to investigate, for instance, model agreeability, this ignores the large variety of LLM techniques and implementations currently out there. The AI space is broad and ever-evolving, and a thorough approach necessitates a broad overview not just based on APIs. ...

## How open models resolve this
Open-source models require being able to keep and distribute a local copy at all times. This enables academics to distribute their own copies of the models used in their research, ensuring reproducibility is maintained.

## Conclusion
By allowing researchers to maintain their own copies of models for their research, open-source AI provides a critical safeguard for the reproducibility of papers. Though there is some limited role for API-based research on proprietary models, for most research applications open-source models provide an avenue for research with greater academic liberty.