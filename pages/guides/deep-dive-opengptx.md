---
title: "OpenGPT-X: Open source AI 'Made in Germany' falls short of own claims"
description: In this deep dive we evaluate OpenGPT-X's flagship Teuken models through the lens of openness
date: 2025-04-14
author: Dick Blankvoort & Jenia Jitsev
status: published
---
# OpenGPT-X: Open source AI 'Made in Germany' falls short of own claims
<author :author="author"></author>

<!--
# Relevant links
### HF pages
- Org page: https://huggingface.co/openGPT-X
- Research model: https://huggingface.co/openGPT-X/Teuken-7B-instruct-research-v0.4
- Commercial model: https://huggingface.co/openGPT-X/Teuken-7B-instruct-commercial-v0.4

### GH pages:
- Org page: https://github.com/OpenGPTX

### Sites
- Main site: https://opengpt-x.de/en/

### Papers
- Towards multilingual LLM evaluation: https://arxiv.org/pdf/2410.08928
- Data processing: https://arxiv.org/pdf/2410.08800
- Progress report: https://arxiv.org/pdf/2410.03730v1
- Models: https://arxiv.org/pdf/2410.03730
- MinHash/LSH algorithm: https://link.springer.com/chapter/10.1007/978-3-031-82481-4_27
- Tokenizer: https://arxiv.org/pdf/2310.08754

# Main narration brainstorming
-->

