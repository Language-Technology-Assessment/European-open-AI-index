---
title: LLM Diversification
description: Exploring innovative models closely tied to other models
date: 2025-05-26
author: Dick Blankvoort
status: unpublished
---
# LLM Diversification
<author :author="author"></author>
<date :date="date"></date>

<!-- Desired message:
1. We do not record all AI models comprehensively. In particular, we do not record models which do not match certain diversification criteria.
2. This implies that there exists a significant amount of innovation outside of our index as well.
3. These are some notable projects which, despite perhaps not diversifying themselves majorly from other models, are still worthy of a mention. 
4. <Some minor information about model merges, how they make things challenging>
-->

<!-- Problem statement filtered through the index -->
At the European Open Source AI Index, we seek to provide a comprehensive overview of transparancy within the open-source AI landscape. A significant challenge in designing such an overview is deciding what models to include. While this might seem a trivial endeavor at first, a cursory glance into the AI space reveals a wealth of AI models each competing for recognition. Deciding which models to include in an overview thus involves a process of highly targeted curation, with the goal of being as comprehensive as possible while not flooding the overview with a great quantity of irrelevant models.

<!-- Outlining the purpose of the blog -->
In this blog post, we seek to highlight one aspect of deciding what makes a model worthy of inclusion; its perceived level of diversification. Through this, we also seek to highlight some potentially interesting initiatives which might not be captured by our index, as well as provide insight into some more obscure techniques used in LLMs.

<!-- Body header -->
## Diversification in LLMs
<!-- Cutting the topic up into three concrete categories -->
Let's start with some ground work. In general we distinguish a few types of models which do not diversify themselves enough for inclusion. In this post, we distinguish three primary categories; insufficiently innovative models, architecture adaptions, and fine-tunes based on a dataset.

<!-- Category 1 -->
### Fine-tunes based on a dataset
<!-- Showcasing examples within the category -->
There are quite a few models in our dataset which are not included primarily due to being based on fine-tuning on a dataset. It could be that they achieve [a relatively narrow end by fine-tuning](https://huggingface.co/teknium/CollectiveCognition-v1.1-Mistral-7B), [employ a novel fine-tuning approach](https://huggingface.co/ernie-research/HH-RLHF-Gemma-2B-MA-PPO-Fixed5), or [that they are primarily designed to show innovation in a dataset](https://huggingface.co/OFA-Sys/OccuLLaMA-7B). For whatever reason, the models do not diversify themselves enough to warrant separate entries.

<!-- Why they are significant regardless, and why we nonetheless do not include them -->
This is not to say that these models do not deliver major innovation, as many of them do so. For instance, [DeepScaleR](https://huggingface.co/agentica-org/DeepScaleR-1.5B-Preview) achieves significant performance gain in long contexts over its base model [DeepSeek-R1-Distilled-Qwen-1.5B](https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B), claiming comparable performance to GPT-o1 with a mere 1.5B parameters. Additionally, the various [Airoboros](https://huggingface.co/jondurbin/airoboros-110b-3.3) models together represent a significant effort to tune the Airoboros dataset. The only thing given is that, when considering these models, their emphasis lies more on the approach taken with fine-tuning than on the model inherently.

<!-- Category 2 -->
### Adaptions to different hardware/architectures
<!-- Showcasing examples in the category & why we do not consider them -->
There are a few models we record which are designed to transplant an existing model to a different hardware or architecture. While such efforts are certainly commendable, they do not warrant separate entries in the index. Notable models here are [AMD's models designed for different hardware](https://huggingface.co/amd/AMD-OLMo-1B-SFT-DPO), Amazon's [FalconLite](https://huggingface.co/amazon/FalconLite), and [DeepMixtral](https://huggingface.co/cognitivecomputations/DeepMixtral-8x7b-Instruct). In general, these models represent a good effort towards exploring the benefits of running models in different forms.

<!-- Category 3 -->
### Not enough _index-relevant_ innovation
<!-- Showcasing examples in the category & why we do not consider them -->
Lastly, there are models which simply do not provide enough _index-relevant innovation_ to qualify for inclusion in our index. The word _index-relevant_ is key here, as such models may still deliver plenty of innovation in their own rights. Notable models in this category are [Flan-T5](https://huggingface.co/google/flan-t5-xxl), which though a strict improvement over T5 does not differentiate itself much from it, [RecurrentGemma](https://huggingface.co/google/recurrentgemma-9b-it), which is an interesting RNN-based alternative to Gemma, and model merges.

<!-- Model merges -->
Model merges are a relatively novel category of LLMs which combine (or 'merge') two existing LLMs together. Though the technique approach is highly interesting and worthy of study, the fact that it has thusfar (as far as we can tell) primarily been applied for [gaming LLM leaderboards](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) means that we generally discount any models created using the technique.

<!-- Placing diversification in a broader context (outside the index) -->
## Other entities dealing with the matter of inclusion
<!-- Highlighting how the model manifests in LLM arenas -->
Any entity seeking to catalogue the AI landscape must decide on which models to include. LLM arenas, for instance, perpetually face the challenge of deciding which models to compare against each other. Approaches taken in this can differ greatly. While indices such as [OpenLM.AI](https://openlm.ai/chatbot-arena/) and [LMArena.AI](https://lmarena.ai/) seek to provide a curated comparison of models and place emphasis on highlighting models by the greatest innovators, projects such as the [Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard#/) (archived since March) attempt to compare many different open models. In general, a curated approach focusing mainly on the largest innovations seems to have won out. This has the advantage of producing leaderboards which highlight the most well-known innovations within the AI space, however has the disadvantage that many lesser-known models within the open-source AI space are only highlighted to a lesser extent.

<!-- Rounding off -->
## Conclusion
<!-- Highlighting the takeaway message -->
The true extent of open-source AI will always reach beyond the scope of our index (and, in fact most indices seeking to provide an overview of the AI field), and so we would encourage readers to explore the space independently whenever possible. A good start here are the models listed in the text. What we offer at the index is merely a showcase of the most interesting and pertinent models, and there is a great deal more innovation to dig into.

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