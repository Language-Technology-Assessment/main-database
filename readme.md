# How to contribute 

Every system is a separate yaml file. The first few fields contain basic metadata about the system/model, the rest of the file is a set of triples of `_class`, `_link` and `_notes`. Class can be one of three values: 🟩 open, 🟧 partial or 🟥 closed (leave empty to signify NA). Link is a URL providing evidence for the openness classification. Notes provide context and reasoning for the classification.

You're free to build on this work and reuse the data. It is licensed under CC-BY 4.0, with the stipulation that attribution should come in the form of a link to http://osai-index.eu and a citation to the paper in which the dataset & criteria are published:

> Liesenfeld, Andreas, and Mark Dingemanse. 2024. ‘Rethinking Open Source Generative AI: Open-Washing and the EU AI Act’. In _The 2024 ACM Conference on Fairness, Accountability, and Transparency_ (FAccT ’24), 1774–87. Rio de Janeiro, Brazil: ACM. doi:[10.1145/3630106.3659005](https://doi.org/10.1145/3630106.3659005).

# Which models are included?

The index aims to include any *instruct-tuned generative AI system or model* that is described by the responsible organisation or builder as "open-source" or "open", or that is marketed as such by offical outlets of the responsible organisation or builder. Generally, the index aims to:

- refer to the model by its most recent version, without naming the model size. Evaluation is then based around the largest model in the family. This may skip over some nuances with how different sizes might use different base models and fails to capture how models have evolved over time.

- the index is periodially updated by our small team (or community contributers!) to capture how models and the information supplied related to them evolve. For instance, as new models first get released and then get preprints, related 'preprint' and 'paper' entries may be updated in due course.

- models spanning across different modalities may be includes in more than one modality category (text; image; video etc) leading to multiple entries in the index.

# Openness Criteria and system information
For each model, the yaml files in this database collect (1)some general information about the system, (2) about the organization behind it, (2) and about 14 dimension of openness. The below list spells out for the openness criteria for features in the areas of system information and organisation, followed by openness criteria groupt into 'Availability', 'Documentation' and 'Access'. Use these guidelines to document determinations of openness levels as precisely as possible, including links to evidence. Notes are optional.

## **System**

    name: Name of the model including eventual version number or size indication, e.g. Llama 3.1 or Olmo-7B-instruct
    
    link: Link to official model publisher website or, if that does not exist, platform hosting the model.

    type: Model type in one word, e.g. text, video, audio. Multiple keywords possible.
    
    basemodelname: If applicable, name of base model ("foundation model") that was used.

    endmodelname: Name of the model the enduser interacts with.
    
    endmodellicense: License that applies to enduser interaction with the model.

    releasedate: Earliest release date of the model through any offical source, in YYYY MMM format, e.g. 2024 NOV.

## **Organisation**

    name:  Organisation that released the model. Usually synonymous with model builder.

    link: Link to offical source of information about model release, e.g. offical website or blog.

## **Availability**

**Datasources Basemodel**

Are datasources for training the base model comprehensively documented and freely made available? 
  
    🟥 Training data sources of base large language model are not open for inspection or shared.
    
    🟧 Some of the training data sources of base large language model are open for inspection or shared.
    
    🟩 All training  data sources of base large language model are not open for inspection or shared.

**Datasources Endmodel**

Are datasources for training the model that the enduser interacts with comprehensively documented and freely made available? 

    🟥 Training data sources of the end model are not open for inspection or shared.
    
    🟧 Some of the training data sources of end large language model are open for inspection or shared.
    
    🟩 All training  data sources of end large language model are not open for inspection or shared.

**Weights basemodel**

Are the weights of the base models made freely available?

    🟥 Weights of the base model are not shared.
    
    🟧 Weights of the base model are partially/not fully shared.
    
    🟩 Weights of the base model are shared.

**Weights endmodel**

Are the weights of the model that the enduser interacts with made freely available?

    🟥 Weights of the user-facing end model are not shared.
    
    🟧 Weights of the user-facing end model are partially/not fully shared.
    
    🟩 Weights of the user-facing end model are shared.

 **Training Code**
 
 Is the source code of datasource processing, model training and tuning comprehensively and freely made available?

    🟥 No source code available.
    
    🟧 Some source code is open.
    
    🟩 Project source code openly available and fully open available for inspection.

## **Documentation**

**Code Documentation**

Is the source code of datasource processing, model training and tuning comprehensively documented?
   
    🟥 Code documentation not available.
    
    🟧 Some components of the system features code documentation, but not every step of base and/or end model training and tuning  is documented (irrespective of whether these components are shared).
    
    🟩 All components of the system features a comprehensive code documentation.

**Hardware Architecture Documentation**

Is the hardware architecture used for datasource processing and model training comprehensively documented?

    🟥 System architecture and model training setup are not documented.
    
    🟧 System architecture and model training setup is partially documented.
    
    🟩 System architecture and model training setup is fully documented.

**Preprint**

Are archived preprint(s) are available that detail all major parts of the system including datasource processing, model training and tuning steps?

    🟥 No archived preprint(s) available.
    
    🟧 Archived preprint(s) that detail some parts of the system including datasource processing, model training and tuning steps.
    
    🟩 Archived preprint(s) are available that detail all major parts of the system including datasource processing, model training and tuning steps.

**Paper**

Are peer-reviewed scientific publications available that detail all major parts of the system including datasource processing, model training and tuning steps?

    🟥 No peer-reviewed paper(s) available.
    
    🟧 Peer-reviewed paper(s) detail parts of the software including base models, fine-tuning, or RLHF components.
    
    🟩 Peer-reviewed paper(s) are available that cover all parts of the software including base models, fine-tuning, and RLHF components.

**Model card**

Is a model card in standardized format available that provides comprehensive insight on model architecture, training, fine-tuning, and evaluation are available?

    🟥 Model card(s) not available.
    
    🟧 Model card(s) that provide partial insight on model architecture, training, fine-tuning, and evaluation are available.
    
    🟩 Model card(s) are available that provide comprehensive insight on model architecture, training, fine-tuning, and evaluation are available.

**Datasheet**

Is a datasheet as defined in "Datasheets for Datasets" (Gebru et al. 2021) available?

    🟥 Datasheet(s) are not available.
    
    🟧 Datasheet(s) that provide partial insight on data collection and curation are available.
    
    🟩 Datasheet(s) are available that provide comprehensive insight on data collection and curation are available following the standards defined in [Datasheets for Datasets](https://doi.org/10.1145/3458723) by Gebru et al. (2021)


## **Access methods**

**Package**

Is a packaged release of the model available on a software repository (e.g. a Python Package Index, Homebrew)?

    🟥 No index software package is available.
    
    🟧 User-oriented code or web-interface is available but not as a versioned package.
    
    🟩 A packaged release of the model available on a software repository is available (e.g. a Python Package Index, Homebrew).


**API**

Is an API available that provides unrestricted access to the model (other than security and CDN restrictions)?

    🟥 No API access.
    
    🟧 Commerial or restricted-access user API is available.
    
    🟩 An API available that provides unrestricted access to the model (other than security and CDN restrictions).

    
**Licenses**

Is the project fully covered by Open Source Initiative (OSI)-approved licenses, including all data sources and training pipeline code?

    🟥 The project is not licensed clearly or does not use an Open Source Initiative (OSI)-approved license.
    
    🟧 Only parts of the model and data sources are released under an  Open Source Initiative (OSI)-approved license, such as model weights.
    
    🟩 The project is fully covered by Open Source Initiative (OSI)-approved license, including all data sources and training pipeline code.
