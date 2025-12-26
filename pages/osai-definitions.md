--- 
title: Open Source AI definitions
description: "Open Source AI definitions"
author: European Open Source Index
date: 2025-12-27
status: published
---

# A European Open Source AI Definition

In Europe, everyone developing and deploying open-source generative AI systems has to navigate two issues: some of the strictest personal data protection laws (in form of the GDPR or its derivatives in e.g. the UK or Switzerland) and unclear regulation of open-source AI systems (e.g. underspecified use of open-source terminology in the EU AI act and the Cyersecurity Act). To make things worse, Europe - unlike the US and China - does not have a definition of open source AI that is aligned with its own laws. This confusing situation on the regulatory side is sharply contrasted by the significant contributions that organisation in Europe contribute the open source AI ecosystem. A latest example of this is the Swiss AI Initiative's "Apertus" model series that achieved an outstanding degree of openness. It's high time to clarify our regulation of open-source AI to unlock the continent's potential to chart an independent way forward. Here, we recap current defintions of open source (generative) AI and propose a European Open Source AI definition that is simple, GDPR-aligned, and uniquely European.

### Current definitions and European regulation 

As of early 2026, European open-source AI model builders and providers are still left in legal limbo. While open-source AI is explicitly mentioned in legal framework such as the EU AI Act and the Cybersecurity act. An unresolved key issue is whether open data is part of open-source AI. Two definitions have been proposed so far, one in China and one in the US. China's Open Atom Foundation has published legal documents that make clear that in China, open source AI refers only to model weights, open data not included. In the US, the Open Source Initiative (OSI) has published their "Open Source AI Definition 1.0", that ,in a nutshell, encourages open data as part of open-source AI but allows private, not open-source-licensed data to be used in OSAI models. The European Union's AI Office is yet to clarify which defintions of open source AI applies to us. Or is Europe better off charting its own way forward?

Distinct from both the US and China, Europe has some the strictest privacy and data protection regulations in form of the General Data Protection Regulation (GDPR). If these uniquely European achievements are to be carried over into the age of (open-source) AI, the only working approach to open and transparent AI models is to comprehensively share training data that is both appropriately open-source licensed _and_ open for inspection for GDPR compliance. At its core, the matter is simple: the only way to ensure all [eight core rights](https://gdpr-info.eu/chapter-3/) of people in Europe are granted is in form of complete data transparency.[^1]

|  | Open Weight | OSAI in China | OSAI in the US  | European Open Source AI |
| :--- | :--- | :--- | :--- | :--- |
| Defined by | | _Open Atom Foundation_ | _Open Source Initiative_ | _EU AI Office?_ |
| **Model Weights** | Released | Released | Released | Released |
| **Training Code** | Not Shared | Fully Shared | Fully Shared | Fully Shared |
| **Training Pipeline** | Withheld | Nice to have | Nice to have | Fully Shared |
| **Training Data** | Not Shared/Not disclosed | Not Shared/Not disclosed* | Data sharing encouraged but closed data allowed* | Fully shared* |
| **Training Data Composition** | Partially/Not Disclosed | Fully Disclosed | Fully Disclosed | Fully Disclosed |


### A definition fit for Europe

A European open-source definition must be designed for maximal simplicity _and_ GDPR alignment, serving as a guardrail of innovative technology of and for [the public](https://www.mozillafoundation.org/en/research/library/public-ai/). This principle goes back to the beginning of the open source movement when core pieces of complex technology of personal computers (Unix kernels) were freed from the shackles of monopolized proprietary ownership and made freely available to everyone (for more see, [Open Sources](https://www.oreilly.com/openbook/opensources/book/raymond.html)). Europe is currently the most promising place to carry this spirit over into the era of AI. The European Open Source AI definition picks up the work of the Open Source Initiative (OSI) that published a US-centered definition in 2024: _the Open Source AI Definition 1.0_ (OSAID 1.0). For Europe, a simplified version of OSAID 1.0 is needed, that takes a clear stand on an issue that has proven divise within the open-source AI community: full release of model training data.

The OSAID 1.0 takes an ambiguous position when it comes to the question whether open data is part of open-source AI or not. The definition encourages open data while allowing training data to be withheld under certain conditions. To make this work, training data is broken down into four types, with different requirements of whether this data needs to either be shared, documented, or can be kept under wraps (in the case of "privately-held, unsharable data" (see [OSAID FAQ for more detail](https://opensource.org/ai/faq)). In the US context of an AI landscape dominated by private firms this makes sense and, as a result, OSI has opted that their definition is to be ["supported by diverse stakeholders", including private corporations and "cannot be an empty set"](https://github.com/samj/osaid/blob/main/presentations/2024-09-13-osi_townhall_16.pdf). In comparison, Europe features many publically-funded organisations and a strong public sector that actively develops open-source AI using public data. Our open-source definition must be designed for them. Given GDPR requirements, private or unsharable data has no place in open-source AI systems here. It's simple: In Europe, open-source AI _is_ public AI.

### Path towards distincly European AI 

The European Open Source AI defintion differs from its counterparts in the [US](https://opensource.org/ai/open-source-ai-definition) and [China](https://www.openatom.org/law/licence), setting Europe on a distinct path.

_It is simple._ A clear and simple boundary between open-weight AI and open-source AI is drawn. Open-source AI means full open-data AI. Only models meeting these high standard warrant true open-source status. If data can't be shared, call it _open-weight_.  

_It enables GDPR alignment._ Meeting the highest openness and transparency standards is the only way to enable compliance with the continent's outstanding data protection standards. In fact, uniquely high standards for privacy and data protection offer a [competitive edge](https://dataethics.eu/book/) for European AI to be at the forefront of open-source AI model development.  

_It actually supports innovation._ Despite what open-weight model providers often claim, only open-source AI [actually delivers innovation](https://www.linuxfoundation.org/hubfs/LF%20Research/lfr_market_impact_052025a.pdf). Organisations in Europe and beyond (e.g. The Swiss AI Inititave, Allen Institute for AI) demonstrate the public benefits of open-source AI. The European open-source AI definition is designed to include only true open-source AI technology, safeguards against [open-washing](https://dl.acm.org/doi/10.1145/3630106.3659005), and its legal adoption protects the many, often small, organisations that [already deliver top open models](https://preview.osai-index.eu/the-index).

 ___
Join the [discussion](https://codeberg.org/AI-technology-assessment/European-open-AI-index/issues/23). 
Make you voice heard at the [European AI Office](https://ai-act-service-desk.ec.europa.eu/en/ai-act-service-desk).



[^1]: This stance has seen increasing support in the form of court rulings that clarify the relationship between generative AI model output and other forms of (training) data, see GEMA vs OpenAI (Nov 2025).


More on European open-source AI and AI-ready data in the EU:

1. [European Data Union Strategy](https://digital-strategy.ec.europa.eu/en/policies/data-union)

2. [Digital Commons European Digital Infrastructure Consortium (DC-EDIC)](https://digital-strategy.ec.europa.eu/en/news/commission-launch-digital-commons-edic-support-sovereign-european-digital-infrastructure-and)

3. [Open Future AI commons report](https://openfuture.eu/publication/ai-commons/)
