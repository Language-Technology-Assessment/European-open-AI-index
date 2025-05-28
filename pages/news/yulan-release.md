---
title: YuLan-Mini - A new highly open model
description: Gaoling School of Artificial Intelligence releases a new highly open AI model
date: 2025-05-28
author: The EU OSAI index team
status: published
---
# YuLan-Mini - A new highly open model
<date :date="date"></date>

At the European Open Source AI Index, we welcome any efforts to promote openness in the AI space. Most new models we add end up somewhere midway the index, often because they build on widespread models like Llama or Mistral that are not themselves very open to start with. Much to our delight, [there is a genuinely new model in town](https://osai-index.eu/model/YuLan) that has overtaken good old BLOOMZ for the second-place spot.

YuLan-Mini is a new model by the Gaoling School of Artificial Intelligence. Claiming particularly good performance in math and code, the model is fully open according to nearly all of our [openness measures](https://dl.acm.org/doi/10.1145/3630106.3659005). The model creators publish the data used to train their base model on [HuggingFace](https://huggingface.co/datasets/yulan-team/YuLan-Mini-Datasets), providing thorough information on the data mixture in an [accompanying table](https://docs.google.com/spreadsheets/d/1YP8-loVUxgxo36UEpOwflR3GRHLieBnLlCy8g10g8RU/edit?gid=0#gid=0). The model weights themselves are published under an [open MIT license](https://huggingface.co/yulan-team/YuLan-Mini-Instruct), and training procedures and code are documented both on [GitHub](https://github.com/RUC-GSAI/YuLan-Mini/) and in a [corresponding paper](https://arxiv.org/abs/2412.17743). The model itself is made available through [Ollama](https://huggingface.co/yulan-team/YuLan-Mini-Instruct#quick-start-%F0%9F%92%BB) for convenient use.

The detailed documentation of YuLan-Mini brings home the degree of scaffolding possible in the current open source AI landscape. For instance, to bootstrap maths abilities, YuLan-Mini uses Qwen 2.5 Math 7B Instruct as a teacher model; for instruction tuning, AllenAI's DOLMA dataset plays an important role; and for reward modeling the [Skywork Reward model](https://huggingface.co/Skywork/Skywork-Reward-Llama-3.1-8B), built on public data, is used. YuLan-Mini exemplifies the continuing reliance of current models on large amounts of synthetic data, in a tradition that goes back to Alpaca's first GPT4-derived datasets. The prominence of synthetic data is something we follow with interest, as model makers have to walk a fine line between performance improvements and [model collapse](https://openreview.net/forum?id=iqoqtNyVta).

We commend the effort involved with open-sourcing this model to such a significant extent. Somewhat surprisingly, YuLan-Mini has received relatively little attention from the open-source community. With all versions of the model currently sitting at less than [150 downloads per month](https://huggingface.co/mradermacher/YuLan-Mini-GGUF), we think there is a lot more potential for this model out there. We encourage anyone interested in open source generative AI to give this model a spin, peek under the hood, and learn from its high documentation standards.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: YuLan
---
::