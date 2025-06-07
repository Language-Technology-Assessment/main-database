---
title: Language Technology Assessment main database - OSAI Index
tags:
  - open-source
  - generative AI
  - catalogue
  - index
authors:
  - name: Andreas Liesenfeld
    orcid: 0000-0001-6076-4406
    affiliation: 'Centre of Language and Speech Technology, Radboud University'
  - name: Mark Dingemanse
    orcid: 0000-0002-3290-5723
    affiliation: 'Centre of Language and Speech Technology, Radboud University'
  - name: Nityaa Kalra
    orcid: 0009-0005-0958-553X
    affiliation: 'Centre of Language and Speech Technology, Radboud University'
  - name: Dick Blankvoort
    orcid: 0009-0003-0766-4678
    affiliation: 'Centre of Language and Speech Technology, Radboud University'

date: 7 June 2025
---

## Introduction

The European Open Source AI index is an EU-based community-driven public resource on open-source generative AI systems, created for the purposes of cataloguing and scrutinizing systems which claim to be open or open-source. This upload catalogues the index at a specific point in time (2025-05-12).

The index is hosted at the Centre of Language and Speech Technology at Radboud University at [osai-index.eu](osai-index.eu), and is maintained by a small team of academics and community members.

The index is based largely off the papers [Opening up ChatGPT: Tracking openness, transparency, and accountability in instruction-tuned text generators](https://dl.acm.org/doi/abs/10.1145/3571884.3604316) and [Rethinking open source generative AI: open-washing and the EU AI Act](https://dl.acm.org/doi/abs/10.1145/3630106.3659005). To this end, evaluation is done largely based on fourteen key openness criteria.

## Open-source criteria
For this index, we consider as an open-source model any model which describes itself as either 'open-source' or 'open', or for which their positioning in the open-source space makes the model's open-source nature implicit (e.g. [DeepHermes](https://huggingface.co/NousResearch/DeepHermes-3-Llama-3-8B-Preview)). We thus rely largely on a model's own claims to determine whether open-source status is sought. For each model for which a claim to openness is made, we use our evaluation criteria to determine to what degree open-source values are achieved in practice.

## File contents
For each model, the yaml files in our index collect:
(1) some general information about the model,
(2) some information about the organization behind it, and
(3) about 14 dimension of openness.

The below list spells out what each of our features contains, as well as openness criteria for openness dimensions.
- System:
  - name: Name of the model including eventual version number or size indication, e.g. Llama 3.1 or Olmo-7B-instruct
  - link: Link to official model publisher website or, if that does not exist, platform hosting the model.
  - type: Model type in one word, e.g. text, video, audio. Multiple keywords possible.
  - performanceclass: [The performance class of the model.](https://osai-index.eu/news/performance-classes)
  - basemodelname: If applicable, name of base model ("foundation model") that was used.
  - endmodelname: Name of the model the enduser interacts with.
  - endmodellicense: License that applies to enduser interaction with the model.
  - releasedate: Earliest release date of the model through any offical source, in YYYY MMM format, e.g. 2024 NOV.
- Organisation:
  - name: The organisation that released the model. Usually synonymous with the model builder.
  - link: Link to offical source of information about model release, e.g. offical website or blog.
- Datasources Basemodel - Whether data sources for training the base model are comprehensively documented and freely made available.
  - closed: Training data sources of base large language model are not open for inspection or shared.
  - partial: Some of the training data sources of base large language model are open for inspection or shared.
  - open: All training  data sources of base large language model are not open for inspection or shared.
- Datasources Endmodel - Whether datasources for training the model that the end-user interacts with are comprehensively documented and freely made available.
  - closed: Training data sources of the end model are not open for inspection or shared.
  - partial: Some of the training data sources of end large language model are open for inspection or shared.
  - open: All training  data sources of end large language model are not open for inspection or shared.
- Weights basemodel - Whether the weights of the base models are made freely available.
  - closed: Weights of the base model are not shared.
  - partial: Weights of the base model are partially/not fully shared.
  - open: Weights of the base model are shared.
- Weights endmodel - Whether the weights of the model that the end-user interacts with are made freely available.
  - closed: Weights of the user-facing end model are not shared.
  - partial: Weights of the user-facing end model are partially/not fully shared.
  - open: Weights of the user-facing end model are shared.
- Training Code - Whether the source code of datasource processing, model training and tuning is comprehensively and freely made available.
  - closed: No source code available.
  - partial: Some source code is open.
  - open: Project source code openly available and fully open available for inspection.
- Code Documentation - Whether the source code of datasource processing, model training and tuning is comprehensively documented.
  - closed: Code documentation not available.
  - partial: Some components of the system features code documentation, but not every step of base and/or end model training and tuning  is documented (irrespective of whether these components are shared).
  - open: All components of the system features a comprehensive code documentation.
- Hardware Architecture Documentation - Whether the hardware architecture used for datasource processing and model training is comprehensively documented.
  - closed: System architecture and model training setup are not documented.
  - partial: System architecture and model training setup is partially documented.
  - open: System architecture and model training setup is fully documented.
- Preprint - Whether archived preprint(s) are available that detail all major parts of the system including datasource processing, model training and tuning steps.
  - closed: No archived preprint(s) available.
  - partial: Archived preprint(s) that detail some parts of the system including datasource processing, model training and tuning steps.
  - open: Archived preprint(s) are available that detail all major parts of the system including datasource processing, model training and tuning steps.
- Paper - Whether peer-reviewed scientific publications are available that detail all major parts of the system, including datasource processing, model training and tuning steps.
  - closed: No peer-reviewed paper(s) available.
  - partial: Peer-reviewed paper(s) detail parts of the software including base models, fine-tuning, or RLHF components.
  - open: Peer-reviewed paper(s) are available that cover all parts of the software including base models, fine-tuning, and RLHF components.
- Model card - Whether a model card is available in standardized format that provides comprehensive insight on model architecture, training, fine-tuning, and evaluation.
  - closed: Model card(s) not available.
  - partial: Model card(s) that provide partial insight on model architecture, training, fine-tuning, and evaluation are available.
  - open: Model card(s) are available that provide comprehensive insight on model architecture, training, fine-tuning, and evaluation are available.
- Datasheet - Whether a datasheet as defined in ["Datasheets for Datasets"](https://doi.org/10.1145/3458723) (Gebru et al. 2021) is available.
  - closed: Datasheet(s) are not available.
  - partial: Datasheet(s) that provide partial insight on data collection and curation are available.
  - open: Datasheet(s) are available that provide comprehensive insight on data collection and curation are available following the standards defined in [Datasheets for Datasets](https://doi.org/10.1145/3458723) by Gebru et al. (2021)
- Package - Whether a packaged release of the is model available on a software repository (e.g. a Python Package Index, Homebrew).
  - closed: No index software package is available.
  - partial: User-oriented code or web-interface is available but not as a versioned package.
  - open: A packaged release of the model available on a software repository is available (e.g. a Python Package Index, Homebrew).
- API - Whether an API is available that provides unrestricted access to the model (other than security and CDN restrictions).
  - closed: No API access.
  - partial: Commerial or restricted-access user API is available.
  - open: An API available that provides unrestricted access to the model (other than security and CDN restrictions).
- Licenses - Whether the project is fully covered by Open Source Initiative (OSI)-approved licenses, including all data sources and training pipeline code.
  - closed: The project is not licensed clearly or does not use an Open Source Initiative (OSI)-approved license.
  - partial: Only parts of the model and data sources are released under an  Open Source Initiative (OSI)-approved license, such as model weights.
  - open: The project is fully covered by Open Source Initiative (OSI)-approved license, including all data sources and training pipeline code.

## Inclusion criteria

The index aims to include any instruct-tuned generative AI system or model that is described by the responsible organisation or builder as "open-source" or "open", or that is marketed as such by official outlets of the responsible organisation or builder. Generally, the index aims to:


- Refer to models by their most recent version and generally focus on the largest available version within a model family. While this approach helps streamline comparisons, it does overlook some nuances. For example, differences in licensing, architecture, or openness between model sizes or incremental updates.

- The index is periodically updated by our small team of researchers and community contributors. Updates reflect newly released models and improvements in documentation or licensing information over time. For instance, a model entry may be revised when a preprint becomes available or when a license changes.

- Models that span multiple modalities (e.g., text, image, video) may appear in more than one modality category, resulting in multiple entries in the index.


## Collection

Models are collected through a combination of manual curation and community contributions. Sources include:

- GitHub issues submitted by users
- Model lists maintained by platforms like Ollama
- Leaderboards such as LLM Arena
- Hugging Face’s most-liked models
- Ongoing individual monitoring of the generative AI landscape.

Once a model is added, it is associated with its parent organisation. New models from tracked organisations are continuously monitored, particularly through their Hugging Face profile(s) or official repositories.

## Uses

The Open Source AI Index provides a structured overview of the state of openness in the generative AI ecosystem. It is intended for researchers, policymakers, developers, and advocates seeking to assess how open various AI systems truly are beyond surface-level claims.

By cataloguing openness across different dimensions, the index supports more informed debates around transparency, reproducibility, and public accountability in AI. It can also serve as a foundation for further work in responsible AI, dataset documentation, and policy evaluation. We stand open to our data being used in future projects in the field.


## Maintenance

Responsibility for maintenance lies primarily with the Centre for Language and Speech Technology (CLST) at Radboud University. However, the project is designed to be community-driven, and contributions from the wider open-source AI community are encouraged. We aim to move towards a more decentralized maintenance model over time, enabling transparency and shared ownership of the index.
