---
title: Assessing data transparency
description: Why determining data openness for models as a non-expert is challenging
date: 2026-05-19
author: Dick Blankvoort
status: draft
---
# Assessing data transparency
<author :author="author"></author>
<date :date="date"></date>

- 'Data openness' as a concept intuitively seems like it should be a binary. A model either shows on which data it was trained, or it does not. There are a few factors which complicate this process, however.

- First, and as we already model in our database, there is a difference between the pretraining data of a model and the fine-tuning data of a model. While the former involves large amounts of data scraped from the internet and generally focuses on instilling a latent representation of concepts, the latter focuses on, for instance, tuning this model such that it outputs text in the form of a helpful assistant. When assessing data openness, it is common to discover that the base model data for a model is not disclosed while the fine-tuning data is. As such we choose to account for these sources separately.

- Second, any accounting of data openness should take into account data openness for every model in the fine-tuning chain. That is, if a model is fine-tuned further from an already fine-tuned model, both sets of fine-tuning data should be accounted for. Though this might seem obvious, it is far from unusual for models to claim openness while key aspects of their fine-tuning are obscured due to facts such as this, and for such wrongful claims about openness to subsequently be taken up.

- Third, there are different levels to which data can be disclosed, each of which is useful to different stakeholders. We distinguish:
  1. Disclosing a list of data sources used, which is primarily useful for rights assessment.
  2. Disclosing the exact mixture of data which went into the dataset, which is primarily useful for theoretical assessments.
  3. Disclosing an exact description of how data from input data sources was filtered to produce the final dataset, which is primarily useful for replication.
  4. Disclosing the dataset itself, which is primarily useful for further open-source development.
- While in the ideal case data would be disclosed in all of these ways, in practice this rarely happens. In our index we deem it satisfactory if data is disclosed through any of these four vectors, which means that some 'open-data' models may nonetheless be unsatisfactory for specific stakeholders.

- Fourth, tracking full data openness might necessitate tracking more than just surface-level data disclosures. In particular, in order to make sure that data is handled in a transparent manner, data provenance has to be considered to a certain extent. If a model's final training data is open however either it or its source data sets have no information about *how data is collected*, this might limit reproducibility and rights assessment in meaningful ways. Many modern AI models are, for instance, trained on copyrighted data located within openly-licensed datasets, which means that a proper investigation into the data on which a model was trained must not take the final dataset at its word with regards to data claims.