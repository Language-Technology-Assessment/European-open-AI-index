---
title: An overview of AI model types
description: Providing an overview of the different types of AI models available
date: 2025-02-25
author: Dick Blankvoort & Mark Dingemanse
status: published
---
# An overview of AI model types
<author :author="author"></author>

In recent years, the field of AI has grown dramatically. Besides the introduction of ChatGPT and the subsequent revolution in text-based LLMs, there has been a revolution of no lesser significance in image-based diffusion models. The surge of new models can make it challenging to see what types of model are available and how current models should be categorized. Here we provide an overview of the most common types of AI models currently available, with the aim of helping the reader to get a better grasp on the AI landscape as a whole.

Throughout this blog post, we provide references to example models in our index, if available, using a grid view.

## Text-based large language models
::the-index
---
hideFilters: true
filters: 
  view: grid
  models: OLMo
---
::

Let's start with the models which initiated the recent revolution in the field of AI; **text-based LLMs**. It is useful to think of text-based models such as [ChatGPT](https://chatgpt.com) as constructed in (at least) two phases. First, a base LLM is developed which stores a model of human language and uses it to generate text. Subsequently, this model is 'fine-tuned' (slightly modified) in various ways to serve as an effective chatbot.

### Base models
<!-- TODO: Explain what exactly a token is. -->
A **base LLM** (sometimes described as a foundation LLM) is a text prediction engine that is trained to generate probabilities of possible next tokens given an input prompt. Recent text-based LLMs are typically trained on vast amounts of data, including countless websites, books and other text sources. By statistically representing the relationships between billions of tokens, they can generate plausible continuations of sequences of tokens. Base LLMs are often trained on supercomputers, since the amount of processing power required is vast.

### Instruct models and chat models
Though a base LLM is excellent for text prediction tasks, it does not straightforwardly allow for carrying on conversations. For this, a derivative model is necessary in the form of an **instruct model**. Instruct models are created by taking an existing base model, and repeatedly showing it examples from human text-based interactions. This allows the model to generate patterns mirrorring some aspects of the source interactions, opening up the possibility for people to treat it as a conversational participant.   

**Chat models** are instruct models which have received additional fine-tuning to avoid harmful conversation topics and to serve as helpful assistants. By further tuning a model on examples of helpful AI conversations and showing examples where the model rejects discussing harmful topics, chat models can be made to pick up on the pattern that they should output text in a helpful tone and reject harmful topics.

It is worth noting that although the terms 'chat model' and 'instruct model' are usually used in the sense described above, **the terms are also occasionally used interchangeably**. A model may be advertised as an instruct model when it has in fact undergone safety fine-tuning, and a model which has only undergone instruction tuning may sometimes be described as a chat model. The ambiguity with regards to this terminology is partially due to the inherent complexity of the underlying subject matter, and partially due to frequent attempts to combine the two tuning stages into one. In general, it is best to inspect the specifics of a chat- or instruct-model on a case-by-case basis.

Fine-tuning a base model into an instruct model and subsequently a chat model requires far less computing power than training the foundation model from scratch. Typically, only a few million instructions are needed and the amount of processing power required is only slightly more than the amount required for running the model in the first place. As such, the barrier of entry for deriving chat models from base models is far lower than the barrier of entry for constructing base models in the first place. This means that many more players can participate in the construction of chat- and instruct-models than in the construction of base models.

In our index, we include chat- and instruct-models under the 'text' mode label. For each model, we also list the underlying base models.

### Reasoning models
::the-index
---
hideFilters: true
filters: 
  view: grid
  models: eurus, deepseek-R1
---
::

