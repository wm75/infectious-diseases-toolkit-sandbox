---
title: An automated SARS-CoV-2 genome surveillance system built around Galaxy
contributors: [Wolfgang Maier] 
description: An automated, modular system for large-scale FAIR analysis of SARS-CoV-2 sequencing data analysis powered by the Galaxy platform.
affiliations: [DE, European Union]
page_id: COVID19GalaxyProject
related_pages:
  showcase: [korogenoest]
training:
  - name: Mutation calling, viral genome reconstruction and lineage/clade assignment from SARS-CoV-2 sequencing data
    registry: TeSS
    url: https://tess.elixir-europe.org/materials/hands-on-for-mutation-calling-viral-genome-reconstruction-and-lineage-clade-assignment-from-sars-cov-2-sequencing-data-tutorial
  - name: Automating Galaxy workflows using the command line
    registry: TeSS
    url: https://tess.elixir-europe.org/materials/hands-on-for-automating-galaxy-workflows-using-the-command-line-tutorial 
---

## Introduction 

The SARS-CoV-2 pandemic has generated a demand for sequencing-based viral genome analysis at an unprecedented scale. This challenge triggered the initiation of many new sequencing initiatives, but, luckily, also a lot of activity in public compute and storage infrastructure projects and in workflow initiatives and frameworks, that such initiatives could rely on. 

Here we demonstrate how the Galaxy Project with the help of many additional collaborators leveraged and combined public infrastructure and systems for storing and sharing data and for managing data analysis workflows, to form a modular and scalable system for FAIR analysis of SARS-CoV-2 sequencing data.


## Who is the showcase intended for?

Automated Galaxy workflow runs for viral genome surveillance are of interest for any department, institution or organisation that intends to perform routine genome monitoring of virus sequences at non-trivial scale, and who cares about FAIR large-scale data analysis.


**Figure goes here**

### Alternative text
Image composed of three connected panels labelled Data Access, Data Analysis and Data Deposition & Visualization. The first panel shows the European Nucleotide Archive as the source of the data that gets pulled into Data Analysis. That second panel shows the Galaxy Project in the center and connections to the workflow registries Dockstore and WorkflowHub. Github pull requests are shown as an alternative input source for Data Analysis. Data Analysis is connected to the rightmost panel via an arrow leading to a schematically depicted FTP server holding key results files of an analysis. From there, data flow to the Viral Beacon, to the UCSC Genome Browser, and to an interactive notebook is shown.

### Figure caption
An automated SARS-CoV-2 sequencing data analysis system built around Galaxy as the analysis engine. Data to process is discovered and pulled into Galaxy from the European Nucleotide Archive (ENA) and processed via defined releases of Galaxy Workflows published at and downloaded via WorkflowHub. Third parties can also suggest their own public samples of interest to be included in analysis runs by opening a pull request on github with URLs to the raw data. Key files for every analysis run are exported to a publicly accessible FTP server space provided by the Centre of Genomic Regulation (CRG), and can be consumed by downstream visualisations like CRG’s Viral Beacon, the UCSC genome browser, and custom interactive notebooks.

## The components used

### European Nucleotide Archive (ENA)

to which many large national SARS-CoV-2 sequencing data providers submit their raw data. In the showcase we are using the ENA’s public API to extract links to the raw sequencing data of newly submitted sequenced reads from several large-scale national genome surveillance efforts including (but not limited to):
  - the COVID-19 Genomics UK Consortium (COG-UK; ENA study accession: PRJEB37886)
  - the Portuguese network for SARS-CoV-2 genomics (PRJEB47340)
  - the Estonian national sequencing initiatives (KoroGeno-EST-3 and KoroGeno-EST-2022; see dedicated showcase)

In addition, we provide the possibility to request analysis of samples of particular interest via pull requests to a dedicated github repo.

### WorkflowHub registry for scientific workflows

The registry provides access to hundreds of workflows with defined releases, among them several Galaxy workflows for SARS-CoV-2 genome analysis provided and reviewed by the IWC.

### European Galaxy Server

which provides free access to powerful publicly-funded compute infrastructure and  thousands of bioinformatics tools
In the showcase we download ENA-hosted sequencing data using the links discovered above to the server and process it with the workflows from WorkflowHub.

### FTP server

provided by the Centre for Genomic Regulation (CRG)  For every sample processed through Galaxy workflow runs, we are exporting key results files (reads mapped to the viral reference sequence, variant calls, consensus sequences and tabular reports) to a public space on this server so that consumers can discover, access and reuse it without dealing with Galaxy at all. We are also maintaining a provenance JSON file on that server that makes it possible to reconstruct the full data processing history of each sample. One can access all the data by logging in to: ftp://xfer13.crg.eu as User: FTPuser Password: FTPusersPassword

### Viral Beacon project

In the showcase the project acts as a consumer of the data and provides visualisations for it

### UCSC genome browser

which offers a Galaxy ENA mutations track populated from the data on the CRG’s server.

These components are connected using free and open source “glue” code that can be found on github. The code relies, to a large extent, on built-in Galaxy functionality, which it accesses via the Galaxy API, including uploading data via links, running workflows in an automated manner, sending result datasets to a remote file source, tagging analysis artefacts for easier discovery, publishing analyses for accessibility, etc, allowing us to keep the code minimal.

## How to reuse these components

An important aspect for reusability is the modular architecture of the showcase. You could for example:
- Swap out the Galaxy server instance used to process the data
  All analysis tools used in the Galaxy workflows are publicly available and are easy to install on any Galaxy instance.
- Get the raw sequencing data from other sources than the ENA
  As long as you can give Galaxy access to the data there should be a way to feed it into the system.
- Build and run modified versions of the workflows
  Galaxy comes with an easy-to-use graphical workflow editor that lets you adapt any of the existing public workflows to your specific needs.
- Send results files to a different remote file system
  Galaxy has a plugin system through which it can be connected to various remote file systems for data export.
- Use the data to populate other dashboards of your choice
  The Galaxy project and collaborators have, for example, come up with an interactive Observable dashboard as an alternative visualisation tool for the showcase.

## What can you use the showcase for?
 
This showcase illustrates how you can combine existing public frameworks, registries, and data repositories, that have all been created or enhanced significantly over the course of the COVID-19 pandemic, to conduct automated, reproducible, shareable, transparent, high-quality viral sequencing data analysis at any scale using open-source code. 

Thanks to its modular architecture, the showcase and its underlying code and workflows can be tweaked to the specific needs of your project with relatively little effort.

## COVID19 Galaxy Project Team Members
Wolfgang Maier, Simon Bray, Anton Nekrutenko, Björn Grüning, Marius van den Beek and Dannon Baker from the Galaxy project; Babita Singh, Mauricio Moldes, Jordi Rambla from CRG and the Viral Beacon project; Maximilian Haeussler from the UCSC genome browser team; Sergei Pond (Temple University) developed interactive Observable notebooks.

Additional people who have helped improve the workflows used for the data analysis: Ulvi Talas (University of Tartu), Peter van Heusden (SANBI)
