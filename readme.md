# How to contribute 

Every project is a separate yaml file. The first few fields contain basic metadata about the model, the rest of the file is a set of triples of `_class`, `_link` and `_notes`. Class can be one of three values: 🟩 open, 🟧 partial or 🟥 closed (leave empty to signify NA). Link is a URL providing evidence for the openness classification. Notes provide context and reasoning for the classification.

You're free to build on this work and reuse the data. It is licensed under CC-BY 4.0, with the stipulation that attribution should come in the form of a link to http://opening-up-chatgpt.github.io and a citation to the paper in which the initial dataset & criteria were published:

> Andreas Liesenfeld, Alianda Lopez, and Mark Dingemanse. 2023. Opening up ChatGPT: Tracking openness, transparency, and accountability in instruction-tuned text generators. In _Proceedings of the 5th Conference on Conversational User Interfaces (CUI ’23)_, July 19–21, 2023, Eindhoven, The Netherlands.


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

**datasources_basemodel**
  
    🟥 Training data sources of base large language model are not open for inspection or shared.
    
    🟧 Some of the training data sources of base large language model are open for inspection or shared.
    
    🟩 All training  data sources of base large language model are not open for inspection or shared.

**datasources_endmodel**

    🟥 Training data sources of the end model are not open for inspection or shared.
    
    🟧 Some of the training data sources of end large language model are open for inspection or shared.
    
    🟩 All training  data sources of end large language model are not open for inspection or shared.

**weights_basemodel**

    🟥 Weights of the base model are not shared.
    
    🟧 Weights of the base model are partially/not fully shared.
    
    🟩 Weights of the base model are shared.

**weights_endmodel**

    🟥 Weights of the user-facing end model are not shared.
    
    🟧 Weights of the user-facing end model are partially/not fully shared.
    
    🟩 Weights of the user-facing end model are shared.

 **trainingcode**

    🟥 Project is closed source code.
    
    🟧 Some source code is open.
    
    🟩 Project source code openly available and fully open available for inspection.

## **Documentation**

**Code**
 
    🟥 Code documentation not available.
    
    🟧 Some components of the project features code documentation.
    
    🟩 All components of the project features a comprehensive code documentation.

**Architecture**

    🟥 System architecture and model training setup are not documented.
    
    🟧 System architecture and model training setup is partially documented.
    
    🟩 System architecture and model training setup is fully documented.

**Preprint**

    🟥 No archived preprint(s) available.
    
    🟧 Archived preprint(s) that detail parts of the software including base models, fine-tuning, or RLHF components are available.
    
    🟩 Archived preprint(s) are available that cover all parts of the software including base models, fine-tuning, and RLHF components.

**Paper**

    🟥 No peer-reviewed paper(s) available.
    
    🟧 Peer-reviewed paper(s) detail parts of the software including base models, fine-tuning, or RLHF components.
    
    🟩 Peer-reviewed paper(s) are available that cover all parts of the software including base models, fine-tuning, and RLHF components.

**Model card**

    🟥 Model card(s) not available.
    
    🟧 Model card(s) that provide partial insight on model architecture, training, fine-tuning, and evaluation are available.
    
    🟩 Model card(s) are available that provide comprehensive insight on model architecture, training, fine-tuning, and evaluation are available.

**Datasheet**

    🟥 Datasheet(s) are not available.
    
    🟧 Datasheet(s) that provide partial insight on data collection and curation are available.
    
    🟩 Datasheet(s) are available that provide comprehensive insight on data collection and curation are available.


## **Access methods**

**Package**

    🟥 No index software package is available.
    
    🟧 User-oriented code or web-interface is available but not as a versioned package.
    
    🟩 A packaged release of fully open-source software (e.g. a Python Package Index, Homebrew) is available.


**API**

    🟥 No API access.
    
    🟧 Commerial or restircted-access user API is available.
    
    🟩 An open API available that provides unrestricted access to the text generator (other than security and CDN restrictions).

    
**Licenses**

    🟥 The project is not licensed clearly or does not use an Open Source Initiative (OSI)-approved license.
    
    🟧 Only parts of the model and data sources are released under an  Open Source Initiative (OSI)-approved license, such as model weights.
    
    🟩 The project is fully covered by a true Open Source Initiative (OSI)-approved license, including all data sources and training pipeline code.
       

