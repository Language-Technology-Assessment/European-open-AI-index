--- 
title: Open Source AI definitions
description: "Open Source AI definitions"
author: European Open Source Index
date: 2025-12-05
status: published
---

# A European Open Source AI Definition

In Europe, everyone developing and deploying open-source generative AI systems has to navigate two issues: strict requirements for privacy protections laws (in form of the GDPR or its derivatives in e.g. the UK or Switzerland) and unclear regulation of open source AI systems (as included in the EU AI act and the Cyersecurity Act). To make things worse, Europe did not even have an own defintion of open source AI that is aligned with its own laws. Nonetheless, organisations in Europe have made significant contributions to the open source AI ecosystem with The Swiss AI Initiative's "Apertus" models a latest example. Here, we recap the current regulatory situations and propose a European Open Source AI defintion that is both GDPR-aligned and super simple. And the best thing about it: it is already used by some of the leading open source AI models of Europe.

### Current definitions and European regulation 

No clear definition linked to the EU AI Act and or GDPR

Only a definition proposed by the Open Source Initiative (Palo Alto, US) that does not mandate all training data to be shared. It has become clear that this approach is not in line with recent developments in Europe, where the GDPR has enshrined each person's [eight core rights](https://gdpr-info.eu/chapter-3/) in relation to their data.   

Court ruling (German) that clarifies that a piece of data coming out of an LLM still covered by copyright of rights holder


### A definition fit for Europe

Designed for maximal simplicity _and_ GDPR alignment

The European Open Source AI definition is modelled on the work of the Open Source Initiative (OSI) that published a US-based definition in 2024: _the Open Source AI Definition 1.0_ (OSAID 1.0). 
For Europe, a simplified variation of OSAID 1.0 is needed, which is crucially adjusted that enhances alignment with European law: full release of training data.

The US-based OSAID 1.0 breaks down training data into four types, with different requirements of whether data used in the model needs to be shared, "sufficiently documented", or can even be kept under wraps (in the case of "privately-held, unsharable data" (see (OSAID FAQ for more detail)[https://opensource.org/ai/faq]). 
In Europe, private or unsharable data has no place in open-source AI systems. Open-source AI is public AI. 

*This is a crucial change for several reasons:*

- That this is in line with the high standards of European law as clarified in xx court rulings. 

- Suits the European generative AI landscape, where publically-funded model builders and providers have shown that fully open AI is possible. Something that did not apply to the US-based definitions, a country with a gen AI landscape dominated by private organisations. https://github.com/samj/osaid/blob/main/presentations/2024-09-13-osi_townhall_16.pdf

*This is a _better_ definition for several reasons:*

simplicity 

https://digital-strategy.ec.europa.eu/en/news/commission-launch-digital-commons-edic-support-sovereign-european-digital-infrastructure-and

Aligned with the high standards for privacy and data protection that are a unique feature of the Europrean Union's landmark GDPR regulation (and derivates thereof that apply to most countries in Europe)

all training data has to be shared (either by the model providers themselves or by linking to an existing already open source-licensed dataset.
This definition is based on the view that, in AI systems, _data is part of the model_ 


Recent work has shown feasibility and potential of open-source AI. OLMo Trace, Apertus

| Feature | Open Weights | OSI Open Source AI (defined by the Open Source Initiative) | European Open Source AI (aligned with EU Law) |
| :--- | :--- | :--- | :--- |
| Model Weights | Released | Released | Released |
| Training Code | Not Shared | Fully Shared | Fully Shared |
| Open Training pipeline and steps | Withheld | Nice to have | Released |
| Training dataset | Not Shared/Not disclosed | Data sharing encouraged but closed data allowed* | Full open data* |
| Training Data Composition | Partially/Not Disclosed | Fully Disclosed | Fully Disclosed |


### Path towards distincly European AI 

The Open Source AI defintion for Europe proposed here differs from its counterparts in the US and China and sets Europe on a distinct path.

_It is simple._ A clear and simple boundary between open-weight AI and open-source AI is drawn. Open-source AI means open-data AI. Only models meeting these high standard warrant true open-source status. For others, its open-weight. 

_Its highest standards for openness allow GDPR aignment._ Meeting the highest openness and transparency standards are the only way to ensure compliance with the continent's strict standards when it comes to privacy protection.

_It supports open innovation._ In AI, only openness all the way down can fullfil the promise that open source AI will deliver innovation. Like the early open source movement, open source AI is an alternative to he current state-of-the-art dominated by open-weight models build with private data. Open source AI is distinctly public AI, it is AI in the public domain, open to everyone - just like open-source software always was. Organisations from Europe and beyond (e.g. The Swiss AI Inititave's Apertus, Allen AI's OLMo models) show that truly open and public AI is possible. Europe's definition must protect them. 
 

Public AI by Mozilla 
https://www.mozillafoundation.org/en/research/library/public-ai/

AI commons by open future?
https://openfuture.eu/publication/ai-commons/

Links: 
https://opensource.org/ai/open-weights
https://opensource.org/ai/faq
