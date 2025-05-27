--- 
title: Introducing Performance Classes in the OS AI Index
description: "How we classify models under 3 performance classes: Limited, Full and Latest"
author: Nityaa Kalra
date: 2025-04-03
status: published
---

# Introducing Performance Classes in the OSAI Index
<author :author="author"></author>

Evaluating the performance of LLMs has never been straightforward. With every new model release, benchmarks shift, leaderboards get updated, and comparisons become increasingly complex.

Raw benchmark scores do not always reflect real-world usability. This is why we are introducing **Performance Classes**- a way to categorize models based on broad performance tiers, helping users quickly navigate the landscape without getting lost in ever-changing rankings.

## The Three Performance Classes

We have grouped models into three broad performance tiers. These categories help distinguish between cutting-edge models, well-rounded general-purpose models, and specialized or legacy models.

* **Latest:** A small, curated set of top-performing models based on consulting a range of popular benchmarks. This class represents state-of-the-art models but will be updated periodically as newer, stronger models emerge.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: deepseek-v3
---
::

* **Full:** Models that don’t necessarily lead in benchmarks but still offer strong, general-purpose performance. These models strike a balance between capability and practicality.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: OLMo
---
::

* **Limited:** Small, purpose-built models designed for niche tasks, as well as older models like BERT that have been surpassed by modern architectures.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: pharia
---
::


## Why Performance Classes?

Performance isn’t a single, absolute measure. A model’s real-world impact also depends on factors like accessibility, efficiency, and task suitability. Performance Classes offer a straightforward way to assess model capabilities without relying solely on fluctuating benchmark scores.

While Performance Classes serve as an additional feature to help users navigate the diverse landscape of models, our core focus remains on openness. As the field evolves, we’ll continue refining these categories to ensure they remain useful and relevant. We hope this framework makes it easier to navigate the LLM landscape while keeping openness as the guiding principle of our evaluations.



