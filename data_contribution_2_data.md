<!--

author:   Arcus Library Sciences
email: dlarcuslibraryscience@chop.edu
version:  1.0.0
current_version_description: Brief description of why this version exists
module_type: standard
docs_version: 1.1.0
language: en
narrator: UK English Female
title: Arcus Project Template Orientation
comment:  Learn about the project template directory structure, which is used in Acus labs and for archiving data.
long_description: Arcus Archives is the canonical repository for research data at CHOP. Archiving research data preserves the important research performed at CHOP according to archival standards while facilitating data sharing. This module reviews reasons to archive research data at Arcus, and the data scoping, privacy review and technical considerations taken before receiving data. Module 2 covers the steps of archiving the data at Arcus.

estimated_time: 30 minutes

@pre_reqs
We recommend completing the Arcus Data Contribution Orientation before doing this module. It's helpful to have reviewed the [Arcus website](https://arcus.chop.edu) at  (available only on the CHOP network), to understand Arcus’s overall goals.

@end

@learning_objectives

After the completion of this training module, learners will be able to:

* Use the project template directory structure to organize clinical data and omics data in any storage environment
* How to use the project template within a Arcus Scientific Computing lab
* Prepare a research data contribution for archiving in Arcus

@end


import: https://raw.githubusercontent.com/arcus/education_modules/main/_module_templates/macros.md
-->

# Arcus Project Template Orientation

<div class = "overview">

## Overview

@comment

### Is this module right for me?

@long_description

### Details

**Estimated time to completion**: @estimated_time

**Pre-requisites**:

@pre_reqs

**Learning Objectives**:

@learning_objectives

</div>

<div class = "important">

