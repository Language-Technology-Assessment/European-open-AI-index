---
title: The Chinese-Western divide in AI
description: In which we outline the divide between the Chinese and Western AI landscapes
date: 2025-06-13
author: Dick Blankvoort
status: published
---
# The Chinese-Western divide in AI
<author :author="author"></author>
<date :date="date"></date>

As western researchers, [it is oftentimes difficult to divine what is going on at the other side of the Great Firewall](https://time.com/6289567/china-restricts-open-source-data-research-backfire/). By and large the Chinese AI space remains obscure to the rest of the world, leading to new models occasionally [just 'appearing' from the perspective of the West](https://www.britannica.com/money/deepseek). In this blogpost, we seek to provide some more context behind the Chinese AI landscape, and provide a picture as to how the space has evolved to the present day.

## What makes the Chinese open-source AI space obscure
A first challenge with regards to tracking open-source AI research on the Chinese side is that not all AI models are published on the same platforms used in the West. Though HuggingFace remains a popular platform in China and most major releases are published there, there is competition from a Chinese-only platform known as [WiseModel](https://wisemodel.cn/home). Tracking models on this platform requires crossing the language barrier in order to divine what is going on in the space, and that is a barrier not easily crossed. This means that lesser-known models often go unnoticed.

A second challenge is the culture barrier. Though a significant part of AI research is published in English as well as Chinese, Chinese research is done from a distinctly different grounding. For instance, a significant part of research on [tokenizing Chinese characters](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00560/116047) remains primarily centralized in the Chinese AI space. Translation through can also result in nuances being dropped, as exemplified by [discrepancies between the Chinese and English releases of the CCP's foreign policy statements](https://uscnpm.org/2022/06/05/sabine-mokry-lost-in-translation-discrepancies-official-chinese-foreign-policy-translations/).

Lastly, DeepSeek has demonstrated the necessity of sometimes obfuscating research due to e.g. sanctions. In a similar way to which western AI companies hide the true nature of their pretraining datasets to avoid [risks of backlash](https://arxiv.org/abs/2311.03449), Chinese AI companies might see themselves necessitated forced to hide information about their hardware infrastructure to obfuscate the use of [smuggled GPUs](https://www.tomshardware.com/pc-components/gpus/chinese-businessman-shows-off-sanctions-busting-nvidia-ai-gpus-he-bought-despite-us-ban-200-h200-gpus-skid-past-us-sanctions).

## The commercial Chinese OS landscape
From what we can gather, there are two major groups within commercial Chinese open-source AI space. These are the traditional Chinese Big Tech companies (Baidu, Alibaba, Tencent, Xiaomi) as well the Chinese AI tigers (Zhipu AI, Moonshot AI, Minimax, Baichuan Intelligence, Stepfun, and 01.AI). The former represent the traditional entrenched tech conglomerates, while the latter represent the new wave of AI start-ups seeking to disrupt the industry.

As things stand, all of the Chinese Big Tech companies have thrown themselves into the open-source AI space. Tencent has been developing both open LLMs and video models through their Hunyuan series, Alibaba is responsible for the development of both the text-based and multimodal Qwen models as well as the video-generating Wan models, and Xiaomi has just recently published their open-source MiMo models. Lastly, though Baidu has contributed no models which fit within our index, their work on [ERNIE and related projects](https://huggingface.co/ernie-research) has contributed to the advancement of open-source reseaerch.

The AI tigers [are six AI-based Chinese start-ups which have demonstrated great promise to the industry](https://qz.com/china-six-tigers-ai-startup-zhipu-moonshot-minimax-01ai-1851768509). All of these start-ups have made commitments to publishing their technologies as open-source, with [Baichuan](/model/baichuan), [01.ai](/model/yi) and [Minimax](/model/minimax-text) focusing around creating text-based models, [StepFun](/model/step-video) focusing around providing video models, Zhipu.AI delivering both [text-](/model/glm) and [image-based](/model/cogview) models, and Moonshot [focusing on vision-language models](https://huggingface.co/moonshotai/Moonlight-16B-A3B). Despite their open-source commitments, though, the degree to which these models are in actuality open-sourced is rather disappointing.

Classifying all Chinese AI models in our index, and keeping in mind that there might be some bias in which models are represented due to the above-mentioned reasons, we obtain the following pie chart for the origins of Chinese models in our index.

![Diagram depicting the distribution of Chinese AI models](/images/chinese_model_distribution.png "Origins of Chinese AI models.")

From this, it seems that the Chinese AI space is highly centralized along the above-mentioned ten companies.

## The academic Chinese OS landscape
The above pie chart also indicates the degree to which academic institutions contribute to the open-source Chinese AI landscape. In general, we see that research efforts in the early years of OSAI were primarily led by student teams, the most notable example of which is [OpenChat](/model/openchat). Currently, however, work has shifted more towards [larger-scale research collaborations](/model/eurus) and [independent research labs](/model/aquilachat), indicating that academic AI research has both intensified and etablished itself in more formal institutions. While it is difficult to speculate on the future, we would expect such centralization trends to continue with the establishment of [national-level AI collaborations](/model/internlm).

## Conclusion
There [remain significant geopolitical divides](/guides/big-tech-companies-role) in the open-source AI landscape, with the Chinese-Western one being most notable. The sudden rise of DeepSeek and the general lack of knowledge about the Chinese AI landscape in general underpin the need to ensure that the open-source community stay united and aware of each other's research. In general, when constructing our index we found a significant lack of resources capturing the entire AI space, leading to fragmentation and duplicate work. To ensure more effective and global research, we believe the open-source community would benefit from establishing more communication channels and getting in touch with the other side of the isle.