[The OpenGPT-X initiative](https://opengpt-x.de/en/) is an organization seeking to create open source AI models 'Made in Germany'. In this article, we evaluate its flagship [Teuken](https://opengpt-x.de/models/teuken-7b-de/) models through the lens of open source. In collaboration with Jenia Jitsev of LAION and the Jülich Supercomputing Centre, we explore some of the project's strengths and weaknesses. We find that the model falls short of its own claims of openness, and document early signs of adverse consequences for the European open source AI ecosystem.

OpenGPT-X is a project developed under the umbrella of GAIA-X, a European initiative seeking to create [an open and transparent platform for merging and sharing data](https://www.heise.de/news/Gaia-X-Bundesnetzagentur-stellt-117-Millionen-Euro-fuer-Projekte-bereit-6528649.html). To this end, OpenGPT-X has received [around 15 million euros from the German Federal Ministry for Economic Affairs and Climate Protection](https://www.dfki.de/en/web/news/kick-off-for-opengpt-x-dfki-and-partners-develop-large-scale-language-models-for-europe). With the project recently concluded, we evaluate the published models for transparency and openness.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: Teuken
---
::
Table: An overview of Teuken evaluated for 14 dimensions of openness. 

## Evaluating the Teuken models

### Access to training data
The Teuken models are described as being pretrained on ["data from publicly available sources"](https://huggingface.co/openGPT-X/Teuken-7B-instruct-research-v0.4/blob/main/README.md), with [openness being marketed as a key feature](https://opengpt-x.de/en/about/). We tried to verify these claims, investigating whether the model data is indeed as open as is purported. 

The data used to train the base model of the Teuken series originates from two sources; the [FineWeb-Edu dataset](https://huggingface.co/datasets/HuggingFaceFW/fineweb-edu) and a [private dataset](https://arxiv.org/pdf/2410.08800) constructed by OpenGPT-X itself. The FineWeb-Edu dataset is widely available and used as pretraining data in over 200 models. The data sources of the private dataset, on the other hand, has a number of qualities which make obtaining insight into it challenging.

The full set of training data was not made publicly available. This means that anyone seeking to inspect or reproduce the data behind the models needs to request data access from the model authors. Although this is fairly standard practice, it does pose challenges to transparency and makes it difficult to reconstruct what data went into the model.

Reconstruction is further hampered by a lack of a clear and open source codebase that documents the processes of data collection, curation, filtering and processing. While the model does come with a preprint that documents parts of the training procedure, not enough detail is provided to make reproduction feasible. Here we list a selection of data sources that are difficult or impossible to access.

<table style="margin: auto; border-collapse: collapse; margin-bottom: 20px;">
  <tr>
    <th style="border: 1px solid black; padding: 10px;">Data source</th>
    <th style="border: 1px solid black; padding: 10px;">Reason for highlighting</th>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">Corpus of Contemporary Irish</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://www.gaois.ie/en/corpora/monolingual">Replaced by newer dataset</a></td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">medi_notice dataset, Swiss Legislation Corpus</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://pub.cl.uzh.ch/wiki/public/pacoco/medi-notice">Inaccessible without a University of Zürich account</a></td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">Open Legal Data German court decisions</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://openlegaldata.io/research/2019/02/19/court-decision-dataset.html">Listed twice with different word and document count</a></td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">Norwegian Colossal Corpus</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://huggingface.co/datasets/NbAiLab/NCC">Newspapers removed after model release</a></td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">Various subsets of The Pile</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://pile.eleuther.ai/">No subsets provided, only The Pile and (for some subsets) scrapers</a></td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">PRINCIPLE bilingual English-Irish datasets</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://elrc-share.eu/repository/search/?q=PRINCIPLE&selected_facets=languageNameFilter_exact%3AIrish">Not clear which datasets were taken</a></td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">Unknown Slovenian Dataset</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://nlp.ffzg.unizg.hr/resources/corpora/slwac/">404 Error</a></td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">Swiss Policy Documents</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://opendata.swiss/en/dataset?keywords_en=environmental--policy&keywords_en=policy-analysis">Links to a search query with a single result</a></td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;">Various Wikimedia sites</td>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://en.wikipedia.org/wiki/Main_Page">Link to sites, not datasets</a></td>
  </tr>
</table>

We ran into various issues attempting to reconstruct how the model was trained, including 404 pages, pages inaccessible without a specific university account, and links to sites without specifying directions on versioning and access methods. Furthermore, as mentioned [in the model preprint](https://arxiv.org/pdf/2410.03730), the data mixture was adapted before being used for pretraining. This included strategic downsampling of English data and upsampling of data in other languages. However, no information was made available how this processing step was done. Without an exhaustive list of data sources and clarity on data processing procedures, we concluded that reproducing the training procedure was not feasible.

### Documenting preprocessing steps

Next, we examined the preprocessing procedure, these are all the ways in which the training data was edited before model training began. The authors published a preprint that promises to detail training data processing of the Teuken models that even mentions [saving the intermediate results of the data pipeline](https://arxiv.org/pdf/2410.08800), an important step that would enable inspection of the training procedure. However, these checkpoints in the training process were not made available. Making such intermediate steps publicly available can greatly contribute to the openness of the model, such as in the case of Allen AI's OLMo models [and the Dolma dataset](https://huggingface.co/datasets/allenai/dolma).

In contrast to the base model data mixture, the instruction-tuning mixture of Teuken is laid out quite well. As far as we can tell, all data sources are linked properly and open source datasets are used. The instruction-tuning data access could be further improved by publishing a final dataset, as for instance in the case of Cohere Lab's [Aya models](https://huggingface.co/datasets/CohereForAI/aya_dataset).

All in all, the data used to train the Teuken models is not as open as might appear at first glance. While data usage is partly documented, the lack of both a publicly downloadable training dataset and comprehensive documentation of data sources makes it impossible to verify claims that this model is truly open, transparent and reproducible - all hallmarks of open source technology.

### Model weights
Teuken [claims to be open source](https://opengpt-x.de/en/models/teuken-7b/), a core element of which is that the weights of the model are published (open-weights). In this section, we take a closer look at weight availability of the Teuken base and end models.

The base model weights of (pretrained) Teuken are available only upon request from the model authors. We have approached the model creators without specifying the purpose of the request to obtain the model weights, but unfortunately did not received a response yet. For the end model weights, two versions are shared via OpenGPT-X's HuggingFace page; a research model and a commercial model. Given that the paper makes no mention of such a distinction, we found this rather puzzling. The model card and the organization's site claim that the research model was trained on data with a non-permissive license, while for the commercial model this data was excluded. Based on this, we assume that the commercial model excludes the part of the private data mixture that was licensed non-permissively. If this is true, it further highlights the need for training data transparency to allow independent parties to verify these claims.

Given this situation, the question of whether Teuken's models can be called open-weights is somewhat up in the air. Base model weights are only available upon request, while the form of the end model weights is somewhat incongruous with the model described in the paper.

### Tokenizer

One of the claimed innovations of the Teuken model was its use of a balanced multilingual tokenizer. This tokenizer, as the authors claim, [was crucial for bringing down training costs](https://arxiv.org/pdf/2410.03730). In this light, it seems like a missed opportunity that relatively little is known about this tokenizer, as it is only available bundled up with the instruction-tuned model. The [paper from which it derives](https://arxiv.org/abs/2310.08754) provides some implementation details, but does not provide guidance regarding underlying data mixture. The research community could potentially benefit from further information regarding this piece of technology.

### Training and tuning source code
Contrary to other open projects, e.g. [Olmo by AllenAI](https://github.com/allenai/OLMo) , [SmolLM2 by HuggingFace](https://github.com/huggingface/smollm), or [DCLM by the DataComp initiative and their collaborators](https://github.com/mlfoundations/dclm), Teuken models lack training or fine-tuning source code with clear documentation how to reproduce model training. Without this, it is impossible to replicate the author's results, a tenet of open scientific practice.

<!--
### Cherry-picked Evaluation
Benchmark evaluation is an important part of the model building process, and its openness is crucial to allow independent parties to reproduce model performance claims and compare other models using the same evaluation procedure. The authors of Teuken provide a full open-source version of their multilingual benchmarks, building on the community-standard `lm-eval-harness` by EleutherAI. All tasks used in the benchmarks can [be inspected](https://github.com/OpenGPTX/lm-evaluation-harness/tree/main/lm_eval/tasks/opengptx). The exact commands to reproduce benchmark scores measured by authors are however missing, and have to be reconstructed. 

A more severe issue is what we might call "benchmark washing". In attempt to claim performance matching strong reference models, [tables are provided](https://arxiv.org/abs/2410.03730) which show benchmark scores averaged over a large number of languages, which some of the reference models they compare to most probably have not seen during training at all. By averaging, the total score of strong reference models that are known to perform very well on English and other wide-spread European languages (eg German, French, Spanish) goes down, while Teuken models that do not compare well on English manage to catch up. This creates an illusion of performance match to strong reference models.

Averaged benchmark scores are used in all public communication about Teuken, putting forward claims of favorable comparison with strong reference models. Tables reporting single languages scores, including English, that reveal that Teuken is lagging behind strong reference models (e.g. [Llama 3 8B](https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct), [Mistral-7B](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.3)) an European models (e.g. [Salamandra](https://huggingface.co/BSC-LT/salamandra-7b-instruct), [Occiglot](https://huggingface.co/occiglot/occiglot-7b-eu5-instruct)) are placed in the Appendix of the paper and are hard to discover, while the main text emphasizes claimed performance match based on average scores (eg Table 2-4). For instance, Table 18 of the Appendix reveals that Teuken lags behind strong reference models in English, and Table 16 shows also wide gap in performance on German (ostensibly Teuken's strength). Single-language benchmarks do not capture these nuances, obscuring the fact that it is clear that Teuken can only come somewhat close to reference models on average score due to some few languages that are too exotic for other reference models.

This is highly misleading for the public, and can be considered as "benchmark washing", as the scores and model comparison reported in the foreground do not reveal the actual model standing properly. Such score averaging is also used by other European initiatives, eg EuroLLM, however they report single language results clearly in the main paper section and do not overclaim the obtained results, avoiding invoking the wrong impression.
-->

### Licenses
OpenGPT-X claims their model data are processed and stored in a way which is [in line with European standards for data storage and processing](https://www.iuk.fraunhofer.de/en/news-web/2024/teuken-7b--multilinguales-open-source-sprachmodell-veroeffentlic.html). For a European AI initiative these data transparency principles are essential to follow. However, given the previously documented lack of data transparency it is difficult to verify this. A particularly thorny issue here is the inheritance of usage restrictions of licenses of dataset that were used in model training. Examining only the subset of used datasets that we could verify (see table), we found that this portion of [the model datasets used for base model training](https://arxiv.org/pdf/2410.08800) contains a variety of datasets licensed under various non-permissive licenses. Ultimately it remains unclear whether the two published models were trained on data covered by these licenses. Full transparency would alleviate doubts of whether the model adheres with the claimed data standards and was exclusively trained on appropriately licensed data. Notably, the choice to go ahead and publish the model weights provides an easy way out to deliver a working model without having to clarifying the underlying training data licensing situation. This is an example of a widely used practice in the field that nonetheless has a clear adverse impact on the open source AI community.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: OLMo
---
::

Table: Allen AI's OLMo, a model that fairs better than Teuken when it comes to openness standards, for reference.

## Community impact

_Impact on the research community._ The documented lack of data transparency and model openness has consequences for any party using or building on it. Other models building on Teuken would, [similar to Mistral- and Llama-based models](https://dl.acm.org/doi/10.1145/3630106.3659005), inherent its shortcomings. Truly open models can only be built on truly open foundations. [Large and publicly-funded model publishers that actively invite others to adopt and build on their technology](https://www.iais.fraunhofer.de/en/business-areas/speech-technologies/conversational-ai/opengpt-x.html) have a responsibility to provide (base) models that meet the highest possible transparency and openness standards. In the event of widespread adoption in research and development, the lack of openness of OpenGPT-X would negatively affect the openness standards of any study it is part of or project that builds on it.

_Impact on public perception._ OpenGPT-X's own press releases and media coverage paint a rosy picture. Teuken is described as [a fully open source model](https://opengpt-x.de/en/) which [handles data in line with European regulations](https://www.iuk.fraunhofer.de/en/news-web/2024/teuken-7b--multilinguales-open-source-sprachmodell-veroeffentlic.html). Given the limited reproducibility, however, these claims must be taken with a grain of salt. Though some observations regarding model openness are promising, we conclude that the two published models and related technologies (e.g. the published tokenizer) do not warrant the label full open source. We conclude that, when it comes to model openness, the Teuken models are not on par with ideal openness standards.

_Impact on companies._ The Teuken models claim to offer [better control over the technology used](https://www.ki.nrw/en/opengpt-x-research-project-publishes-large-ai-language-model-european-alternative-for-business-and-science-fraunhofer-iais/) while allowing for [optimizing models to specific use cases](https://www.iais.fraunhofer.de/en/business-areas/speech-technologies/conversational-ai/opengpt-x.html). In this regard, we concur with the model authors, as the model provides a sufficient base for developing proprietary company applications. However, given the better performance of [other open-weights LLMs](https://huggingface.co/spaces/openGPT-X/european-llm-leaderboard), also in multi-lingual scenarios, we do not see a strong use case for Teuken over other open-weight models.

<!--
### Impact on GAIA-X
OpenGPT-X is indirectly funded by the GAIA-X project, which seeks to deliver European open data infrastructure. To this end, it seeks to contribute to providing models which are [GDPR-compliant and which conform to EU regulations](https://gaia-x-hub.de/en/funding-projects/). The project has certainly delivered some steps in providing this, as it is delivering models which could be used to increase digital sovereignty. A main challenge, however, lies in using these models to further build towards data-sovereign infrastructure, as they can only be used for fine-tuning, while their performance is lagging far behind state-of-the-art open-weights models.
-->
_Impact on the EU LLM ecosystem._ Within the European LLM ecosystem, OpenGPT-X is a relatively large player, but other similar initiatives exist. **Salamandra** by the Barcelona Supercomputing Center provides simlilar capabilities and is trained on data from 35 different European languages. **EuroLLM** developed by the large-scale UTTER project is another multilingual LLM with similar aims to Teuken. **Occiglot** and **Pharia** are another two large language models with similar aims. The niche that the Teuken model fills in relation to these  models is its greater focus on German as a primarily language, and its design for specialist applications. Though Teuken has a place within this broader ecosystem, it remains to be seen to what degree the model is able to strengthen European innovation and competitiveness, [as is its aim](https://gaia-x-hub.de/en/funding-projects/). A promising step into this direction is that OpenGPT-X has also published its own [OpenGPT-X European LLM leaderboard](https://huggingface.co/spaces/openGPT-X/european-llm-leaderboard), which has seen some community uptake.

### Conclusion
Teuken models cannot be considered fully open source. This is reflected in [the model's current position in the European Open Source AI index](https://osai-index.eu/model/Teuken), where the limitations of its openness are documented on a running basis. Currently, the model lacks important elements that enable reproducibility, a key element of true open source. As the model authors rightfully claim,  ["it is crucial that the technology and expertise to build these models is democratized to enable different communities and organizations to employ these models for their use cases."](https://arxiv.org/pdf/2410.03730)

OpenGPT-X has been marketed as a European model [that rivals DeepSeek](https://www.wiwo.de/unternehmen/mittelstand/gipfeltreffen-der-weltmarktfuehrer-wir-muessen-uns-beim-thema-ki-keine-sorgen-machen/30201276.html). Based on our investigation, we conclude that Teuken is indeed comparable to DeepSeek in at least one regard: in terms of transparency.

::the-index
---
hideFilters: true
filters: 
  models: Teuken, deepseek-v3
---
::
