---
title: The role of Big Tech in open-source AI
description: In which we discuss the current influence of Big Tech in the open-source AI space
date: 2025-06-09
author: Dick Blankvoort
status: unpublished
---
# The role of Big Tech in open-source AI
<author :author="author"></author>
<date :date="date"></date>

## Introduction
<!-- Big tech has played a large role in the AI space so far. In this post we investigate its impact and characteristics. We additionally investigate the impact of academia. -->
The AI race in general has been largely led by companies which broadly fall under the umbrella of 'Big Tech'. However, innovations developed by these companies have for a significant part been closed-source. In this blog post, we investigate the impact of Big Tech on the open-source landscape in order to attempt quantify the impact these companies have had on public AI model development. We also explore the national origins of open-source AI models in order to get a picture of the degree to which research has been centralized in the United States and China. In general we find that, although the role of Big Tech and the US/China remains dominant in the closed-source space, in the open-source space the research field can be seen more as a larger-scale international collaboration.

This blog post is written as an accompaniment to our [data analysis notebook](), which we draw heavily on.

<!-- General approach: we do a classification of all models in our index and perform a quantitative analysis. -->
To investigate our claims, we perform a classification of each open-source model in our index by:
1. Academic or non-academic origins
2. Big Tech dominance (Chinese or American)
3. Country of origin.

This metadata can be found in our YAML files. For our analysis, we [fundamentally assume that our index represents a representative sample of the state-of-the art of the open-source landscape](/guides/osai-overview-value).

<!-- The prevalence of academia -->
![Diagram depicting the prevalence of academia in OSAI](/images/academic_pie.png "Academic prevalence in OSAI")
We find that academia still plays a major role in open-source AI, contributing nearly a third of the models currently in our index. This indicates that open progress on AI models is currently propelled forward by a combination of academic and non-academic institutions.

<!-- The prevalence of Big Tech -->
![Diagram depicting the prevalence of big tech among OSAI companies](/images/big_tech_pie.png "Big Tech prevalence in OSAI")
Further, we see that though Big Tech contributes significantly to open-source AI (with Chinese and American Big Tech together contributing more than a quarter of all models), they are far from the only players.

<!-- Distributions of national origins -->
![Diagram depicting the national origins of OSAI institutions](/images/national_origins_pie.png "National origins in OSAI")
Lastly we see that, indeed, America and China remain dominant in the AI space. American models span nearly 40% of all models in the index, while Chinese models span more than 30%. However, there is also a significant effort towards international collaborations, and European models together contribute a not-insignificant 12.5% of models. As such, while the two major players in the AI space are indeed dominant, there remain sustantial avenues for nations outside the US and China (and Europe in particular) to participate.

<!-- Identical analysis for latest models -->
We next restrict our analysis to just the [latest](/news/performance-classes) models. I.e.: those which represent the state of the art of publicly available models.

![Diagram depicting the prevalence of academia in OSAI among latest models](/images/academic_pie_latest.png "Academic prevalence in OSAI among latest models")

![Diagram depicting the prevalence of Big Tech among OSAI companies in latest models](/images/big_tech_pie_latest.png "Big Tech prevalence in OSAI among latest models")

![Diagram depicting the national origins of OSAI institutions in latest models](/images/national_origins_pie_latest.png "National origins in OSAI among latest models")

For this subset we see a somewhat more restricted picture. Non-academic research significantly outcompetes academic research, and Big Tech becomes somewhat more dominant. Further, we see a significant decrease in the diversity of the national origins of models. On the other hand, however, we also see that there is still significant room for non-big-tech companies to compete within this space, and though the diversity of countries decreases it remains the case that international organizations are still able to compete to a significant extent. As such we can conclude that, even at the cutting edge of open-source AI, there remains a significant amount of innovation outside of the purview of Big Tech.

<!-- Conclusion: The space is still diverse and a collaboration. Even when limiting ourselves to just the latest models. -->
## Conclusion
In the above charts, we found that the AI space can still be characterized by diversity and a collaboration between academic and non-academic institutions. We provide evidence against the belief that research is mostly centralized in the United States and China and show that, at least in our index, both the globality of open-source AI and its cutting edge have a significant international character.
