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

Points from start of analysis:
- Our dataset is highly curated, with us logging 0.0074% of the models on HuggingFace and 28.24% of logged model families finding their way into the index.
- This also means that not all models relevant to OSAI research are included in our index. For one, we limit ourselves to [models which independently represent a significant enough advance in model development](/guides/trends-open-source-model-development).
- However, the goal of this blog post is to investigate to what degree we log _the most important models_. I.e. to what degree we achieve a complete overview of the *most relevant models* in our index.

Established facts:
- Currently, no central resource seems to be available which comprehensively logs OSAI models. As such we need to work with different sources.
- We track all open-source AI models published on Ollama, on the LLM arena, and the top 100 most liked models on HuggingFace. This should give a good overview of the major players.
- Our index includes models from [13 different countries](/guides/big-tech-companies-role), indicating that geographic diversity is extant to at least a reasonable degree in our index.
- We track all major Chinese Big Tech companies and AI tigers, which should hopefully provide a good overview of [the Chinese AI landscape](/guides/chinese-western-divide).
- The European comprehensiveness of our index remains unknown. This is a possible indicator for a weakness.
- Our index does not yet track multimodal models. This makes it rather weak in this regard.
- We factually lag behind a bit in the sheets and do not yet track everything we want to. As such there might be knowledge gaps there.

Possible biases:
- The fact that we include multiple Llama entries makes it so that Meta is slightly overrepresented.
- There is a significant disconnect between the relative amount of image/audio/video models in our index versus HuggingFace. This may indicate that image models are significantly underrepresented and audio/video models are overrepresented, however other explanations are possible (see analysis).
- Though we have taken great steps to investigate the OSAI community from different angles, there remains the significant possibility that there are projects we are unaware of.
- Possible bias towards DeepSeek.

Possible strengths:
- No significant bias is evident towards newer models from the performance classes.
- Distributions for organizations seem to hold sensibly between modalities and performance classes.
- No significant biases are evident from the classifications of organizations.
- In terms of modalities, we can see interpretable trends which may indicate robust trends. TODO investigate/think about those distributions.