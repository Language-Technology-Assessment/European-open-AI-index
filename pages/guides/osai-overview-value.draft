---
title: Assessing the Representativeness of the OSAI Index
description: In which we investigate the value of the European Open Source AI index as an overview of the open-source AI landscape
date: 2025-06-13
author: Dick Blankvoort
status: unpublished
---
# Assessing the Representativeness of the OSAI Index
<author :author="author"></author>
<date :date="date"></date>

<!-- Goal of the blog-post: Investigating whether the OSAI index is representative. -->
At the European Open Source AI Index, we invest a good deal of effort into investigating the open-source status of various AI models. As the index grows more comprehensive, the question emerges of how well it serves as a representative overview of the open-source AI landscape as a whole. In this post, we investigate this fact by performing a quantitative data analysis, accompanied by a forthcoming analysis notebook. <!-- TODO Add link when discussed and included -->

<!-- Data collection approaches and weaknesses therewith. -->
## Basic statistics and large-scale gaps
Existing resources do not offer a complete picture of open-source AI models. As such we need to work with different data sources. For this, we track all open-source AI models published on Ollama, on the LLM arena, and the top 100 most liked models on HuggingFace ([^1]). We believe this provides us with a good longitudinal overview. Our index includes models from [13 different countries](/guides/big-tech-companies-role), indicating that geographic diversity is extant to at least a reasonable degree in our index. We additionally track all major Chinese Big Tech companies and AI tigers, which should hopefully provide a good overview of [the Chinese AI landscape](/guides/chinese-western-divide). The European comprehensiveness of our index, however, remains unknown. This is a possible indicator for a weakness. Our index does not yet track multimodal models. This makes it rather weak in this regard. Lastly, we factually lag behind a bit in the sheets and do not yet track everything we want to. As such there might be knowledge gaps there.

<!-- Basic inclusion stats. Reference to model diversification. -->
## Comprehensiveness of model inclusion
Our dataset is highly curated, with us logging 0.0074% of the models on HuggingFace and 28.24% of logged model families finding their way into the index ([^2]). This latter fact means that not all models relevant to OSAI research are included in our index. For one, we limit ourselves to [models which independently represent a significant enough advance in model development](/guides/trends-open-source-model-development). In general, we only aim to include the most relevant models in our index.

<!-- Grounded analysis of biases. -->
## Possible biases
The fact that we include multiple Llama entries makes it so that Meta is slightly overrepresented in our index ([^3]). Additionally, through our quantitative analysis we find that there is significant disconnect between the relative amount of image/audio/video models in our index versus HuggingFace ([^4]). This may indicate that image models are significantly underrepresented and audio/video models are overrepresented. Though we have taken great steps to investigate the OSAI community from different angles, there remains the significant possibility that there are projects we are unaware of. Lastly, we find that there is slight possible bias towards the DeepSeek models in our index ([^5]).

<!-- Grounded analysis of strengths. -->
## Possible strengths
In our analysis, we find no significant bias towards newer models based on the performance classes ([^6]). Distributions for organizations also seem to hold sensibly between modalities and performance classes ([^7]). We find no significant biases evident from the classifications of organizations, and in terms of modalities we can see interpretable trends which may indicate robust trends. This means that overall, aside from a skewed distribution of model modalities, our model collection largely follows sensible distributions.

<!-- Wrapping things up: the index is robust enough to function as an object of quantitative data analysis of the AI landscape. -->
## Conclusion
In general, we find that the European Open Source AI index serves as a fairly representative sample of the open-source AI landscape. Though certain model families are slightly overrepresented and not all modalities are logged equally comprehensively, in general we find that sensible data distributions hold.

[^1]: 'Sources' tab on https://docs.google.com/spreadsheets/d/1Ay_Y_Xr4Bb-AUu_RRU_phkGdglERffG2gHM5PlbgTpQ/edit?usp=sharing
[^2]: 'Simple counts of models and organizations' section in the quantitative analysis notebook.
[^3]: https://osai-index.eu/model/llama-4, https://osai-index.eu/model/llama-3.3, https://osai-index.eu/model/llama-3.1, https://osai-index.eu/model/llama-3, https://osai-index.eu/model/llama-2
[^4]: 'Types' section in the quantitative analysis notebook.
[^5]: 'Performance class' section in the quantitative analysis notebook.
[^6]: 'Performance class' section in the quantitative analysis notebook.
[^7]: 'Organization & Types' and 'Performance class' sections in the quantitative analysis notebook.