**Reasoning models** are the most recent types of models which have emerged in the AI space, exemplified by models such as [DeepSeek-R1](https://huggingface.co/deepseek-ai/DeepSeek-R1) and basing themselves off techniques pioneered by models such as [Eurus](https://huggingface.co/openbmb/Eurus-70b-nca). Such reasoning models are better able to handle multi-step reasoning tasks by breaking them up into separate steps.

It is worth noting that reasoning LLMs do not strictly 'reason' in the common sense. Instead, they are tuned in the same way as chat models are tuned to do particularly well at a task known as chain-of-thought reasoning. In chain-of-thought reasoning, the LLM does not commit to a final response right away but iterates over multiple steps (a 'chain of thought'), adding all intermediate steps to the context window, allowing them to contribute to the final answer. This process is designed to mimic ([though it might not entirely reflect](https://arxiv.org/abs/2307.13702)), the process of human thinking and self-reflection.

## Code LLMs
::the-index
---
hideFilters: true
filters: 
  view: grid
  models: StarCoder
---
::

**Code LLMs** are LLMs specializing in handling code. There are two main ways of creating a code LLM. Firstly, it is possible to further train a regular base, chat or instruct model using code data (possibly adding some code-integrating instructions) to arrive at a model which can understand and generate code in a conversational setting. The model this produces is akin to the 'chat' functionality of GitHub Copilot, with the model serving as a helpful assistant for aiding in code-related tasks.

The second way of creating a code LLM is to train a model from scratch using code data. This results in a model which does not necessarily understand human language, but understands how to complete code very well. As such, models produced in this way are primarily useful as code autocompletion agents.

Code LLMs are usually tuned on multiple programming languages, allowing for a great deal of versatility. However, it is not uncommon to see further fine-tuning of a code model to a specific language (e.g. Python), to allow it to perform particularly well when programming in one specific setting.

### Math LLMs
**Math LLMs** are large language models fine-tuned to perform well on mathematical reasoning tasks. Similarly to code LLMs, a few approaches are possible.

Firstly, it is possible to tune a pre-existing large language model to perform particularly well at mathematical reasoning. Existing approaches have tuned base, chat-tuned, instruct-tuned, and even code-tuned LLMs to provide good mathematical reasoning. However, all of these approaches generally converge to a model that specializes in solving and reasoning about mathematical problems in natural language.

Next, it is possible to tune a language model in the same way one would tune a code completion LLM, making it specialize in completing mathematical proofs using a [proof assistant](https://en.wikipedia.org/wiki/Proof_assistant). This allows for more logically sound reasoning; however, it also requires translating a problem to strictly formal natural language.

Lastly, [recent approaches](https://huggingface.co/internlm/internlm2-math-base-7b) have looked into an LLM which somewhat combines the former two approaches; being able to both understand and think about mathematical problems in natural language and translate the corresponding problem to the language of proof assistants. On the whole, the field of math LLMs remains quite experimental.


### Agentic LLMs
**Agentic LLMs** are LLMs specifically tuned to interface with tools or to perform web-based tasks. Given that both the approaches taken and the applications for which agentic LLMs are designed vary widely, it is difficult to say anything about this group in a general sense. However, a few common facts hold. Firstly, agentic LLMs tend to specialize in either augmenting an LLM to interface well with external tools (e.g. a way of constructing and running programs), or in acting as sophisticated web-based agents. Agentic LLMs also tend to be quite experimental, with each adopting novel techniques for optimizing agentic actions.

Given the emergent nature of agentic models, there are many potential barriers that still need to be addressed. Most notably, agentic LLMs are usually not sufficiently open-source and [potentially pose inherent security risks](https://techcrunch.com/2025/03/07/signal-president-meredith-whittaker-calls-out-agentic-ai-as-having-profound-security-and-privacy-issues/). Future research remains to demonstrate the potential utility of such models and investigate how they can be constructed in an open manner.

## Image, video, and audio models
Although text-based LLMs represent the most popular use case and have seen the most activity in terms of model development, there is also a wide variety of AI models capable of generating audiovisual media of various kinds. Here we highlight the most notable types.

### Image models
::the-index
---
hideFilters: true
filters: 
  view: grid
  models: OmniGen
---
::

**Image diffusion models** are the powerhouses which fueled the recent revolution in AI image generation. Notable members include Midjourney and Stable Diffusion. Image diffusion models operate by attempting to learn how to extract images in the target context from random noise. An image diffusion starts with a completely noisy image and, by subsequently predicting which noise was added, attempts to reconstruct a fully non-noisy image. Consumer-oriented image diffusion models typically condition their output on text, allowing for generating an image a particular way based on a text prompt. The way image diffusion models are trained is typically to feed them images along with text data describing the image, allowing the model to both learn how to generate the images and how to connect the images to the text.

The architecture of an image diffusion model is amenable to many modifications, allowing for, for instance, generating an image based on a different image (image modification), or for generating an image based off a sketch or texture map (ControlNet). Image models are often fine-tuned to output images within specific genres, such as cartoons or paintings.

### Video models
::the-index
---
hideFilters: true
filters: 
  view: grid
  models: Open-Sora
---
::

**Video-generating models** are often variations on the theme of image-generating models. The key challenge for video models compared to image-generating models is to provide consistency between frames, which they accomplish by conditioning subsequent frames on previous frames in various ways. Currently, video-generating models run into issues when attempting to generate longer videos, videos of variable length, and videos of varying resolution. Similar to agentic models, they also commonly suffer from a lack of open-sourceness. In particular, the question of how to create a video model using open-source data has not yet been entirely settled. In general, though video-generating models have already seen some adoption, for now they remain quite experimental.

### World models
An aspirational fine-tune of the video model is the world model. World models seek to ground the video they generate into a virtual world and allow for some degree of control, creating a video-game-like experience. The aim of world models is to allow for the generation of grounded digital worlds. Though some large players in the AI space have already committed to the development of world models, in general this type of model still remains very experimental.

### Audio models
::the-index
---
hideFilters: true
filters: 
  view: grid
  models: TangoFlux
---
::

Audio models are models for generating music and other auditory information. By and large they are equally as experimental as video models, though they have arguably seen slightly more adoption. Audio models are by and large still quite closed, leading to difficulty establishing their typical construction. Nonetheless, they have been shown capable of generating high-quality melodies, vocals, instrument tracks, and even entire songs.

## Multimodal LLMs
Multimodal LLMs are perhaps the most varied of all LLM categories. Very broadly, multimodal LLMs seek to incorporate information from modalities other than text in order to enhance the utility of LLMs. The simplest and most common variant of a multimodal LLM is an image-text-to-text model, which can process images as well as text. However, many variants of multimodal LLMs exist. Notably, some multimodal models have grown to allow for both the processing and generation images and text, and one has proven capable of processing text, images, video, and audio and generating both text and audio.

The exact recipe for constructing a multimodal LLM remains largely in flux, with models processing and generating their target data in many different ways. A common approach, however, is to take a pre-existing LLM and further train it to be able to handle information across a range of target modalities.

## Conclusion
Though this overview seeks to have outlined the most common types of AI models, many more exotic and narrow types still exist. The AI space is vast, and the process of navigating it can feel more like exploration than the plotting out of any particular route. We hope this overview of common model types provides readers with a useful view of the overall landscape, just as our [index](https://www.osai-index.eu/the-index "European Open Source AI Index") helps them to navigate questions of openness and transparency.
