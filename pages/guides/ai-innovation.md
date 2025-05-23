---
title: Innovation in LLMs
description: What counts as 'significant innovation' in LLMs?
date: 2025-05-23
author: Dick Blankvoort
status: unpublished
---
# Innovation in LLMs
<author :author="author"></author>

At the Open Source AI Index, we seek to provide a comprehensive overview of open-source transparancy regarding the AI landscape. A significant challenge involved with designing an index for this is deciding what models to include. Aside from the question of _what should even count as an open-source model_ for the purposes of inclusion, this proces involves deciding which models represent significant enough advancements to warrant a separate entry. Though this might seem a trivial endeavor if one only looks at the open source AI releases from the major tech companies, digging below the surface reveals a wealth of AI models each competing for recognition. Deciding which models to include in a broad overview of AI involves a process of highly targeted curation, with the target of being as comprehensive as possible while not flooding the overview with a great quantity of similar or irrelevant models. In this blog post, we seek to highlight one aspect of deciding what counts as a model worthy of inclusion; its level of innovation. Through this, we seek to highlight some potentially interesting initiatives which might not be captured by our index and provide insight into the various techniques used in LLMs.

## Model inclusion considerations
At the OSAI index, we maintain a backend list of over 2400 models and model versions which might qualify for inclusion. Non-included entities range from [models which do not make explicit claims to open-source](https://huggingface.co/replit/replit-code-v1_5-3b), to [models which lack wide-spread adoption](https://huggingface.co/SebastianSchramm/Cerebras-GPT-111M-instruction-sft-lora-merged-dpo-lora), to [models which no longer represent a significant advance in the space](https://huggingface.co/NousResearch/Nous-Puffin-70B), [to models with a too niche application](https://huggingface.co/nvidia/OpenMath2-Llama3.1-70B), to [models which do not diversify themselves enough from other models to warrant inclusion](https://huggingface.co/nvidia/Llama-3.1-Minitron-4B-Width-Base). It is this last category which will be the primary topic of our blog post today.

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
- ! Model merges !
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

## Other entities dealing with the matter of inclusion
Any entity seeking to catalogue the AI landscape must decide on which models to include. LLM arenas, for instance, perpetually face the challenge of deciding which models to compare against each other. Approaches taken in this can differ greatly. While indices such as [OpenLM.AI](https://openlm.ai/chatbot-arena/) and [LMArena.AI](https://lmarena.ai/) seek to provide a curated comparison of models and place emphasis on highlighting models by the greatest innovators, projects such as the [Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard#/) (archived since March) attempt to compare many different open models. In general, a curated approach focusing mainly on the largest innovations seems to have won out. This has the advantage of producing leaderboards which highlight the most well-known innovations within the AI space, however has the disadvantage that many lesser-known models within the open-source AI space are only highlighted to a lesser extent.

## Conclusion
The true extent of the open-source AI space will always reach beyond the scope of our index (and, in fact most indices seeking to provide an overview of the AI field), and so we would encourage readers to explore the space independently whenever possible. What we offer at the index is merely a showcase of the most interesting and pertinent models, and there is a great deal more innovation to dig into.