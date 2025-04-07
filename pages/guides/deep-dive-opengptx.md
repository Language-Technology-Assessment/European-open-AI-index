---
title: "Deep Dive: OpenGPT-X"
description: Digging into OpenGPT-X's Teuken models
date: 2025-03-24
author: Dick Blankvoort & Jenia Jitsev
status: published
---
# Deep Dive: OpenGPT-X
<author :author="author"></author>

### Introduction
[The OpenGPT-X initiative](https://opengpt-x.de/en/) is an organization seeking to create open-source AI models 'Made in Germany'. In this first of a series of blog posts, we evaluate its flagship [Teuken](https://opengpt-x.de/models/teuken-7b-de/) models through the lens of open-source. In collaboration with Jenia Jitsev of LAION and JSC, we explore some of the project's strengths and weaknesses. In general, we demonstrate that even though the OpenGPT-X initiative claims to be developing fully open-source models, there is a dissonance between the claims made and their actual capabilities.

<!--## Openness
The model developed by OpenGPT-X is known as [Teuken](https://opengpt-x.de/models/teuken-7b-de/). Teuken is billed as providing "multilingual, open source models for Europe". We evaluate the "open source" claim of the model by looking into data availability, availability of model weights, and licensing, particularly focusing on how the claims made surrounding the model compare to the implementation of the model itself.-->

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: Teuken
---
::

### Model data
The Teuken models are described as being pretrained on ["data from publicly available sources"](https://huggingface.co/openGPT-X/Teuken-7B-instruct-research-v0.4/blob/main/README.md), with [openness being marketed as a key feature](https://opengpt-x.de/en/about/). As such it is good to verify these claims, investigating whether the model data is indeed as open as is purported. 

The data used to train the base model of the Teuken series originates from two sources; the [FineWeb-Edu dataset](https://huggingface.co/datasets/HuggingFaceFW/fineweb-edu) and a [private dataset](https://arxiv.org/pdf/2410.08800) constructed by OpenGPT-X itself. The FineWeb-Edu dataset is widely available and used as pretraining data in over 200 models. The private data mixture, on the other hand, has a number of qualities which make obtaining insight into it challenging.

A first observation is that no downloadable version of the full dataset is publicly available. This means that any entity seeking to use the dataset must either reproduce it themselves or request it from the model authors. Although this is fairly standard practice, it does pose challenges to transparency and makes it difficult to reconstruct the model.

Secondly, reconstruction is further hampered by a lack of a clear and open source codebase that documents the processes of data collection, curation, filtering and processing. The model does offer a preprint documenting at least some elements of the data pipeline. Within this preprint, however, even though the sources used for constructing the data mixture are shared, this is not done in sufficient detail to make reproduction feasible. See the following table for a selection of problematic data sources. 

<table>
  <tr>
    <th>Data source</th>
    <th>Reason for highlighting</th>
  </tr>
  <tr>
    <td>Corpus of Contemporary Irish</td>
    <td><a href="https://www.gaois.ie/en/corpora/monolingual">Replaced by newer dataset</a></td>
  </tr>
  <tr>
    <td>medi_notice dataset, Swiss Legislation Corpus</td>
    <td><a href="https://pub.cl.uzh.ch/wiki/public/pacoco/medi-notice">Inaccessible without a University of Zürich account</a></td>
  </tr>
  <tr>
    <td>Open Legal Data German court decisions</td>
    <td><a href="https://openlegaldata.io/research/2019/02/19/court-decision-dataset.html">Listed twice with different word and document count</a></td>
  </tr>
  <tr>
    <td>Norwegian Colossal Corpus</td>
    <td><a href="https://huggingface.co/datasets/NbAiLab/NCC">Newspapers removed after model release</a></td>
  </tr>
  <tr>
    <td>Various subsets of The Pile</td>
    <td><a href="https://pile.eleuther.ai/">No subsets provided, only The Pile and (for some subsets) scrapers</a></td>
  </tr>
  <tr>
    <td>PRINCIPLE bilingual English-Irish datasets</td>
    <td><a href="https://elrc-share.eu/repository/search/?q=PRINCIPLE&selected_facets=languageNameFilter_exact%3AIrish">Not clear which datasets were taken</a></td>
  </tr>
  <tr>
    <td>Unknown Slovak Dataset</td>
    <td><a href="https://nlp.ffzg.unizg.hr/resources/corpora/slwac/">404 Error</a></td>
  </tr>
  <tr>
    <td>Swiss Policy Documents</td>
    <td><a href="https://opendata.swiss/en/dataset?keywords_en=environmental--policy&keywords_en=policy-analysis">Links to a search query with a single result</a></td>
  </tr>
  <tr>
    <td>Various Wikimedia sites</td>
    <td><a href="https://en.wikipedia.org/wiki/Main_Page">Link to sites, not datasets</a></td>
  </tr>
</table>

The sources listed include 404 pages, pages inaccessible without a specific university account, and links to sites without specific directions on versioning and access methods. Without an exhaustive list of data sources and clarity on data processing procedures, it is not feasible to reproduce the training procedure.

Lastly, as mentioned [in the model paper](https://arxiv.org/pdf/2410.03730), the data mixture is further adapted before being used for pretraining. This includes strategic downsampling of English data and upsampling of data in foreign languages. No information is available on the upsampling and downsampling beyond this single statement.

<!--The limited availability of several of the sources also belies the claim that Teuken was pretrained on ["data from publicly available sources"](https://huggingface.co/openGPT-X/Teuken-7B-instruct-research-v0.4/blob/main/README.md). The lack of reproducibility of the base model data, meanwhile, runs counter to claims that [openness is a key feature of the models developed by OpenGPT-X](https://opengpt-x.de/en/about/).-->

The data processing paper of Teuken makes mention of [saving the intermediate results of the data pipeline](https://arxiv.org/pdf/2410.08800). Making these intermediate data publicly available (or the finalized data mixture, as with [OLMo's Dolma dataset](https://huggingface.co/datasets/allenai/dolma)) would greatly contribute to the openness of the model.

Compared to the base model data mixture, the instruction-tuning mixture of Teuken is laid out quite well. As far as we can tell, all data sources are linked properly and open-source datasets are used. The instruction-tuning data could be further improved by publishing a dataset, as with [the Aya models](https://huggingface.co/datasets/CohereForAI/aya_dataset).

In general, the data used to train the Teuken models is not as open as might appear at first glance. While some elements of the dataset are known, the lack of a publicly downloadable version of the dataset and thorough documentation of data sources makes it difficult to verify claims made.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: OLMo, Command-R
---
::

### Model weights
Teuken [claims to be open-source](https://opengpt-x.de/en/models/teuken-7b/), a core element of which is that the weights of the model are published (open-weights). In this section, we investigate the weight availability of the Teuken model, investigating both the weights of the base (pretrained) model and the end model.

#### Base model weights

The base model weights of Teuken are available only upon request from the model authors. This uncommon approach makes it somewhat more difficult to determine model availability. We have approached the model creators to obtain the model weights, however have unfortunately not yet received a response.

<!-- It is difficult to make a definitive judgement about this treatment of the base model. There are indeed legitimate concerns regarding the potential misuse of base models, and restricting the availability of a base model is not unprecedented. However, if this is done, careful consideration must also be taken to ensure that a model remains sufficiently open. -->

#### End model weights

For the end model weights, two versions are provided on OpenGPT-X's HuggingFace page; a research model and a commercial model. Given that the paper makes no mention of such a distinction, this is rather puzzling. The model card and the organization's site claim that the research model was trained on data with a non-permissive license, while for the commercial model this data was excluded. Based on this, we assume that the commercial model excludes the part of the private data mixture that was licensed non-permissively. If this is true, it further highlights the need for data transparency to allow outside parties to verify these claims.

Given the above, the question of whether Teuken's models can be called open-weights is somewhat up in the air. Base model weights are only available upon request, while the form of the end model weights is somewhat incongruous with the model described in the paper.

### Tokenizer

One of the key innovations of the Teuken model was its use of a balanced multilingual tokenizer. This tokenizer, as the authors claim, [was crucial for bringing down training costs](https://arxiv.org/pdf/2410.03730). This makes it rather unfortunate, then, that relatively little is known about the tokenizer used, as it is only available as a bundle together with the instruction-tuned model. The [paper from which it derives](https://arxiv.org/abs/2310.08754) provides some implementation details, however does not provide guidance with regards to the data mixture. We believe that future research could greatly benefit from further information regarding the use of multilingual tokenizers, given that the results appear to be relatively impactful.

### Licenses
OpenGPT-X claims their model data are processed and stored in a way which is [in line with European standards for data storage and processing](https://www.iuk.fraunhofer.de/en/news-web/2024/teuken-7b--multilinguales-open-source-sprachmodell-veroeffentlic.html). This aim of data transparency is indeed a good principle to follow, especially for a European AI initiative. Given the previously mentioned lack of data transparency it is, however, difficult to verify this claim. At least, it seems that the curated portion of [the model's foundational dataset used for pretraining](https://arxiv.org/pdf/2410.08800) contains a variety of data listed with 'various' non-permissive licenses, and it is unknown whether the two models published were trained (partially) on data with such licenses. Further data transparency could alleviate this, so that an outside observer can more easily verify whether the model meets the claimed data standards.

### Impact on the research community
The above-discussed lack of data transparency and openness has consequences for Teuken's ability to be further built upon by the research community. Any models building upon it would, [similar to Mistral- and Llama-based models](https://dl.acm.org/doi/10.1145/3630106.3659005), necessarily suffer from an inherent lack of openness. We must not forget that openness is to a large degree transitive, and as such [any models wishing others to build upon them](https://www.iais.fraunhofer.de/en/business-areas/speech-technologies/conversational-ai/opengpt-x.html) must seek to be as open as possible.

### Impact on public perception
Claims made to the public regarding OpenGPT-X paint a rosy picture. Teuken is described as  [a fully open-source model](https://opengpt-x.de/en/) which [handles data in line with European regulations](https://www.iuk.fraunhofer.de/en/news-web/2024/teuken-7b--multilinguales-open-source-sprachmodell-veroeffentlic.html). Given the inherent challenges in reproducibility, however, these claims must be taken with a grain of salt. Though some research regarding the model is promising, both the model and its underlying technology remain challenging to adopt.

### Impact on companies
The Teuken models claim to offer [better control over the technology used](https://www.ki.nrw/en/opengpt-x-research-project-publishes-large-ai-language-model-european-alternative-for-business-and-science-fraunhofer-iais/) while allowing for [optimizing models to specific use cases](https://www.iais.fraunhofer.de/en/business-areas/speech-technologies/conversational-ai/opengpt-x.html). In this regard, we agree with the model authors, as the model provides a sufficient base for developing proprietary company applications. However, given the relatively better performance of [other open-weights LLMs](https://huggingface.co/spaces/openGPT-X/european-llm-leaderboard), a case has to be made for using the Teuken model in particular.

### Impact on GAIA-X
OpenGPT-X is funded by the GAIA-X project, which seeks to deliver European open data infrastructure. To this end, it seeks to contribute to providing models which are [GDPR-compliant and which conform to EU regulations](https://gaia-x-hub.de/en/funding-projects/). The project has certainly delivered some steps in providing this, as it is delivering models which could be used to increase digital sovereignty. A main challenge, however, lies in using these models to further build towards data-sovereign infrastructure, as they can only be used for fine-tuning.

### Impact on the EU LLM ecosystem
It is important to place Teuken within the context of the broader European LLM ecosystem. OpenGPT-X has published its own [European LLM leaderboard](https://huggingface.co/spaces/openGPT-X/european-llm-leaderboard), which can be used to contextualize the model. Below we list several initiatives which have similar goals to Teuken:
- **Salamandra** is a model developed by the Barcelona Supercomputing Center which is trained on data from 35 different European languages.
- **EuroLLM** is a multilingual LLM with similar aims to Teuken. It was developed by the UTTER project, a collaboration between several institutions. By and large EuroLLM provides similar capabilities to Teuken, although with more measured claims.
- **Occiglot** is a large language model designed to produce text in the top 5 EU languages, produced through an open research project of the same name. 
- **Pharia** is a large language model with similar claims to openness as Teuken, developed by Aleph-Alpha. For more information regarding this model, see [an earlier blog post of ours](https://osai-index.eu/news/aleph-alpha-pivot).

The main niches the Teuken model fills relative to these other models are its greater focus on German as a primarily language, and its design for specialist applications. Though Teuken has a place within this broader ecosystem, it remains to be seen to what degree the model is able to strengthen European innovation and competitiveness, [as is its aim](https://gaia-x-hub.de/en/funding-projects/).

### Conclusion
As things stand, the Teuken models cannot be considered fully open-source. This is reflected in [our rankings](https://osai-index.eu/model/Teuken), where they are positioned near the middle of the pack. The model in particular lacks reproducibility, which is a key element of proper open-source. As the authors rightly claim: ["it is crucial that the technology and expertise to build these models is democratized to enable different communities and organizations to employ these models for their use cases"](https://arxiv.org/pdf/2410.03730).

OpenGPT-X has been marketed as a European model [comparable with even DeepSeek](https://www.wiwo.de/unternehmen/mittelstand/gipfeltreffen-der-weltmarktfuehrer-wir-muessen-uns-beim-thema-ki-keine-sorgen-machen/30201276.html). Based on our investigation of openness features, we can conclude that Teuken is at least in one regard very comparable to DeepSeek.

::the-index
---
hideFilters: true
filters: 
  view: grid
  models: Teuken, DeepSeek-V3
---
::