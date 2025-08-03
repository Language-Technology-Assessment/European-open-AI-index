---
title: On the value of the OSAI index as an AI overview
description: In which we investigate the value of the European Open Source AI index as an overview of the open-source AI landscape
date: 2025-06-13
author: Dick Blankvoort
status: unpublished
---
# On the value of the OSAI index as an AI overview
<author :author="author"></author>
<date :date="date"></date>

<!-- Goal of the blog-post: Investigating whether the OSAI index is representative. -->
At the European Open Source AI Index, we invest a good deal of effort into providing a comprehensive overview of the open-source status of a representative sample of AI models. In this blog post, we investigate the degree to which this comprehensiveness holds as of (date) by performing a quantitative data analysis.

<!-- Data collection approaches and weaknesses therewith. -->
## Basic statistics and large-scale gaps
Currently, no central resource seems to be available which comprehensively logs OSAI models. As such we need to work with different sources. For this, we track all open-source AI models published on Ollama, on the LLM arena, and the top 100 most liked models on HuggingFace. We believe this provides us with a good longitudinal overview. Our index includes models from [13 different countries](/guides/big-tech-companies-role), indicating that geographic diversity is extant to at least a reasonable degree in our index. We additionally track all major Chinese Big Tech companies and AI tigers, which should hopefully provide a good overview of [the Chinese AI landscape](/guides/chinese-western-divide). The European comprehensiveness of our index, however, remains unknown. This is a possible indicator for a weakness. Our index does not yet track multimodal models. This makes it rather weak in this regard. Lastly, we factually lag behind a bit in the sheets and do not yet track everything we want to. As such there might be knowledge gaps there.

<!-- Basic inclusion stats. Reference to model diversification. -->
## Comprehensiveness of model inclusion
Our dataset is highly curated, with us logging 0.0074% of the models on HuggingFace and 28.24% of logged model families finding their way into the index. This latter fact means that not all models relevant to OSAI research are included in our index. For one, we limit ourselves to [models which independently represent a significant enough advance in model development](/guides/trends-open-source-model-development).
In general, we only aim to include the most relevant models in our index.

<!-- Grounded analysis of biases. -->
## Possible biases
The fact that we include multiple Llama entries makes it so that Meta is slightly overrepresented in our index. Additionally, through our quantitative analysis we find that there is significant disconnect between the relative amount of image/audio/video models in our index versus HuggingFace. This may indicate that image models are significantly underrepresented and audio/video models are overrepresented, however other explanations are possible (TODO analysis). Though we have taken great steps to investigate the OSAI community from different angles, there remains the significant possibility that there are projects we are unaware of. Lastly, we find that there is slight possible bias towards the DeepSeek models in our index.

<!-- Grounded analysis of strengths. -->
## Possible strengths
In our analysis, we find no significant bias towards newer models based on the performance classes. Distributions for organizations also seem to hold sensibly between modalities and performance classes. We find no significant biases evident from the classifications of organizations, and in terms of modalities we can see interpretable trends which may indicate robust trends. TODO investigate/think about those distributions.