Hi! This document is still under construction and testing. We apologize in advance for any broken links or unclear language. We invite your feedback. Please add a [support ticket](https://support.arcus.chop.edu/servicedesk/customer/portal/6/create/249) or [email Arcus Library Sciences](mailto:dlarcuslibraryscience@chop.edu) to let us know what we can improve or suggest additional topics.

Please note that **many of the links here will only work if you're on the CHOP network**.

</div>

## Audience

This module introduces the CHOP community to the Project Template, a structure file directory for managing research data. It is useful to ANYONE at CHOP involved in creating, managing or analyzing research data.

The Project Template offers an easy to use and flexible structure for organizing data providing structure and context to project files and documents. It provides a shared, documented framework for organizing a research effort. This achieves multiple goals:

- It assists research teams in building transparency and reproducible workflows.
- It establishes a structure that allows for easier long-term preservation.
- It provides context to assist in future reuse of research either for collaborators or for the original researcher themselves.
- It organizes a research project for archiving within Arcus.

<div class = "learn-more">
<b style="color: rgb(var(--color-highlight));">Learning connection</b><br>

The Project Template is useful in creating reproduceable, generalized and reuseable research. To learn more about reproduceable, generalized and reuseable principles in research, check out the [following module](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/reproducibility/reproducibility.md#1) from the Arcus Education team.

</div>

### In progress data contributors

Thank you for agreeing to contribute your data. All contributed research data will be arranged into the Project Template structure this module describes all sections of the project template structure, what data goes in each section, and give examples of research data arranged in the template.

This module can be used as a reference while you navigate the archiving process, please reach out to the Digital Archivist if you have further questions. Please share this module with others on your research team involved with preparing the data contribution, or other researchers that may be interested in archiving data with Arcus.

### Future data contributors

This module is an overview of CHOP's Project Template Directory structure, all contributed data is aranged in this structure for archiving in Arcus. The Project Template is useful at all stages of research, we suggest implementing it as early as possible in your research as it provides a shared, documented framework for organizing a research effort.

We are happy to meet with researchers at all phases of research for research data management consultations and planning for future archival contributions. This includes early in your research project, as we can help set up a project template file directory structure for storing data and recommend metadata and organization best practices. In addition to this module, there are additional data management resources available on CHOP’s [Arcus resources page](https://www.research.chop.edu/applications/arcus/resources).

If after viewing this module, you are prepared to archive data with Arcus, please fill out [the following request](https://pm.arcus.chop.edu/servicedesk/customer/portal/6/create/256) to start the process.

### Arcus Lab Users

The Project Template is added to all Arcus Scientific Computing Labs (Arcus Lab), so all you have to do is set up your workflows to conform to the template. This module describes all sections of the project template structure, what data goes in each section, and give examples of Arcus lab research data arranged in the template.

As part of the Arcus Lab deployment, your team should have received a Project Template orientation by a member of the Library Science team. If you missed the orientation, or need a refresher on the orientation, please see this [video of the orientation](https://www.youtube.com/watch?v=YJvA_cryI1s)

When appropriate, archiving your research in Arcus is expected with a Scientific Project with an Arcus Lab. This is documented in the [Arcus Terms of Use](https://arcus.chop.edu/terms-of-use). Archiving is required if you would like to move any data created within an Arcus Lab to a new Scientific Project with an Arcus Lab or if other research teams would like to reuse your data.

When you are ready to archive your lab data, please submit the following request in the [Arcus Help Center](https://pm.arcus.chop.edu/servicedesk/customer/portal/6/create/256) to begin the data contribution process.

### Arcus Data Lifecycle

Before describing the template in detail, give background of its history and integration into Arcus data lifecycle. The project template is integral to Arcus data sharing.

**How was this structure developed?**

The CHOP project template file directory structure was adapted from [DrivenData’s Cookiecutter Data Science template](https://cookiecutter.readthedocs.io/en/stable/). It was adapted by former Arcus Digital Archivist, Christiana Dobrzynski, and former CHOP Bioinformaticist, Perry Evans. Both Arcus’ and DrivenData’s templates aim to organize research data and tools for accuracy and reproducibility. See [DataDriven's introduction](http://drivendata.github.io/cookiecutter-data-science/) to learn more about the goals and purpose of project tempalte structures for data preservation and sharing.

The CHOP project template evolved through iterations and feedback from CHOP researchers. A multi-disciplinary groups of practicioners were consulted in the template adaptation development, including:

- Bioinformatics
- Cancer research
- Microbiome center
- Research IT
- Clinical sequening unit
- Medical Informatics Unit

**How is the Project Template used at Arcus?**

The Arcus template also prioritizes streamlined archiving and reproducible research pathways. It strives to archive various research types from the Research Institute, accessible through tools like Arcus Cohort Discovery, Gene, and Omics Variant Browser. This template facilitates organizing diverse research data in a single directory structure, enabling automated archiving, metadata management, and data delivery throughout the research data lifecycle. This file directory structure is used for the entire lifecycle of research data within Arcus:

[FIGURE]

The project template provides a shared structure so that institutional knowledge previously held locally by various members of the data creation team becomes centralized.  
The utility of the project template for lab drive organization and integration with the Arcus archives is summarized in the graphic below.

[FIGURE]

### Data Management for Grant Requirements

The new NIH data management and sharing policy becomes effective January 25, 2023. ALL grant applications or renewals that generate scientific data must now include a detailed Data Management and Sharing Plan (DMSP). The DMSP documents the lifecylce of the data generated in the research project. The plan offers information on data collection for storage, access, sharing and reproducibility of your results.

Use of the Project Template and archiving in Arcus will build a robust and detailed plan for how you will manage and share data during the entire funded period. Detailed information abo.ut Arcus resources for developing and writing a DMSP are available at [this link](https://www.research.chop.edu/applications/arcus/resources)

<div class = "learn-more">
<b style="color: rgb(var(--color-highlight));">Learning connection</b><br>

To learn more about Research Data Management, check out the [following module](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/data_management_basics/data_management_basics.md#1) from the Arcus Education team.

</div>

## Project Template

Overview. Show the whole template.

Arcus' goal for research data management and project templates is to furnish tools that are relevant throughout the entire lifecycle of research data. These tools are adaptabtable and an iterative, as opposed to being a rigid, inflexible solution. Consequently, our approach involves presenting comprehensive overviews, resources, and a project template that offer optimal methodologies and suggestions, rather than strict mandates dictating how research should be conducted within specific domains. This project template exhibits the required flexibility to encompass diverse data capturing needs, while also maintaining a universal quality that facilitates seamless communication among various projects spanning different domains, thereby promoting effective data sharing.

The project template structure outlines a number of directories that are intended to capture three major aspects of a research effort: the data (data), the tools needed to work with that data (access tools), and the contextual information needed to understand the effort and its constituent parts (contextual). The high level directories are as follows (items with asterix are required):

- **_Configs_** (contextual)
- **_Data_** (data)\*
- **_Manifests_** (data)\*
- **_Models_** (access tools)
- **_References_** (contextual)
- **_Reports_** (contextual)
- **_Requirements_** (contextual)
- **_SRC_** (access tools)

Below is an image of the entire Project Templat Directory, with more detail about each section:

https://storage.googleapis.com/arcus-edu-libsci/Project%20Template%20Lab%20Resources/Project%20Template%20Structure.pdf

### Research Data

I was thinking of doing a further explanation of the 'sections' (research data, access tools and contextual files) but I am not sure that is neccessary.

### Access Tools

### Contextual files

## Intro

An introduction to the next section, asking the user to choose examples.

## data/

- Research data: Information collected during the course of research processes used for analysis
- Maintains descriptions of authoritative source data and their associated files and metadata in both raw and processed formats

### data/raw

- Arcus-delivered data goes here.
- Study team generated data brought into Arcus goes here.
- Authoritative source data that should never be deleted.
- Organize in subdirectories if necessary.

#### data/raw omics example

- Most sequencing providers will generate a [**fastq**](https://maq.sourceforge.net/fastq.shtml) file or [**cram**](https://samtools.github.io/hts-specs/CRAMv3.pdf) file.

* These files contain genomic sequences called reads. With paired reads, there are two fastq files per sample. Cram files are single files aligned to a reference genome.

- We collect the compressed fastq form fastq.gz, which can be made with lossless compression utility tools like gzip. fastq metadata are described in the fastq directory.
- Cram files are human readable and highly space efficient by using reference-based compression of sequence data. These files enable us to run a complete re-analysis of the data. Cram files require a companion index file, crai.

#### data/raw clinical example

- For a registry, database, or any other type of clinical dataset the raw data will be the research directly collected from subjects whether managed by automated processes or via manual entry.
- This version of the dataset often contains identifiable information and is most critical for secondary use.

### data/interim

- Managed by study team.
- Unregulated space for intermediate and temporary files.
- Not necessary to save long term.
- Recommend establishing retention schedules for regular review/clean-up.

#### data/interim clinical example

- Scratchwork generated during clincal research is not valuable for posterity's sake.
- However, it can be a good insight into the research process and can be archived.

#### data/interim/ omics example

- QC metrics Quality Control (QC) metrics are reported at various stages of analysis pipelines and give information about the quality of the data generated. QC metrics files should be in a tabular file format, with .type_metrics or .duplicate_metrics as the extension. QC metrics files will always be stored in the sources/data/interim directory.

### data/endpoints

- Managed by study team.
- Final results from research analysis.
- Files generated to support papers or grants.
- Organize in subdirectories if necessary.

#### data/endpoints omics example

- gvcf files contain variant information, describing genomic regions with no variants for a single sample. They are used to compare variant calls across samples to make vcf files. We collect them to enable the easy construction of larger cohorts.
- We collect the compressed version of a gvcf file, which can be made with a lossless compression utility tool like gzip.
- vcf files usually contain multiple samples, and are the starting point for most reserach project's analysis. They are not appropriate for constructing cohorts from multiple projects because they are missing necessary information contained in the gvcf files. We collect the compressed version of a vcf file, which can be made with a lossless compression utility tool like gzip. The variant calls in these files might differ from those in a gvcf file because they are made by considering information from all samples. A researcher would want to use these files when considering each project separately.

#### data/endpoints clinical example

### data/ref-data

- External or public datasets not supplied by Research IS or your lab, such as census data.

#### data/ref-data/platform_data omics example

- As cram files are a compressed format, some information is needed as a seperate file. If possible we collect a fasta file for the reference genome used. The fasta file describes offsets for each contig, to compute exactly where to find a particular reference base at specific genomic coordinates. Each fasta file requires an index file as fasta.fai

## manifests/

- Managed by Arcus
- Inventory of all raw & endpoint data
- Inventory of all participants and their related cohorts/samples/family roles, as applicable.
- Associates IDs with all data files.
- Documents relationships between files in pipelines/workflows.

### manifests/file_manifest omics examples

- file_manifest.csv matches biosample IDs to data files and experimental protocols, described in yaml files. Many files might share the same experimental protocol. These yaml protocol files describe experiment and data processing details (described later).

| column                  | definition                                                                                                                                                                                                                                                                                                                       | type   |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| biosample_id            | This ID links to PARTICIPANT_MANIFEST.                                                                                                                                                                                                                                                                                           | String |
| file_type               | Each experiment template has a list of required file types. Use those terms.                                                                                                                                                                                                                                                     | String |
| protocol                | Each experiment template has protocol yaml files or capture kit information used to describe experiment metadata. This column points to the file path of the protocol or the capture kit information for this file. Paths should start with references/procotols/ or data/ref-data/platform-data                                 | String |
| file_path               | Use one file path per row. It should start with data/.                                                                                                                                                                                                                                                                           | String |
| file_groups             | Files in the same group are related. Paired fastq files belong in the same group. A bam file and its index belong in the same group. Plink bfiles belong in the same group.                                                                                                                                                      | String |
| derived_from_file_group | This column describes relations between file groups. We want to capture consecutive pipeline steps. For example, a bam file is derived from a paired fastq group. Use the name of the file_groups used to construct this file. Delimit multiple groups with a semicolon. Use NA when there are no prior step files to reference. | String |

### manifests/file_manifest clinical example

### manifests/participant_manifest omics example

- participant*manifest.csv matches participants/patients to cohorts and biosample IDs. Ideally, biosample_id links to the CHOP biobank. When you cannot link the the biobank, treat biosample_id as the IDs you use for samples taken from participants. If you deal with only one sample type, you might use the participant ID. If you run a treatment/control experiment, you might use {participantID}\_treat and {participantID}\_control as as a biosample ID scheme. If you work with different tissue samples from participants, you might use {participantID}*{tissue} as a biosample ID scheme.

| column               | definition                                                                                                                    | type   |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ------ |
| local_participant_id | This ID uniquely defined a person, and can be linked to an MRN.                                                               | String |
| cohort               | Use this column to group participants into cohorts that will be cwmpared (For example, case vs healthy control).              | String |
| biosample_id         | Ideally, this ID can link to the CHOP biobank. When this is not possible, use the sample ID from your project.                | String |
| family_id            | When participants are related, use family_id to group related participants. With trios or duos, the proband ID is often used. | String |
| family_role          | Use a term from eHB_relationship_types_as_of_10_30.json to indicate mother, father, proband, sister, etc..                    | String |

### manifests/participant_manifest clinical example

### manifests/participant_crosswalk

- participant-crosswalk.txt is a tab delimited file with no header that links local_participant_id in PARTICIPANT_MANIFEST to MRNs.

column,definition,type,notes
local_id_type,The type of participant id (local).,String,This will always be local.
local_participant_id,Id that is used in PARTICIPANT_MANIFEST,String,
auth_id_type,The type of participant id(chop),String,This will always be chop.
auth_participant_id,Authorative Id of the participant. (Often MRN),String,Use an 8 digit MRN. Left-pad the MRN with zeroes as necessary.

### manifests/participant_family_role omics example

- participant_family_role.csv If you have family data, use this file to describe relationships with terms from data_dicts/eHB_relationship_types_as_of_10_30.json.

| local_participant_id | local_relative_id | relative_family_role |
| -------------------- | ----------------- | -------------------- |
| participant1         | participant2      | biological mother    |
| participant2         | participant1      | biological son       |
| participant1         | participant3      | biological father    |
| participant3         | participant1      | biological son       |
| participant1         | participant4      | biological sister    |
| participant4         | participant1      | biological brother   |

| column               | defintion                                                                                                             | type   |
| -------------------- | --------------------------------------------------------------------------------------------------------------------- | ------ |
| local_participant_id | The local id of a participant.                                                                                        | String |
| local_relative_id    | The local id of a relative to the participant.                                                                        | String |
| relative_family_role | The familial relationship of the relative to the participant. Use terms from eHB_relationship_types_as_of_10_30.json. | String |

- familyid_crosswalk.csv This manifest should be used with trio and cohort. A trio will contain three participants, a cohort can contain hundreds. This file walks the name for the trio or cohort file with the local_participant_id's included in it.

| family_id | individual_id | paternal_id | maternal_id | sex |
| --------- | ------------- | ----------- | ----------- | --- |
| LML100    | 101354        |             |             | 2   |
| LML100    | 101355        |             | 101354      | 1   |
| LML101    | 102454        |             |             | 2   |
| LML101    | 102455        | 102456      | 102454      | 1   |
| LML101    | 102456        |             |             | 1   |
| LML102    | 103767        |             |             | 1   |
| LML102    | 103768        |             |             | 2   |
| LML102    | 103769        | 103767      | 103768      | 2   |
| LML103    | 108976        | 108977      | 108978      | 1   |
| LML103    | 108977        |             |             | 1   |
| LML103    | 108978        |             |             | 2   |
| LML104    | 104666        | 104667      | 104668      | 2   |
| LML104    | 104667        | -9          | -9          | 1   |
| LML104    | 104668        | -9          | -9          | 2   |

| family_id            | Required, the family_id for the trio data                                           |
| -------------------- | ----------------------------------------------------------------------------------- |
| local_participant_id | Required, the local_particpant_id for each of the participants included in the trio |
| paternal_id          | Optional, the local_participant_id for the father of the participant                |
| maternal_id          | Optional, the local_participant_id for the mother of the participant                |
| sex                  | Optional, the sex of the participant. 1 for male, 2 for female                      |

### manifests/file_derivation.csv

- file_derivation.csv describes the relationships between files in a pipeline or workflow.

| column                 | definition                                                      | type   |
| ---------------------- | --------------------------------------------------------------- | ------ |
| destination_file_group | The files in this file group is derived from source_file_group. | String |
| source_file_group      | File group used to derive the destination_file_group.           | String |

### manifests/env_manifest.csv

- Environment files are necessary for all scripts and machine models, and document the environment in which it was created and run. The environment_manifest.csv links the script or machine model and the environment file stored within the configs directory.

| column                | definition                                                                                                                                                                                                                                                                          | type   |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| programming_filegroup | Enter the highest level folder that the environment file relates to. If the file relates to an entire directory then put the whole directory file path. If the file relates to a suddirectory enter that filepath. If it relates to a single file enter the file path and filename. | String |
| related_environment   | Enter the environment filename. Some environment files will be entered multiple times as they relate to multiple files.                                                                                                                                                             | String |
|                       |

## src/

- Managed by study team.
- Access tools required of the research data itself.
- Version control is important!
- Subdirectory folders can be customized and added as needed.

### src/subfolders

- Some example options are as follows
- notebooks: Jupyter, Beaker, Zeppelin, WDL, etc.
- scripts: custom software, code, tools
- rules: for computational workflows
- test: unit testing for code, customizable to team needs

## models/

- machine learning models, model predictions, model summaries, datasheets for model training data

## references/

- contains general information about the research effort such as IRB documents, reference papers, sample information, lab prep information, data dictionaries.
- Protocols: experimental protocols
- Further subdirectories can be customized.

### references/data_dictionary clinical example

- A data dictionary will help people better understand the scope, purpose, and nuance of the data you are collecting.
- Some data dictionaries are extensively detailed, but even a basic minimal data dictionary is better than none at all. Data dictionaries are usually used for tabular datasets, but can be used for data in other formats as well!
- Below are the fields you can consider including in your data dictionary. Only a few are considered truly **required** - the rest are optional but can be extremely helpful, so you should consider whether they make sense to collect in your case.
- You may also have additional fields to include that are not listed here; you know your data best!

**Name​**: (required) provide the name of the data element you are describing as it appears in the dataset.

**Description**​: (required) provide a brief description of the data element. Things to include here if applicable: source of data element, units of measure, formulas for calculated fields, nuances of data capture environment, anything else relevant to understanding what this field means and how to use it.

**Human-readable Name**​: (optional) provide a human readable name / title for the data element. This can be handy if the names in your dataset are hard to parse or hard to understand.

**Type**​: (optional) indicates the type of data i.e. numeric, string, date, etc. If you are collecting data in a database that enforces types, sometimes this can be easily extracted. This is useful to know for future transformation or integration of datasets

**IsNull**​: (optional) this a yes/no field that indicates whether the item can be null (absent of information) or not. If this is set to “no”, this indicates data should ​always​ be present in the field, and is helpful to users who may wonder whether an absence of data is to be expected or indicative of a problem

**Values**​: (optional) if there is a restricted list of values that can populate this field, include that here. An example might be “eye color” with the value list “blue, brown, grey”. Providing the list of values helps users understand why data may be absent. E.g. are there no green-eyed people in the dataset because there were none in the population or because “green” was not one of the available values for this field?

**Date added**​: (optional) indicate the date on which this particular field was added to the dataset. This can be useful for understanding why data may be absent.

**Date removed / Date deprecated**​: (optional) indicate the date on which this particular field ceased to be collected as part of the dataset. This can be useful for understanding why data may be absent.

**Relationships**​: (optional) indicate whether the data element is related to other data elements in your data set (in relational database terms, this is where you would indicate a “foreign key”)

**Additional Documentation**

- In addition to documenting data fields, your data dictionary should also include an overarching description of the dataset itself.
- If you have more than one dataset, or more than one data table, include a description for each. The descriptions for data tables and datasets should include some idea of the scope of data included, as well as the purpose in collecting or creating the data and its intended use.

#### Sample Data Dictionary from the PEDSnet Data Contribution

| table_name | field_name               | description                                                                                                | type       | phi | ordinal_position | crosswalk_needed | crosswalk_note |
| ---------- | ------------------------ | ---------------------------------------------------------------------------------------------------------- | ---------- | --- | ---------------- | ---------------- | -------------- |
| person     | person_id                | A unique identifier for each person; this is created by each contributing site.                            | BigInteger | 1   | 1                | 1                |                |
| person     | gender_concept_id        | A foreign key that refers to a standard concept identifier in the Vocabulary for the gender of the person. | Integer    | 0   | 2                | 0                |                |
| person     | gender_source_concept_id | A foreign key to the gender concept that refers to the code used in the source.                            | Integer    | 0   | 3                | 0                |                |

#### Sample Explanation of Tables from the PEDSnet Data Contribution

| name             | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| adt_occurrence   | The adt_occurrence table contains information about distinct admission, discharge, or transfer events that occur as part of a clinical visit. The typical use case is to identify portions of an inpatient admission that represent different levels of care or locations within a facility, but it can be used for additional characteristics of a visits (e.g. specialty consultation). The time of each event must fall between the start and end times of the associated visit_occurrence.                                                                                                                                                                                                                                                                                                                                                                    |
| care_site        | The Care Site domain contains a list of uniquely identified physical or organizational units where healthcare delivery is practiced (offices, wards, hospitals, clinics, etc.).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| concept_ancestor | The CONCEPT_ANCESTOR table is designed to simplify observational analysis by providing the complete hierarchical relationships between Concepts. Only direct parent-child relationships between Concepts are stored in the CONCEPT_RELATIONSHIP table. To determine higher level ancestry connections, all individual direct relationships would have to be navigated at analysis time. The CONCEPT_ANCESTOR table includes records for all parent-child relationships, as well as grandparent-grandchild relationships and those of any other level of lineage. Using the CONCEPT_ANCESTOR table allows for querying for all descendants of a hierarchical concept. For example, drug ingredients and drug products are all descendants of a drug class ancestor. This table is entirely derived from the CONCEPT, CONCEPT_RELATIONSHIP and RELATIONSHIP tables. |

### references/protocols omics examples

Below is further description about the metadata elements in a sample fastq protocol:

- **sequencing_type**: Type of sequencing that was performed. You should use the term from the vocabulary list. Common types: WGS, WES, RNA-Seq

- **platform_name**: Platform that was used to perform the sequencing. You should use the term from the vocabulary list. Common platforms: Illumina, Solid, Roche, Ion Torrent

- **instrument_model**: Specific sequencing machine used to produce the sequence file. For a list of illumina platforms, see this link. You should use the term from the vocabulary list.

- **platform_unit**: The platform unit string holds three types of information, the FLOWCELL_BARCODE.LANE.SAMPLE_BARCODE. The FLOWCELL_BARCODE refers to the unique identifier for a particular flow cell. The LANE indicates the lane of the flow cell and the SAMPLE_BARCODE is a sample/library-specific identifier.

- **capture_roi**: File name or file path in the repo for a file that gives specifications and details for the region of interest.

- **capture_kit**: Name of the library preparation kit used with the platform for sequencing the sample. It is important that the name of the kit is standardized and consistent, you should copy the name EXACTLY as it was recorded by the sequencing vendor. Capture kit titles that have been used by previous contributuions are recorded in the the vocabulary list, please use the title listed there when possible.

- **process_description**: Further detail about the library or process used when sequencing the files that is not captured by other metadata terms.

- **read_group_id**: A tag that identifies which read group each read belongs to. A read group is a set of reads generated from a single run of a sequencing instrument, and should be unique for each group.

- **aligned**: Fill in: true or false.

- **genome_build**: If the file is aligned, record the genome build the sequence is aligned to. You should use the term from the vocabulary list. Commonly used genome_build terms: HG19 human reference genome, HG38 human reference genome

- **sequencing_center**: Name of the sequencing center or vendor that did the sequencing of the samples. You should use the term from the vocabulary list. Commonly used sequencing centers: Children's Hospital of Philadelphia (CHOP) Division of Genomic Diagnostics (DGD), Children's Hospital of Philadelphia (CHOP) High Throughput Sequencing (HTS) Center, Children's Hospital of Philadelphia (CHOP) Center for Applied Genomics (CAG), Broad Institute

- **run_date**: Date the sequence was performed on.

- **targeted_depth**: Total amount of sequence data produced by the instrument (pre-alignment), divided by the reference genome size. It should have been provided by the vendor.

- **stranded**: ONLY RELEVANT FOR RNA-seq DATA. Whether the strand specificity of origin for each transcript was retained. Fill in: true or false.

- **strand_name**: ONLY RELEVANT FOR RNA-seq DATA, and only filled in if above is true. Strand information or kit used. You should use the term from the vocabulary list.

- **creator**: Name and job title of the creator of the protocol.

- **info_provider**: Name and job title for the person that provided the information. May be the same as the creator.

_to be filled with sample data_:

---

sequencing_type:
platform_name:
instrument_model:
platform_unit:
capture_roi:
capture_kit:
process_description:
read_group_id:
genome_build:
sequencing_center:
run_date:
targeted_depth:

_for RNA-seq files_

stranded:
strand_name:

_information about this file_

creator:
info_provider:

_information about this template_

meta:
version: 2.0.0

# reports/

- Content used for producing papers, presentations, websites, metrics, etc.
- Figures & tables: generated metrics and graphics for supporting reports
- Log.md: computational notebook (if one was used to create the content)
- Methods.md: version controlled methods section for the project
- Further subdirectories can be customized.

# requirements/

- Any module or library dependencies for workflows.
- Additional requirements files can be added as needed.

# configs/

- Configuration files for workflows or applications.

## configs/environments

### Capturing an Analysis Environment

- For each script/notebook in src, each model in models, and any files in data/endpoints, there should be an env._ file (here env._ refers to a file named env with any extension, so env.yaml or env.txt, for example) that describes the environment in which it was created or run.
- Environment files should be named as follows: descriptiveName_env.\* and placed in a folder called environments within the configs/ directory.
- Either individuals files or entire folders(whichever is the appropriate level) in scripts and notebooks within the src/ directory, the models/ directory, or the data/endpoints folder will need to be added to the env_manifest.csv file, matching them with their related environment file.

### Arcus Lab Images

- There should also be a file named lab-image-tag within a folder titled lab-image within the configs/ directory that contains the tag of the Arcus Lab Image that the Lab was using.
- Though unlikely, if artifacts use more that one image than follow the directions above (in the environments section): add a descriptive name to each lab-image-tag file, and add the file paths and related files or directories to the env_manifest linking them together.
