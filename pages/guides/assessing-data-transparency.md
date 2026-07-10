---
title: Assessing data transparency
description: Challenges in determining data openness for models openness
date: 2026-05-19
author: Dick Blankvoort
status: published
---
# Assessing data transparency
<author :author="author"></author>
<date :date="date"></date>

Intuitively, "data openness" seems like a binary: a model either discloses its training data or it does not. In reality, several factors complicate this assumption.
First, as reflected in our database, pretraining data and fine-tuning data are distinct. Pretraining relies on massive web scrapes to build latent conceptual representations, while fine-tuning shapes the model into a specific role (e.g., a helpful assistant). Often, a model's fine-tuning data is public while its base data remains proprietary. Because of this, we evaluate these sources separately.

Second, true openness requires transparency across the entire fine-tuning chain. If a model is built atop an already fine-tuned model, all sequential datasets must be disclosed. While this seems obvious, models frequently claim full openness while obscuring crucial parts of their fine-tuning lineage, leading to misleading claims.
Third, data can be disclosed at different levels, each serving different stakeholder needs. We distinguish four:

- Data sources list: Primarily useful for rights assessment.
- Exact data mixture: Primarily useful for theoretical evaluation.
- Filtering methodology: Primarily useful for replication.
- The full dataset: Primarily useful for open-source development.

Ideally, all four would be provided, but this is rare in practice. Our index considers disclosure through any of these vectors as satisfactory, which means an "open-data" model might still lack the specific details a given stakeholder requires.

Fourth, true transparency requires examining data provenance, not just surface-level disclosures. Even if a final dataset is open, a lack of information on how that data was collected limits reproducibility and rights assessment. For example, many AI models train on openly licensed datasets that still contain copyrighted material. A rigorous assessment cannot simply take a dataset’s licensing claims at face value.

Ultimately, classifying data openness depends heavily on the specific data types required, the fine-tuning lineage, the end user's goals, and the granular data landscape. While our index provides a methodologically grounded assessment, anyone relying on "open-data" models should independently verify whether a model's data is truly open enough for their specific use case.
