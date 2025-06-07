---
title: Model Diversification
description: Exploring innovative models closely tied to other models
date: 2025-06-07
author: Dick Blankvoort
status: unpublished
---
# Model Diversification
<author :author="author"></author>
<date :date="date"></date>

<!-- Desired message:
1. We do not record all AI models comprehensively. In particular, we do not record models which do not match certain diversification criteria.
2. This implies that there exists a significant amount of innovation outside of our index as well.
3. These are some notable projects which, despite perhaps not diversifying themselves majorly from other models, are still worthy of a mention.
-->

<!-- Problem statement from the perspective of the index -->
At the European Open Source AI Index, we seek to provide a comprehensive overview of transparency within the open-source AI landscape. A significant challenge in maintaining such an overview is deciding which models to include and which to exclude. A cursory glance into the AI space reveals a wealth of AI models each competing for recognition, and our index can only include so many before growing cluttered.

<!-- Outlining the purpose of the blog -->
In this blog post, we seek to highlight one aspect we consider when deciding what makes a model relevant for inclusion; its perceived level of diversification from other models. By examining this aspect, we seek to highlight some potentially interesting initiatives which might not be captured by our index, as well as provide insight into some more obscure techniques used in AI technologies.

<!-- Body header -->
## Diversification in LLMs
<!-- Cutting the topic up into three concrete categories -->
Let's start with some ground work. There are many reasons why a model might be considered too similar to another model to warrant inclusion, however in this post we will limit ourselves to three categories. A model might be insufficiently innovative to warrant inclusion, it might be an adaption of a different model to a different architecture, or it might be primarily a fine-tune based on a dataset.

