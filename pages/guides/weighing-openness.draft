---
title: Weighting Openness Criteria Across Different AI Domains
description: How openess criteria is weighted across different domains. 
date: 2025-08-04
author: Nityaa Kalra
status: unpublished
---

# Weighting Openness Criteria Across Different AI Domains

The term "openness" in generative AI is often used as a blanket statement, but its meaning is far from monolithic. While the Open Source AI Index (OSAI) attempts to quantify this concept through a set of universal metrics, the importance of each metric shifts depending on the domain and the stakeholders involved. A researcher's definition of "open" can be different from a lawyer's, a security expert's, or a musician's. Therefore, a one-size-fits-all approach to openness can often be misleading and counterproductive.

At OSAI, we recognize this complexity. Rather than dictating a single, immutable standard, we aim to approach the concept of openness from a scientific perspective by breaking it down into its constituent parts. In this blog post we analyze how different openness criteria are weighted across various domains. 

## Academia and Research
For the academic and research communities, the gold standard of openness is reproducibility. The foundation of scientific inquiry rests on the ability to replicate and validate results, which is why the weighting in this domain leans heavily towards training code, data, model weights, and detailed documentation. These elements are considered essential, not optional.

This emphasis is reflected in community efforts like the [NeurIPS reproducibility checklist](https://jmlr.org/papers/v22/20-303.html) [1], which encourages open practices through formal requirements. The [Model Openness Framework (MOF)](https://arxiv.org/abs/2403.13784) by White et al. (2024) sharpens this perspective by distinguishing between completeness (the release of components like code, data, and weights) and openness (defined by the licenses attached to those components) [2]. For a researcher, the ideal is both: a complete release under a license that enables unrestricted scientific use.

## Legal
In the legal and compliance domain, the focus shifts to the legal and ethical implications of using a model. Here, stakeholders are less concerned with open-sourcing model internals and more focused on compliance, due diligence, and accountability. Clear documentation of the model development process, provenance of training data, and licensing terms are important here. 

These priorities are stated in legislative efforts like the [EU AI Act](https://artificialintelligenceact.eu) [3], which mandates that high-risk AI systems maintain technical documentation detailing their development and use (Article 11), and provide transparency to ensure human oversight (Article 13). 

## Finance and Healthcare

Both healthcare and finance operate in high-stakes, regulated environments where the cost of AI failures can be life-altering or economically devastating. In these domains, openness serves the purpose of risk mitigation, bias control, and traceable governance. While financial institutions and medical providers may not open-source their models, internal transparency is essential. Regulatory bodies require models to be explainable and compliant with privacy laws like HIPAA and GDPR. Auditability by internal teams and regulators is non-negotiable and is central to decisions like loan approvals or medical diagnoses. This shows that openness can also mean rigorous internal practices and verifiable documentation that satisfy regulatory, ethical, and societal expectations.

## Security

For security-critical systems, openness is a delicate balance between transparency and risk. Full public openness might invite exploitation, which is why controlled internal transparency is key. The [NIST AI Risk Management Framework](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) [4] emphasizes the importance of secure system logging, traceable component pipelines, and robust internal documentation to manage and mitigate security-related risks. This approach prioritizes accountability over full public exposure. Real-world incidents such as the misuse of publicly available LLM endpoints in phishing and jailbreak attacks have pushed stakeholders towards a model of openness that favors accountability over full exposure [5].

## Creative Industries (Music, Art etc.)
Creative fields value openness primarily in terms of rights management, attribution, and content provenance. For these stakeholders, openness ensures fair use and ethical generation, not necessarily code transparency. This distinction is at the heart of the ongoing global conversation led by organizations like the [World Intellectual Property Organization (WIPO)](https://www.wipo.int/portal/en/) [6]. WIPO's discussions on AI and intellectual property highlight the conceptual challenges that AI poses to traditional copyright law, particularly concerning authorship, originality, and the use of copyrighted works in training data. The creative community's definition of openness is therefore less about the free availability of a model's source code and more about a transparent, auditable process that supports ethical transparency and informed reuse.

## Summary and the Pursuit of Scientific Openness

The different domains are not entirely separate. Their needs are often interconnected. For example, the legal community's demand for data provenance to address copyright claims (a legal concern) directly benefits researchers who need to audit for bias (an academic concern). The security requirements of the finance and healthcare sectors provide a foundation of trust that benefits the public as a whole.

By demanding true scientific openness, we empower all stakeholders to navigate the complexities of this technology with a foundation of transparency and trust. At OSAI, we argue that while these different perspectives are all valid, they are best served by a commitment to scientific openness. This is a state where a model's creation, operation, and limitations can be fully understood, audited, and reproduced by the broader community. It is defined not just by ease of use or public access, but by the availability of the core components of the scientific process: the data, the code, the weights, and the methodology.

This distinction is critical in an era of rising "false openness". Many models today are released under open licenses but with key components like training data or code kept proprietary. This selective transparency may support limited use, but it blocks meaningful scrutiny. Without full access, researchers can not verify performance, regulators can not assess risk, and creators can not understand data provenance. This practice, sometimes called *openwashing*, goes against the very principles that true openness is meant to uphold. For openness to matter and be aligned with public interest, it must be complete, not conditional.

## References

[1] Pineau, J. et al. 2020. [Improving reproducibility in machine learning research (JMLR, vol. 22)](https://jmlr.org/papers/v22/20-303.html)  
[2] White, M. et al. 2024. [The Model Openness Framework: Promoting completeness and openness in AI (arXiv)](https://arxiv.org/abs/2403.13784)  
[3] [EU Artificial Intelligence Act](https://artificialintelligenceact.eu)   
[4] Tabassi, E. 2023. [NIST AI Risk Management Framework (AI RMF 1.0)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)  
[5] Carlini, N. et al. 2023. [Extracting Training Data from Diffusion Models (arXiv)](https://arxiv.org/abs/2301.13188)  
[6] [WIPO – World Intellectual Property Organization](https://www.wipo.int/portal/en/)
