---
title: Data sources
description: Finding and sharing data for human biomolecular related data sources.
contributors: []
page_id: hbd_data_sources
rdmkit:
  - name: Human Data
    url: https://rdmkit.elixir-europe.org/human_data
  - name: Sensitive Data
    url: https://rdmkit.elixir-europe.org/sensitive_data
  - name: Biomolecular simulation data  
    url: https://rdmkit.elixir-europe.org/biomolecular_simulation_data
  - name: Data transfer
    url: https://rdmkit.elixir-europe.org/data_transfer
related_pages: 
  showcase: []
  human_biomolecular_data: [hbd_data_description]
  human_clinical_and_health_data: [hchd_data_sources, hchd_data_description]
  socioeconomic_data: []
  pathogen_characterisation: []
training:
  - name:
    registry:
    url:
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction

This document aims to serve as a comprehensive resource for anyone interested in the data sources platforms of infectious diseases using human biomolecular data, which have become increasingly important in recent years as a result of advancements in technology and the ever-growing threat of global pandemics. 

By providing this overview of the data sources platforms of infectious diseases using human biomolecular data, this document aims to facilitate the development of new research initiatives and collaborations in the field.


### What is human biomolecular data, and why is it important for infectious diseases research?

Human biomolecular data refers to information obtained from the analysis of biological molecules, such as DNA, RNA, proteins, and metabolites. This type of data is used to study the molecular mechanisms underlying disease and to identify potential drug targets.

Human clinical data, on the other hand, refers to information obtained from the study of patients, including their medical histories, physical exams, and laboratory tests. This type of data is used to diagnose and treat disease, as well as to evaluate the safety and efficacy of new therapies.

While both types of data are important for understanding human health and disease, they are collected and analysed in different ways and for different purposes.

Human biomolecular data is of great importance in infectious disease research because it plays a critical role in understanding the molecular basis of the disease. By analyzing the biomolecular data, researchers can gain a deeper understanding of the disease's pathogenesis, evolution, and transmission. Personalised medicine is another area where biomolecular data can be applied. By analyzing an individual's biomolecular data, researchers can develop personalised treatment plans that are tailored to the specific needs of the patient. For example, if a patient has a genetic mutation that predisposes them to a particular disease, this information can be used to develop a personalised treatment plan that takes into account the patient's genetic profile.

<!-- ## Data deposition and FAIRness -->

<!--- Currently in standby waiting to check the clinical data sources FAIRness.--->

<!-- ### Considerations -->

## Search and discoverability

Search and discoverability are crucial for finding and accessing relevant information, resources, and data related to a specific topic or area of interest, particularly in the context of infectious diseases. Infectious diseases can evolve rapidly and have significant impacts on public health, making it necessary to monitor and respond to outbreaks effectively. This requires access to up-to-date information on disease prevalence, transmission patterns, and clinical outcomes, which can come from various sources, such as clinical data, biomolecular data, public health reports, and social media.

Search and discoverability is crucial in infectious disease surveillance because it enables public health professionals and researchers to quickly find and access relevant data sources. This can help them identify emerging disease threats, monitor the spread of disease, and make informed decisions about disease control measures. Without effective search and discoverability, there can be delays in identifying outbreaks and responding to them, leading to increased spread of disease and negative impacts on public health.

