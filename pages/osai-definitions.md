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

As of 2025, open source AI model builders and providers are left in legal limbo. While open source AI is explicitly mentioned in legal framework such as the EU AI Act and the Cybersecurity act. The European Union's AI Office is yet to clarify which defintions of open source AI applies. Two definitions have been proposed so far, one in China and one in the US. China's Open Atom Foundation has published legal documents that make clear that in China, open source AI refers only to model weights, open data not included. In the US, the Open Source Initiative (OSI) has published their "Open Source AI Definition 1.0", that ,in a nutshell, encourages open data as part of open-source AI but allows private, not open-source-licensed data to be used in OSAI models. In Europe, the issue of whether and to what extend open weights and open data are part of OSAI has not been clarified.

Distinct from both the US and China, Europe has some the strictest privacy and data protection regulations there are, prominently in form of the General Data Protextion Regulation (GDPR). The only approach to open and transparent AI models in line with such regulation are those that comprehensively share training data that is both appropriately open-source licensed _and_ open for inspection of GDPR compliance. Even in face of the recently proposed deregulations of AI in Europe as part of the Digital Omnibus, the GDPR applies to training data release as part of open source AI. All core rights [eight core rights](https://gdpr-info.eu/chapter-3/) as enshrined in the GDPR remain in place and the only way towards GDPR-compliant open-source AI remains complete transparency. 

Court ruling (German) that clarifies that a piece of data coming out of an LLM still covered by copyright of rights holder [find source]


|  | Open Weight | China Open Source AI | US Open Source AI  | European Open Source AI |
| :--- | :--- | :--- | :--- | :--- |
| Defined by | | _Open Atom Foundation_ | _Open Source Initiative_ | _EU AI Office?_ |
| **Model Weights** | Released | Released | Released | Released |
| **Training Code** | Not Shared | Fully Shared | Fully Shared | Fully Shared |
| **Training Pipeline** | Withheld | Nice to have | Nice to have | Fully Shared |
| **Training Data** | Not Shared/Not disclosed | Not Shared/Not disclosed* | Data sharing encouraged but closed data allowed* | Fully shared* |
| **Training Data Composition** | Partially/Not Disclosed | Fully Disclosed | Fully Disclosed | Fully Disclosed |


### A definition fit for Europe

A European open-source definition should be designed for maximal simplicity _and_ GDPR alignment, serving as a guardrail of innovative technology of and for (the public)[https://www.mozillafoundation.org/en/research/library/public-ai/]. These radical ideas go back to the very beginning of the open source movement when core pieces of technology of personal computers (Unix kernels) were freed from the shackles of proprietary ownership and made freely available to everyone (for more see, [Open Sources](https://www.oreilly.com/openbook/opensources/book/raymond.html)). Europe is in the best place to carry this spirit over into the era of AI. The European Open Source AI definition picks up the work of the Open Source Initiative (OSI) that published a US-based definition in 2024: _the Open Source AI Definition 1.0_ (OSAID 1.0). For Europe, a simplified variation of OSAID 1.0 is needed, that addresses an issue that has proven divise within the open source AI community: full release of model training data.

The OSAID 1.0 takes an ambiguous position when it comes to the question whether open data is part of open-source AI or not. The defintion maintains that, while encouraging data releases, withholding training data is possible in some cases. To make this work, training data is broken down into four types, with different requirements of whether data used in the model needs to be shared, "sufficiently documented", or can even be kept under wraps (in the case of "privately-held, unsharable data" (see (OSAID FAQ for more detail)[https://opensource.org/ai/faq]). In the US context of an AI landscape dominated by private corporations this makes sense in light of the OSIs aims to provide a defintion that is ("supported by diverse stakeholders, including private corporations" and "cannot be an empty set")[https://github.com/samj/osaid/blob/main/presentations/2024-09-13-osi_townhall_16.pdf]. At the time, there were simply no sufficiently open models available in the US. Europe is different. Given GDPR requirements, private or unsharable data has no place in open-source AI systems here. Open-source AI is AI of which all training data has to be shared (either by the model providers themselves or by linking to an existing already open source-licensed dataset. Since in AI systems, _data is part of the model_. Open-source AI _is_ public AI.

### Path towards distincly European AI 

The European Open Source AI defintion differs from its counterparts in the [US](https://opensource.org/ai/open-source-ai-definition) and [China](https://www.openatom.org/law/licence), setting Europe on a distinct path.

_It is simple._ A clear and simple boundary between open-weight AI and open-source AI is drawn. Open-source AI means open-data AI. Only models meeting these high standard warrant true open-source status. For others, its open-weight. 

_Its highest standards for openness allow GDPR alignment._ Meeting the highest openness and transparency standards are the only way to ensure compliance with the continent's strict standards when it comes to privacy protection. Aligned with the high standards for privacy and data protection that are a unique feature of the Europrean Union's landmark GDPR regulation (and derivates thereof that apply to most countries in Europe)

_It supports open innovation._ In AI, only openness all the way down can fullfil the promise that open source AI will deliver innovation. Like the early open source movement, open source AI is an alternative to he current state-of-the-art dominated by open-weight models build with private data. Open source AI is distinctly public AI, it is AI in the public domain, open to everyone - just like open-source software always was. Organisations from Europe and beyond (e.g. The Swiss AI Inititave's Apertus, Allen AI's OLMo models) show that truly open and public AI is possible. The European open-source AI definition supports truly open AI technology, safeguards again open-washing, and encourages open innovation. 

 ___
Discuss the definition [here](https://codeberg.org/AI-technology-assessment/European-open-AI-index/issues/23). 

Current issues in open-source AI as public AI in Europe:

1. AI-ready data governance in Europe

[Digital Commons European Digital Infrastructure Consortium (DC-EDIC)](https://digital-strategy.ec.europa.eu/en/news/commission-launch-digital-commons-edic-support-sovereign-european-digital-infrastructure-and)

[Open Future AI commons report](https://openfuture.eu/publication/ai-commons/)