<!-- Category 1 -->
### Fine-tunes based on a dataset
<!-- Showcasing examples within the category & why we do not consider them -->
There are quite a few models in our dataset which are not included due to primarily revolving around fine-tuning a model on a dataset. It could be that these models [employ a novel fine-tuning approach](https://huggingface.co/ernie-research/HH-RLHF-Gemma-2B-MA-PPO-Fixed5) or  [show significant innovation in a dataset](https://huggingface.co/OFA-Sys/OccuLLaMA-7B), however in the end the emphasis with them lies not so much on the model but rather on how the model was created.

<!-- Showcase Airoboros & explain how these models benefit the field of OSAI -->
Their lack of inclusion is certainly not to say that these models do not deliver major innovation. For instance, the various [Airoboros](https://huggingface.co/jondurbin/airoboros-110b-3.3) models together represent a significant effort to tune the well-crafted Airoboros dataset, which has been subsequently used in the training of [at least 350 different AI models](https://huggingface.co/models?dataset=dataset:jondurbin/airoboros-3.2).

<!-- Category 2 -->
### Adaptions to different hardware/architectures
<!-- Showcasing examples in the category & why we do not consider them -->
There are a few models we record which are designed to transplant an existing model to a different hardware or architecture. Notable models here are AMD's [models trained on AMD hardware](https://huggingface.co/amd/AMD-OLMo-1B-SFT-DPO), Amazon's [FalconLite](https://huggingface.co/amazon/FalconLite), and Snowflake's [Llama-3.1-SwiftKV](https://huggingface.co/Snowflake/Llama-3.1-SwiftKV-8B-Instruct). While such efforts are certainly commendable, they do not warrant separate entries in the index.

<!-- Explain how these models benefit the field of OSAI-->
In general, these models do represent a good effort towards exploring the benefits of running models in different forms and under different architectures. Exploring different hardware solutions has the potential to disrupt [existing monolopies in the AI hardware space](https://www.bloomberg.com/news/features/2025-03-20/are-ai-monopolies-here-to-stay-nvidia-and-the-future-of-ai-chips), and exploring models within the context of alternative architectures has the opportunity to lead to [great performance improvements](https://huggingface.co/Snowflake/Arctic-LSTM-Speculator-Llama-3.1-8B-Instruct).

<!-- Category 3 -->
### Not enough index-relevant innovation
<!-- Showcasing examples in the category, explain their use cases & why we do not consider them -->
Lastly, there are models which simply do not provide enough index-relevant innovation to qualify for inclusion in our overview. The word _index-relevant_ is key here, as such models may still deliver plenty of innovation in their own right. Notable models in this category are [Flan-T5](https://huggingface.co/google/flan-t5-xxl), which though a strict improvement over T5 does not differentiate itself much from it, [RecurrentGemma](https://huggingface.co/google/recurrentgemma-9b-it), which is an interesting RNN-based alternative to Gemma, and [model merges](https://huggingface.co/blog/mlabonne/merge-models).

<!-- Model merges -->
Model merges are a relatively recent category of LLMs which combine (or 'merge') two existing LLMs together. Though the technique approach is highly interesting and worthy of study, the fact that it has thusfar (as far as we can tell) primarily been applied for [gaming LLM leaderboards](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) means that we generally discount any models created using the technique.

<!-- Placing diversification in a broader context (outside the index) -->
## Other entities dealing with the matter of inclusion
<!-- Highlighting how the model manifests in LLM arenas -->
Any entity seeking to catalogue the AI landscape must decide on which models to include. LLM arenas, for instance, perpetually face the challenge of deciding which models to compare against each other in order to provide a comprehensive overview. Approaches taken in this differ. While indices such as [OpenLM.AI](https://openlm.ai/chatbot-arena/) and [LMArena.AI](https://lmarena.ai/) seek to provide a curated comparison of models and place emphasis on highlighting models by the greatest innovators, projects such as the [Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard#/) (archived since March) attempted to compare every open model submitted.

<!-- Comment on trends and their implications -->
In general, a curated approach focusing mainly on the largest innovations seems to have won out. This has the advantage of producing leaderboards which highlight the most well-known innovations within the AI space, however has the disadvantage that many lesser-known models within the open-source AI space are only highlighted to a lesser extent.

<!-- Rounding off -->
## Conclusion
<!-- Highlighting the takeaway message -->
The true extent of open-source AI will always reach beyond the scope of our index, and so we would encourage readers to explore the space independently whenever possible. A good start here are the models listed in the text. What we offer at the index is merely a showcase of the most relevant models with regards to transparancy, and there is a great deal more innovation to dig into.

<!--
General categories of 'too undiversified':
- ! Regular fine-tunes !
  - CollectiveCognition-v1.1-Mistral-7B
  - DeepScaleR-1.5B-Preview
  - Llama-3.1-8B-Dragonfly-v2
  - Gemma2-9B-IT-Simpo-Infinity-Preference
  - Llama-3.2-1B-Instruct-APIGen-FC-v0.1
  - Mistral-7B-v0.1-Flashback-v2-Instruct
  - Opt-125M-DPO-Full
  - EleutherAI-Pythia-6.9B-Deduped-SFT-TLDR
  - ! Novel fine-tuning approach (subcat) !
    - HH-RLHF-Gemma-2B-MA-PPO-Fixed5
    - GRIN-MoE
  - ! Demonstrates innovation in a dataset (subcat) !
    - Bagel
    - DistilabelBeagle14-7B
    - Distilabeled-Marcoro14-7B-Slerp-Full
    - Distilabeled-OpenHermes-2.5-Mistral-7B
    - OccuLLaMA-7B
- ! Model adaptions to different arch/hardware !
  - FalconLite
  - Llama-3.1-SwiftKV-8B-Instruct
  - AMD-OLMo-1B-SFT-DPO
  - DeepMixtral-8x7B-Instruct
- ! Too minor innovation for sign. inclusion !
  - Flan-T5-XXL
  - RecurrentGemma-9B-IT
  - ! Model merges (subcat) !
- Attempted replications of existing models
  - Alpaca-Chavez
- Safety-tuned/unaligned models
  - AmberChat/AmberSafe
  - R1-1776
  - SpicyBoros-70B-2.2
  - WizardLM-Uncensored-Falcon-7B
- Fine-tuned on different models?
  - GPT4-x-Alpaca
  - Redmond-Hermes-Coder
  - Hermes-RWKV-v5-7B
- Language-tuned models?
  - Arabic-StableLM
  - C4AI-Command-R7B-Arabic-02-2025
  - Japanese-Stable-VLM
  - Llama-2-13B-Chat-Dutch
- Vision models?
  - Aya-Vision
  - BELLE-VL
  - K2-Vision-65B
  - Wings-Qwen1.5-8B
- (Non-)MoE variants?
  - Eurus-70B-NCA
  - Hunyuan-7B-Instruct
  - Airoboros-LMoE
- Different base model?
  - Airoboros-Mistral
  - Airoboros-Jamba
- Different model versions (not discussed)
- Different model sizes (not discussed)
- Quantization/Context length (not discussed)
-->