Standardised terminology and data formats are also essential for effective search and discoverability in infectious disease surveillance. The use of common disease codes and data structures can facilitate the integration and analysis of data from multiple sources, making it easier to identify trends and patterns. This can improve the ability to identify emerging disease threats and develop effective disease control measures. See [Data harmonisation](#data-harmonisation) section.

Biomolecular data is also critical for understanding the molecular basis of infectious diseases and developing effective diagnostic and treatment strategies. This includes genetic and molecular data related to the pathogen and its interactions with the host. The search and discoverability of biomolecular data sources can be facilitated through the use of standardised data formats and data sharing platforms. This can improve the ability to develop effective diagnostic and treatment strategies for infectious diseases, ultimately protecting the health and wellbeing of individuals and communities.

Overall, search and discoverability are essential for effective infectious disease surveillance and response. By ensuring that relevant data sources are easily accessible and usable, public health professionals can more effectively monitor and control the spread of infectious diseases, ultimately protecting public health.

### Considerations

Despite the growing amount of infectious disease data stored in various sources, finding and analyzing this data can be challenging for the scientific community. There is a clear need for a user-friendly and efficient way to discover and analyse this data.

- *Data sharing platforms*: Access to data sharing platforms can facilitate the discovery and sharing of biomolecular data related to infectious diseases. Such as the [Covid19 DataPortal](https://www.covid19dataportal.org/).
- *Data privacy and security*: Privacy and security protocols must be in place to protect sensitive biomolecular data from unauthorised access.
- *Data quality*: High-quality biomolecular data is critical for accurate disease surveillance, diagnosis, and analysis. Efforts should be made to ensure that data quality is maintained throughout the data lifecycle. See [Human biomolecular data - Quality control](https://www.infectious-diseases-toolkit.org/human-biomolecular-data/quality-control) page.
- *Data storage and management*: Proper data storage and management practices must be followed to ensure that biomolecular data is organised and easily accessible to relevant parties.
- *Metadata*: Metadata should be included with biomolecular data to provide context and facilitate search and discoverability.
- *Collaboration*: Collaboration between data producers, curators, and users can promote effective search and discoverability of biomolecular data related to infectious diseases.
- *Data standardization*: Standardised data formats and common disease codes are essential for integrating and analyzing biomolecular data from different sources.

### Existing approaches

Consequently, we have compiled some of the main tools, portals, and data sharing platforms that allow for searching and discovering biomolecular data related to infectious diseases from various sources with the next considerations.

- Beacon v2: Beacon is an API (usually extended with a user interface) that allows for data discovery of phenoclinic and biomolecular data. The version 2 (v2) of the Beacon protocol has been accepted as GA4GH standard in Spring 2022. It includes, among other changes:
  - Query options for biological or technical metadata using filters defined through CURIEs (e.g. phenotypes, disease codes, sex or age).
  - An option to trigger the next step in the data access process (e.g. who to contact or which are the data use conditions).
  - An option to jump to another system where the data could be accessed (e.g. if the Beacon is for internal use of the hospital, to provide the Id of the EHR of the patients having the mutation of interest).
  - Annotations about the variants found, among which the expert/clinician conclusion about the pathogenicity of a given mutation in a given individual or its role in producing a given phenotype.
  - Information about cohorts.

  Useful links related to Beacon v2:
  - [Beacon v2 Website](https://beacon-project.io)
  - [Beacon v2 Models](https://docs.genomebeacons.org/models/)
  - [Beacon v2 GitHub](https://github.com/ga4gh-beacon/beacon-v2/)
  - [Beacon v2 GitHub API](https://github.com/EGA-archive/beacon2-ri-api)
  - [Beacon v2 Reference Implementation paper](https://academic.oup.com/bioinformatics/article/38/19/4656/6671215)

  Example of Beacon v2 with synthetic data:
  - [Synthetic data (CINECA)](https://ega-archive.org/studies/EGAS00001002472)
  - [CINECA Beacon v2 API](https://ega-archive.org/beacon-apis/cineca/)
  - [CINECA Beacon v2 Training-UI](http://18.169.16.40:9000/)

- Biosamples: [BioSamples](https://www.ebi.ac.uk/biosamples/) stores and supplies descriptions and metadata about biological samples used in research and development by academia and industry. For example it stores data from infectious diseases such as COVID-19.
- COVID-19 DataPortal: The European COVID-19 Data Platform facilitates data sharing and analysis in order to accelerate coronavirus research and acts as a Data sharing platform. The European COVID-19 Data Platform consists of three connected components:
  - [SARS-CoV-2 Data Hubs](https://www.covid19dataportal.org/data-hubs), which organise the flow of SARS-CoV-2 outbreak sequence data and provide comprehensive open data sharing for the European and global research communities.
  - [Federated European Genome-phenome Archive](https://www.covid19dataportal.org/federated-ega), which provides secure controlled access sharing of sensitive patient and research subject data sets relating to COVID-19.
  - [COVID-19 Data Portal](https://www.covid19dataportal.org/), which brings together and continuously updates relevant COVID-19 datasets and tools, will host sequence data sharing and will facilitate access to other SARS-CoV-2 resources.

  You can find further information about the Covid-19 Data Portal in the link [here](https://rdmkit.elixir-europe.org/covid19_data_portal).

## Data access and transfer

Sharing genetic and molecular information between researchers and institutions is essential for gaining a better understanding of human biology and disease. This is especially important when it comes to infectious diseases. By studying the genetic makeup of pathogens and how they interact with human cells, researchers can identify new targets for treatments and vaccines. They can also develop strategies to prevent or contain potential outbreaks before they occur.

Of course, sharing this kind of sensitive information comes with challenges. Privacy, security, and ethical considerations must be taken into account. Researchers need to handle this information responsibly and with respect for individuals' rights. Legal and regulatory barriers can also impede data sharing and collaboration.

However, the benefits of sharing human biomolecular data outweigh the risks. Access to this data is crucial for scientific progress and medical advancements. It's important for us to continue finding ways to responsibly and securely share this valuable resource. Let's work together to make sure that we do so while respecting everyone's rights and ensuring that data is kept safe and secure.

### Considerations

When looking for solutions to human biomolecular data access, you should consider the following aspects:
- Check with your institution that you are following the ethical and legal requirements.
- Deposit your data in a controlled access repository
- Ensure that the data use conditions are publicly available to ease the data access process
- Assemble your Data Access Committee to process data access requests

When looking for solutions to data transfer, you can check [this](https://rdmkit.elixir-europe.org/data_transfer) documentation.

### Existing approaches

- You can check a list of existing controlled access repositories below.
  - [European Genome-phenome Archive](https://ega-archive.org/)
  - [Estonian BioBank](https://genomics.ut.ee/en/content/estonian-biobank)
  - [Dutch Covid-19 Data Portal](https://covid19initiatives.health-ri.nl/p/Dashboard) 
  - [PANTHER](https://pantherstudy.org.uk/) 
  - [ACE](https://co-connect.ac.uk/ace-cohort/)
- You can use one of these standards to make your data use conditions publicly available to possible data requesters.
  - The [GA4GH Data Use Ontology DUO](https://github.com/EBISPOT/DUO) is an international standard, which provides codes to represent data use restrictions for controlled access datasets.
  - The [Automatable Discovery and Access Matrix (ADA-M)](https://github.com/ga4gh/ADA-M) provides a standardised way to unambiguously represent the conditions related to data discovery and access. 
  - By depositing your data to one of the existing controlled access repositories, they will already show the data use conditions (e.g. [EGAD00001007777](https://ega-archive.org/datasets/EGAD00001007777))
- A data access committee (DAC) is a group responsible for reviewing and approving requests for access to sensitive data, such as human biomolecular data. Its role is to ensure that requests are in compliance with relevant laws and regulations, that data is being used for legitimate scientific purposes, and that privacy and security are being maintained. 

You can find further information about sharing human data [here](https://rdmkit.elixir-europe.org/human_data#sharing-and-reusing-of-human-data).

## Data harmonisation

To ensure that researchers can effectively utilise data, it is essential that it be collected and stored in a standardised manner. Using standardised formats and databases facilitates data sharing across research groups, enabling more efficient and effective analysis. This approach not only saves time, but also yields more accurate results.

It is important to note that there are currently no specific standards and schemes for biomolecular data focused on infectious diseases. Nevertheless, thanks to the Sars-CoV-2 outbreak, the scientific community has established standards, schemes, and data models with controlled vocabularies and ontologies explained in detail in the Human Clinical and Health Data section.

### Considerations

- Looking for an existing standardised metadata schema for human biomolecular data, like [MIABIS](https://github.com/BBMRI-ERIC/miabis) or [EGA](https://ega-archive.org/submission/sequence/programmatic_submissions) schemas. 
- Incorporating key data elements such as patient demographics, clinical features, and laboratory test results in the metadata schema
- Ensuring interoperability with other existing metadata schemas to facilitate data sharing and integration
- Including metadata fields for sample collection, processing, and storage information to ensure data quality and reproducibility
- Implementing controlled vocabularies and ontologies for standardised annotation and data integration
- Enabling data harmonisation across different studies to facilitate meta-analyses and systematic reviews
- Seek input and feedback from stakeholders across the research and public health communities to ensure that the schema meets the needs of diverse users and supports a range of research questions and applications.
- Regularly updating and refining the metadata schema to accommodate new data types and emerging research needs.

### Existing approaches

When looking for solutions to standards, schemas, ontologies and vocabularies, you can check [this](https://rdmkit.elixir-europe.org/metadata_management#how-do-you-find-appropriate-standard-metadata-for-datasets-or-samples) documentation.