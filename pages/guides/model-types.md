---
title: An overview of AI model types
description: Providing an overview of the different types of AI models available
date: 2025-02-25
author: Dick Blankvoort
status: published
---
# An overview of AI model types
<author :author="author"></author>

In recent years, the field of AI has grown dramatically. Aside from the introduction of ChatGPT and the subsequent revolution in text-based LLMs, there has been a revolution of no lesser significance in image-based diffusion models. With more and more models being published every day, it has become a challenge to keep clear what types of model are available and how current models should be categorized. In this blog post, we seek to provide an overview of the most common types of AI models currently developed, with the aim of helping the reader to get a better grasp on the AI landscape as a whole.

## Text-based large language models
To start, it is useful to look to the models which initiated the recent revolution in the field of AI; text-based LLMs. Text-based models such as [ChatGPT](https://chatgpt.com) are not constructed in a single step, instead undergoing at least a two-phase construction. Firstly, a base LLM is developed which stores a model of human language and uses it to generate text. Subsequently, this model is 'fine-tuned' (slightly modified) to serve as an effective chatbot.

### Base models
A base LLM (also occasionally known as a foundation LLM) is a text prediction engine which operates by applying a detailed internal language model to preceding text. Recent text-based LLMs are often trained on vast amounts of data, frequently books and web data, storing their understanding of human language in an expansive machine learning network. Base LLMs are often trained on supercomputers, since the amount of processing power required is vast.

### Instruct models and chat models
Though a base LLM is excellent for text prediction tasks, it does not straightforwardly allow for carrying on conversations. For this, a derivative model is necessary in the form of an instruct model. Instruct models are created by taking an existing base model, and repeatedly showing it examples from human conversations. This allows the model to focus particularly on outputting language patterns mirrorring those of human conversation, giving it the ability to act as a conversation partner.

Chat models are instruct models which have received additional fine-tuning to avoid harmful conversation topics and to serve as helpful assistants. By further tuning a model on examples of helpful AI conversations and showing examples where the model rejects discussing harmful topics, chat models can be made to pick up on the pattern that they should output text in a helpful tone and reject harmful topics.

It is worth noting that although the terms 'chat model' and 'instruct model' are usually used in the sense described above, the terms are also occasionally used interchangeably. A model may be advertised as an instruct model when it has in fact undergone safety fine-tuning, and a model which has only undergone instruction tuning may sometimes be described as a chat model. The ambiguity with regards to this terminology is partially due to the inherent complexity of the underlying subject matter, and partially due to frequent attempts to combine the two tuning stages into one. In general, it is best to estimate the specifics of a chat- or instruct-model on a case-by-case basis.

Fine-tuning a foundation model into an instruct model and subsequently a chat model requires far less computing power than training the foundation model from scratch. Typically, only a few million instructions are needed and the amount of processing power required is only slightly more than the amount required for running the model in the first place. As such, the barrier of entry for constructing chat models is far lower than the barrier of entry for constructing foundation models. This means that, theoretically, many more players can participate in the construction of chat- and instruct-models than in the construction of base models.

In our index, we aim to only include chat- and instruct-models under the 'text' mode label. Below each model, the underlying base models are then listed.

### Reasoning models
Reasoning models are the most recent types of models which have emerged in the AI space, exemplified by models such as [DeepSeek-R1](https://huggingface.co/deepseek-ai/DeepSeek-R1) and basing themselves off techniques pioneered by models such as [Eurus](https://huggingface.co/openbmb/Eurus-70b-nca). Though the information available is still somewhat scant, it is likely that reasoning models are models tuned to perform some self-reflection before generating a response. This has the potential to greatly increase the quality of responses.

It is worth noting that reasoning LLMs do not strictly 'reason' in the common sense. Instead, they are tuned in the same way as chat models are tuned to do particularly well at a task known as chain-of-thought reasoning. In chain-of-thought reasoning, part of the output of an LLM is dedicated to thinking and reflecting about a problem before giving a definite answer.

## Variant large language models
Though the most common large language model is one specializing in chat-based communication, several other variants exist. In this section, we highlight the most common of these variants.

### Code LLMs
Code LLMs are LLMs specializing in handling code. There are two main ways of creating a code LLM. Firstly, it is possible to further train a regular base, chat or instruct model using code data (possibly adding some code-integrating instructions) to arrive at a model which can understand and generate code in a conversational setting. The model this produces is akin to the 'chat' functionality of GitHub Copilot, with the model serving as a helpful assistant for aiding in code-related tasks.

The second way of creating a code LLM is to train a model from scratch using code data. This results in a model which does not necessarily understand human language, but understands how to complete code very well. As such, models produced in this way are primarily useful as code autocompletion agents.

Code LLMs are usually tuned on multiple programming languages, allowing for a great deal of versatility. However, it is not uncommon to see further fine-tuning of a code model to a specific language (e.g. Python), to allow it to perform particularly well when programming in one specific setting.

### Math LLMs
Math LLMs are large language models fine-tuned to perform well on mathematical reasoning tasks. Similarly to code LLMs, a few approaches are possible.

Firstly, it is possible to tune a pre-existing large language model to perform particularly well at mathematical reasoning. Existing approaches have tuned base, chat-tuned, instruct-tuned, and even code-tuned LLMs to provide good mathematical reasoning. However, all of these approaches generally converge to a model that specializes in solving and reasoning about mathematical problems in natural language.

Next, it is possible to tune a language model in the same way one would tune a code completion LLM, making it specialize in completing mathematical proofs using a [proof assistant](https://en.wikipedia.org/wiki/Proof_assistant). This allows for more logically sound reasoning; however, it also requires translating a problem to strictly formal natural language.

Lastly, [recent approaches](https://huggingface.co/internlm/internlm2-math-base-7b) have looked into an LLM which somewhat combines the former two approaches; being able to both understand and think about mathematical problems in natural language and translate the corresponding problem to the language of proof assistants. On the whole, the field of math LLMs remains quite experimental.

### Agentic LLMs
Agentic LLMs are LLMs specifically tuned to interface with tools or to perform web-based tasks. Given that both the approaches taken and the applications for which agentic LLMs are designed vary widely, it is difficult to say anything about this group in a general sense. However, a few common facts hold. Firstly, agentic LLMs tend to specialize in either augmenting an LLM to interface well with external tools (e.g. a way of constructing and running programs), or in acting as sophisticated web-based agents. Agentic LLMs also tend to be quite experimental, with each adopting novel techniques for optimizing agentic actions.

### Domain-specific LLMs
Though many LLMs seek to provide knowledge in a broad range of domains, some instead specialize in specific areas of knowledge. The most common of these specializations is that of the biomedical specialist LLM, which seeks to augment doctors by providing medical advice. Domain-specific LLMs show potential in providing more specialist knowledge and taking on a more narrow role than that of a chatbot.

### Genomic language models
Lastly, a rather specific but relatively common type of specialized LLM is that of the genomic language model. Rather than attempting to understand language, this model seeks to understand the gene structure of DNA. Through this, it seeks to engender a greater understanding of the operational function of DNA and provide insight into how it can give rise to complex behavior in our bodies.

## Image, video, and audio models
Aside from text-based LLMs, there is also a wide variety of AI models capable of generating audiovisual media of various kinds. In this section, we highlight the most notable ones.

### Image models
Image diffusion models are the powerhouses which fueled the recent revolution in AI image generation. Notable members include Midjourney and Stable Diffusion. Image diffusion models operate by attempting to learn how to extract images in the target context from random noise. An image diffusion starts with a completely noisy image and, by subsequently predicting which noise was added, attempts to reconstruct a fully non-noisy image. Consumer-oriented image diffusion models typically condition their output on text, allowing for generating an image a particular way based on a text prompt. The way image diffusion models are trained is typically to feed them images along with text data describing the image, allowing the model to both learn how to generate the images and how to connect the images to the text.

The architecture of an image diffusion model is amenable to many modifications, allowing for, for instance, generating an image based on a different image (image modification), or for generating an image based off a sketch or texture map (ControlNet). Image models are often fine-tuned to output images within specific genres, such as cartoons or paintings.

### Video models
Video-generating models are often more sophisticated variants of image-generation models. Their key challenge compared to image-generating models is to provide consistency between frames, which they accomplish by conditioning subsequent frames on previous frames in various ways. Currently, video-generating models also run into issues when attempting to generate longer videos, videos of variable length, and videos of varying resolution. In general, though video-generation models have already seen some adoption, for now they remain quite experimental.

### World models
An aspirational fine-tune of the video model is the world model. World models seek to ground the video they generate into a virtual world and allow for some degree of control, creating a video-game-like experience. The aim of world models is to allow for the generation of grounded digital worlds. Though some large players in the AI space have already committed to the development of world models and released models show promise, in general this type of model still remains very experimental.

### Audio models
Audio models are models for generating music and other auditory information. By and large they are equally as experimental as video models, though they have arguably seen slightly more adoption. Audio models are by and large still quite closed, leading to difficulty establishing their typical construction. Nonetheless, they have been shown capable of generating high-quality melodies, vocals, instrument tracks, and even entire pop songs.

## Multimodal LLMs
Multimodal LLMs are perhaps the most varied of all LLM categories. Very broadly, multimodal LLMs seek to incorporate information from sources other than text in order to enhance the utility of LLMs. The simplest and most common variant of a multimodal LLM is an image-text-to-text model, which can process images as well as text. However, many variants of multimodal LLMs exist. Notably, some multimodal models have grown to allow for both the processing and generation images and text, and one has proven capable of processing text, images, video, and audio and generating both text and audio.

The exact recipe for constructing a multimodal LLM remains largely in flux, with models processing and generating their target data in many different ways. A common approach, however, is to take a pre-existing LLM and further train it to be able to understand information in the target modalities.

## Conclusion
Though this overview seeks to have outlined the most common types of AI models, many more exotic and narrow types still exist. The AI space is vast, and the process of navigating it is far closer to exploration than the plotting out of any particular route. For now it is hoped that this blog post has endowed the reader with greater understanding of AI, allowing them to navigate the space with greater ease.