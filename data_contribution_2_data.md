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
comment: Learn about how to disclose data to CHOP by making a data contribution!
long_description:  Arcus Archives serves as the canonical repository for research data at CHOP. Archiving data with Arcus safeguards and maintains research data in accordance with established archival protocols, also while promoting data sharing. The Data Contribution Module provides an overview of the reasons to archive research data with Arcus, as well as the processes involved in scoping data, conducting privacy assessments, and addressing technical requirements prior to data submission. This Module explores the Project Template directory structure, and delves into the specific steps required for archiving data within the Arcus platform.

estimated_time: 60 minutes

@pre_reqs
We recommend completing the [Arcus Data Contribution Orientation](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_data_contribution.md#1) before doing this module. It's helpful to have reviewed the [Arcus website](https://arcus.chop.edu) (available only on the CHOP network), to understand Arcus’s overall goals.

@end

@learning_objectives

After the completion of this training module, learners will be able to:

* Use the project template directory structure to organize clinical data and omics data in any storage environment
* Use the project template within a Arcus Scientific Computing lab
* Prepare a research data contribution for archiving in Arcus

@end

@contingent_text
<script modify="false">
try {
  let data_type = @input(`data_type`)

  if(data_type[@0]) {
    send.liascript(`@1`)
  } else send.clear()
} catch(e) { }
</script>
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

**Prerequisites**:

@pre_reqs

**Learning Objectives**:

@learning_objectives

</div>

<div class = "important">

Hi! This document is still under construction and testing. We apologize in advance for any broken links or unclear language. We invite your feedback. Please add a [support ticket](https://support.arcus.chop.edu/servicedesk/customer/portal/6/create/249) or [email Arcus Library Science](mailto:dlarcuslibraryscience@chop.edu) to let us know what we can improve or suggest additional topics.

Please note that **many of the links here will only work if you're on the CHOP network**.

</div>

## Audience

This module introduces the CHOP community to the Project Template, a structured file directory for managing research data. It is useful to ANYONE at CHOP involved in creating, managing or analyzing research data.

The Project Template offers an easy to use and flexible structure for organizing data, and ensures necessary context is preserved for project files and documents. It provides a shared, documented framework for organizing a research effort. This achieves multiple goals:

- It assists research teams in building transparency and reproducible workflows
- It establishes a structure for easier long-term preservation
- It preserves context needed for future reuse of research by collaborators or for the original researcher
- It organizes a research project for archiving within Arcus

<div class = "learn-more">
<b style="color: rgb(var(--color-highlight));">Learning connection</b><br>

The Project Template is useful in creating reproducible, generalized and reuseable research. To learn more about reproducible, generalized and reuseable principles in research, check out the [following module](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/reproducibility/reproducibility.md#1) from the Arcus Education team.

</div>

### In progress data contributors

Thank you for agreeing to contribute your data, all contributed research data will be arranged in CHOP's Project Template structure. This module describes all sections of the project template structure, what data goes in each section, and shows examples of research data arranged in the template.

This module can be used as a reference while you navigate the archiving process, please reach out to the Digital Archivist if you have further questions. Please share this module with others on your research team involved with preparing the data contribution, or other researchers that may be interested in archiving data with Arcus.

### Future data contributors

This module is an overview of CHOP's Project Template structure, all contributed data is arranged in this structure for archiving in Arcus. The Project Template is useful at all stages of research, we suggest implementing it as early as possible in your research as it provides a shared, documented framework for organizing a research effort.

Arcus's Library Science team is happy to meet with researchers at all phases of research for research data management consultations and planning for future archival contributions. This includes early in your research project, as we can help set up a project template file directory structure for storing data and recommend metadata and organization best practices. In addition to this module, there are additional data management resources available on CHOP’s [Arcus resources page](https://www.research.chop.edu/applications/arcus/resources).

If after viewing this module, you are prepared to archive data with Arcus, please fill out [a data contribution request](https://pm.arcus.chop.edu/servicedesk/customer/portal/6/create/256) to start the process.

### Arcus Lab Users

The Project Template is added to all Arcus Scientific Computing Labs (Arcus Lab), so all you have to do is set up your workflows to conform to the template. This module describes all sections of the project template structure, what data goes in each section, and shows examples of research data arranged in the template.

As part of the Arcus Lab deployment, your team should have received a Project Template orientation by a member of the Library Science team. If you missed the orientation, or need a refresher on the orientation, please see this [video of the orientation](https://www.youtube.com/watch?v=YJvA_cryI1s). Much of the content covered in the video is also in this module.

When appropriate, archiving your research in Arcus is expected from Scientific Projects with an Arcus Lab. This is documented in the [Arcus Terms of Use](https://arcus.chop.edu/terms-of-use). Archiving is required if you would like to move any data created within an Arcus Lab to a new Scientific Project or if other research teams would like to reuse your data.

When you are ready to archive your lab data, please submit the following request in the [Arcus Help Center](https://pm.arcus.chop.edu/servicedesk/customer/portal/6/create/256) to begin the data contribution process.

## Arcus Data Lifecycle

Arcus's goal for research data management and the project template is to provide tools that are relevant throughout the entire lifecycle of research data. The project template is designed to be adaptable and iterative to capture the wide range of research activities at CHOP. The project template combines flexibility to encompass diverse data capturing needs, while also maintaining a consist structure for all archived data which facilitates seamless communication among various projects spanning different domains, thereby promoting effective data sharing.

**How was this structure developed?**

The CHOP project template file directory structure was adapted from [DrivenData’s Cookiecutter Data Science template](https://cookiecutter.readthedocs.io/en/stable/). It was adapted by former Arcus Digital Archivist, Christiana Dobrzynski, and former CHOP Bioinformatician, Perry Evans. Both Arcus’s and DrivenData’s templates aim to organize research data and tools for accuracy and reproducibility. See [DataDriven's introduction](http://drivendata.github.io/cookiecutter-data-science/) to learn more about the goals and purpose of project template structures for data preservation and sharing.

The CHOP project template evolved through iterations and feedback from CHOP researchers. A multi-disciplinary groups of practitioners were consulted in the template adaptation development, including:

- Bioinformatics
- Cancer research
- Microbiome center
- Research IT
- Clinical sequencing unit
- Medical Informatics Unit

**How is the Project Template used at Arcus?**

The Project Template prioritizes streamlined archiving and reproducible research pathways. It archives a wide range of research types from the Research Institute, making them discoverable through tools like Arcus Cohort Discovery, available as an application [on the Arcus website](https://arcus.chop.edu), [Gene](https://chop.alationcloud.com), and the Arcus Variant Browser, (available as an application [on the Arcus website](https://arcus.chop.edu)). The Project Template facilitates organizing diverse research data in a single directory structure, enabling automated archiving, metadata management, and data delivery throughout the research data lifecycle. This file directory structure is used for the entire lifecycle of research data within Arcus:

![Flowchart of the lifecycle of research data organized in the project template in Arcus. The main steps are delivering research data into Arcus labs in the project template structure, automated processing to archive the data, and redelivery of that data into an Arcus lab for reuse.](media/project_template/ProjectTemplate_Lifecycle.png)

The project template provides a shared structure so that institutional knowledge previously held locally by various members of the data creation team becomes centralized.

The utility of [the project template](https://github.research.chop.edu/arcus/rdm-project-template) for lab drive organization and integration with the Arcus archives is summarized in the graphic below.

![Flow chart of the workflow of archiving research data using the project template. The main steps are Organizing the file system, adding the research data, applying a standard pipeline, and automated Arcus data ingest](media/project_template/ProjectTemplate_workflow.png)

## Project Template

The project template structure includes directories for capturing three major aspects of a research effort: the data (data), the tools needed to work with that data (access tools), and the contextual information needed to understand the effort and its constituent parts (contextual). The high level directories are as follows (items with asterix are required):

- **_Configs_** (contextual)
- **_Data_** (data)\*
- **_Manifests_** (data)\*
- **_Models_** (access tools)
- **_References_** (contextual)
- **_Reports_** (contextual)
- **_Requirements_** (contextual)
- **_SRC_** (access tools)

Below is an image of the entire Project Template Directory, with more detail about each section:

![Graphic representation of the Project template with a short explanation of all the different sections. These sections are described in detail later in this module.](media/project_template/ProjectTemplate_Description.png)

### Research Data

The Project Template brings together three categories of information: Research Data, Access Tools and Contextual files. Research data is the actual data collected during the course of research processes used for analysis. The manifests describe this data, crosswalking files to participants. Research data (with manifests) is the minimum required information for all Arcus data contributions.

![Graphic representation of the Project template highlighting the research data directories described above. Research data directories are data and manifests.](media/project_template/research_data.png)

### Access Tools

Access Tools are the code used to do the analysis. This can include machine models, scripts and Jupyter notebooks.

![Graphic representation of the Project template highlighting the access tool directories, models and src. Subdirectories of src are notebooks, rules, scripts and tests.](media/project_template/access_tools.png)

### Contextual Files

Contextual Files provide information needed to understand the data and analysis. This can include omics protocols, data dictionaries, reports and diagrams.

![Graphic representation of the Project template highlighting the contextual files directories, configs, references, reports and requirements.](media/project_template/contextual_files.png)

## Project Template Directories

The next part of this module will walk through each sub-directory of the project template in detail. Though the project template is flexible enough to handle a wide range of research data, it's application and the filetypes in each directory will be different depending on the type of project. For this reason, we have two different examples: clinical data or omics data. In many of the following sections, you can select the option to view examples and specific information for the data type.

### File Naming and File Type Standards

Regardless of project type, Arcus follows industry standard guidelines for digital archiving applying these standards to incoming data contributions. File names should follow a consistent and clear schema, and not contain any spaces, periods or special characters. Further recommendations for file naming are below:

- [File naming tips sheet](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/fileNaming_bestPractices_MIT.pdf)
- [File naming conventions and activity sheet](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/arcus_rdm_filenaming_activity.pdf)
- [Recommended practices for README files](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/Arcus%20RDM%20Data%20Dictionaries%20Best%20Practices.pdf)

Whenever feasible, Arcus prefers to archive non-proprietary file formats as opposed to proprietary ones. Proprietary formats necessitate specific software for access or utilization, while non-proprietary formats are frequently open-source. Whenever you have the option, it's advisable to store data in a non-proprietary (open) file format. This choice enhances the accessibility of your content to others, enabling effortless reuse across various software platforms. Furthermore, this approach guarantees the continued utility of the file in the long term. In contrast, proprietary files carry the risk of becoming obsolete due to potential software incompatibility or restricted access.

<div class = "important">
<b style="color: rgb(var(--color-highlight));">Important note</b><br>

When it is necessary to save files in a proprietary format, consider including a README file that documents the name and version of the software used to generate the file, as well as the company who made the software. This could help down the road if we need to figure out how to open these files again.

</div>

### Preferred File Formats

For both the clinical data and omics examples in the Project Template walk through, we reference our preferred data formats for each type of data. Below are some general resources to help in choosing file formats:

- [Library of Congress Recommended Formats Statement](https://www.loc.gov/preservation/resources/rfs/)
- [UCSC Glossary of Omics File Formats](https://genome.ucsc.edu/FAQ/FAQformat.html)
- [NIH Clinical Trials Data Formats Overview](https://rethinkingclinicaltrials.org/chapters/conduct/acquiring-real-world-data/data-formats/#:~:text=XML%20is%20used%20as%20the,number%20of%20defined%20document%20templates.)

## data/

The data folder is where the data files are organized. Data is the information collected during the course of research processes used for analysis. The data directory maintains descriptions of authoritative source data and their associated files and metadata in both raw and processed formats. There are four sub-directories within the data folder for organizing the data: _raw/_, _interim/_, _endpoints/_, and _ref-data_.

All files within the **data/** folder and its subdirectories will be listed in the **file_manifest.csv**. The manifests are detailed in the **manifests** section of this course.

### data/raw

This directory holds authoritative source data that should never be deleted. This folder is where the original, unmodified data for the research project is stored. In a research process, this is the data used for the initial analysis. Further sub-directories can be added to organize data, if necessary.

**Within an [Arcus Scientific Lab](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/arcus_orientation.md#1)**

- Arcus delivered archival data will be found here.
- Study team generated data brought into Arcus goes here.
- This data is managed by Arcus, and should not be modified by the research team.

**Raw** data is different depending on the type of research. Please select what type(s) of data you would like more information about, you can select both:

- [ ] omics data
- [ ] clinical data
<script output="data_type">"@input"</script>

<script modify="false">
try {
  let data_type = @input(`data_type`)

  if(data_type[0]) {
    send.liascript(`## Omics Data


![Gif showing omics data arranged in the raw directory. Read files (cram/fastq/bam) are stored in data/raw.](media/project_template/raw_omics.gif)

For omics data, the raw folder contains the sequencing data. Most sequencing providers will generate a [**fastq**](https://maq.sourceforge.net/fastq.shtml) file or [**cram**](https://samtools.github.io/hts-specs/CRAMv3.pdf) file, we prefer these file types for archiving. These files contain genomic sequences called reads. With paired reads, there are two fastq files per sample. Cram files are single files aligned to a reference genome.

- We collect the compressed fastq form fastq.gz, which can be made with lossless compression utility tools like gzip. fastq metadata are described in the fastq directory.
- Cram files are human readable and highly space efficient by using reference-based compression of sequence data. These files enable us to run a complete re-analysis of the data. Cram files require a companion index file, .crai.

`)
  } else send.clear()
} catch(e) { }
</script>

<script modify="false">
try {
  let data_type = @input(`data_type`)

  if(data_type[1]) {
    send.liascript(`## Clinical Data


![Gif showing clinical data arranged in the raw directory. Data directly collected from subjects in CSV/TSV/XML or similar format is stored in data/raw.](media/project_template/raw_clinical.gif)

For a registry, database, or any other type of clinical dataset the raw data will be the research directly collected from subjects whether managed by automated processes or via manual entry. This version of the dataset often contains identifiable information and is most critical for secondary use.

- CSV and TSV formats are a great option for archiving flat file documents from an external data source to be contributed for archiving.
- Structured data in the [HL7's FHIR format](https://www.hl7.org/fhir/) or another ontology in the XML or JSON standard are also a preferred option.

**Within an [Arcus Scientific Lab](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/arcus_orientation.md#1)**

- Clinical data is often delivered to users in the BigQuery format to optimize search capabilities and performance. This data is accessed using SQL pad, which is preloaded into the lab. For Electronic Health Record (EHR) data, we have an existing workflow with the Arcus Data Repository (ADR) team for preserving work in this format.

<div class = "important">
<b style="color: rgb(var(--color-highlight));">Important note</b><br>

REDCap is a great application for clinical data projects of all sizes available to all CHOP personnel. The REDCap team at CHOP has great resources for [data collection best practices](https://storage.googleapis.com/arcus-edu-libsci/PDFs/Best%20Practices%20for%20REDCap%20Data%20Collection.pdf) for new projects and how to [import data](https://storage.googleapis.com/arcus-edu-libsci/PDFs/REDCap_Data_Import_Instructions.pdf) residing in a different application for complete projects ready to be archived. If you automate data collection directly from patients encounters in the EHR, there are options to feed that data directly into [REDCap via an API](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/using_redcap_api/using_redcap_api.md#1). If you collect data in REDCap, there is an option to both tag data with an identifiability label at the onset of a project as well as export data with all identifiable fields tagged.

</div>
`)
  } else send.clear()
} catch(e) { }
</script>

<script modify="false">
try {
  let data_type = @input(`data_type`)

  if(!data_type[0] & !data_type[1]) {
    send.liascript(`**Nothing is selected** 
<br>

`)
  } else send.clear()
} catch(e) { }
</script>

### data/interim

The interim directory is for storing outputs of data processing and analysis completed using the original, unmodified data store in **data/raw**. It is generally used for files that do not need to be stored long-term. Further sub-directories can be added to organize data, if necessary.

**Within an [Arcus Scientific Lab](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/arcus_orientation.md#1)**

- Data in this directory is managed by the study team
- It should be used as an unregulated space for intermediate and temporary files.
- Recommend establishing retention schedules for regular review/clean-up of data in this folder.

**Interim** data is different depending on the type of research. Please select what type(s) of data you would like more information about, you can select both:

- [ ] omics data
- [ ] clinical data
<script output="data_type_interim">"@input"</script>

<script modify="false">
try {
  let data_type = @input(`data_type_interim`)

  if(data_type[0]) {
    send.liascript(`
    ## Omics Data

![Gif showing omics data arranged in the interim directory. Metrics and reports (recalibration reports and QC metrics) produced as part of a bioinformatics analysis workflow stored in data/interim.](media/project_template/interim_omics.gif)

This directory is for the quality control and other reporting created during a bioinformatics workflow, using the sequence files stored in the \\_data/raw\\_ directory.

- QC metrics Quality Control (QC) metrics are reported at various stages of analysis pipelines and give information about the quality of the data generated. QC metrics files should be in a tabular file format, with .type\\_metrics or .duplicate\\_metrics as the extension.
    `)
  } else send.clear()
} catch(e) { }
</script>

<script modify="false">
try {
  let data_type = @input(`data_type_interim`)

  if(data_type[1]) {
    send.liascript(`
    ## Clinical Data
![Gif showing clinical data arranged in the interim directory. Scratch or alternatively formatted data (CSV/JSON/XML or similar) created during analysis or sharing stored in data/interim.](media/project_template/interim_clinical.gif)

This directory is for practice work generated during clinical research when analyzing and sharing original, unmodified data saved in \\_data/raw\\_. This can provide be a good insight into the research process and will be archived on a case by case basis. Additionally, alternatively formatted data, or excluded data can be saved in the interim directory. Data should be saved as a tsv, csv, xml or json file if possible.
    `)
  } else send.clear()
} catch(e) { }
</script>

### data/endpoints

The endpoints directory holds the final results created as part of a research analysis. Often, these are files created to support papers or grants, and other dissemination. Further sub-directories can be added to organize data, if necessary.

**Within an [Arcus Scientific Lab](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/arcus_orientation.md#1)**

- Data in this directory is managed by the study team.
- Data in this directory will be saved if the project is archived in Arcus.

**Endpoints** data is different depending on the type of research. Please select what type(s) of data you would like more information about, you can select both:

- [ ] omics data
- [ ] clinical data
<script output="data_type_endpoints">"@input"</script>

<script modify="false">
try {
  let data_type = @input(`data_type_endpoints`)

  if(data_type[0]) {
    send.liascript(`
    ## Omics Data

![Gif showing omics data arranged in the endpoints directory. Gene sequence variation files (vcf or gvcf) created using a bioinformatics workflow stored in data/endpoints.](media/project_template/endpoints_omics.gif)<!-- style = "max-height: 500px;" -->

This directory is for files created at the end of a bioinformatics workflow, like gvcf and vcf files.

- **gvcf** files contain variant information, describing genomic regions with no variants for a single sample. They are used to compare variant calls across samples to make vcf files. We collect them to enable the easy construction of larger cohorts. We collect the compressed version of a gvcf file (g.vcf.gz) which can be made with a lossless compression utility tool like [gzip](https://www.gzip.org). All gvcf files should include an index file, .tbi
- **vcf** files usually contain multiple samples, and are the starting point for most research project's analysis. They are not appropriate for constructing cohorts from multiple projects because they are missing necessary information contained in the gvcf files. We collect the compressed version of a vcf file (vcf.gz), which can be made with a lossless compression utility tool like [gzip](https://www.gzip.org). The variant calls in these files might differ from those in a gvcf file because they are made by considering information from all samples. A researcher would want to use these files when considering each project separately. All vcf files should include an index file, .tbi

    `)
  } else send.clear()
} catch(e) { }
</script>

<script modify="false">
try {
  let data_type = @input(`data_type_endpoints`)

  if(data_type[1]) {
    send.liascript(`
    ## Clinical Data

![Gif showing clinical data arranged in the endpoints directory. Analyzed or deidentified versions of data (CSV/JSON/XML or similar) stored in data/endpoints.](media/project_template/endpoints_clinical.gif)

This directory contains an analyzed version of a dataset or deidentified datasets.

- Sometimes these files can be more cohort scoped or present a refinement into initial research questions.
- This data is highly valuable for reuse because often errors in the clinical record emerge from this process and can be illustrative for researchers in an overlapping or similar specialty.
- Data should be saved as a tsv, csv, xml or json file if possible.

    `)
  } else send.clear()
} catch(e) { }
</script>

### data/ref-data

This directory is for any external or public datasets not created by the study team necessary to understand or repeat the analysis for the project.

**Within an [Arcus Scientific Lab](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/arcus_orientation.md#1)**

- External or public datasets not supplied by Research IS or your lab, such as census data, will be available in this directory.

**Ref-data** data is different depending on the type of research. Please select what below if need need more information about omics data for this directory:

- [ ] omics data
- [ ] clinical data
<script output="data_type_ref">"@input"</script>

<script modify="false">
try {
  let data_type = @input(`data_type_ref`)

  if(data_type[0]) {
    send.liascript(`
    ## Omics Data

- As cram files are a compressed format, some information is needed as a separate file. If possible we collect a fasta file for the reference genome used. The fasta file describes offsets for each contig, to compute exactly where to find a particular reference base at specific genomic coordinates. Each fasta file requires an index file as fasta.fai
- bed files are a text file format used to store genomic regions as coordinates and associated annotations, see [documentation](https://samtools.github.io/hts-specs/BEDv1.pdf) for more information on the format. If available, we collect this file as a .bed extension.


    `)
  } else send.clear()
} catch(e) { }
</script>


<script modify="false">
try {
  let data_type = @input(`data_type_ref`)

  if(data_type[1]) {
    send.liascript(`
    ## Clinical Data

Arcus Archives does not collect clinical reference data sets but there are ways to tap into the power of these datasets within Arcus.

- The Arcus Applied Data Sciences team offers [GIS Data](https://chop.alationcloud.com/domain/30/) of many high value publicly available regularly refreshed Geographical Information System Datasets.
- There is also an option via [Jira Service Desk](https://jira.arcus.chop.edu:8443/servicedesk/customer/portal/6/create/355?q=upload&q_time=1696276238126) to upload reference data directly to your lab following disclosure and approval.

    `)
  } else send.clear()
} catch(e) { }
</script>


## manifests/

Manifests are an inventory of all data in the collection, and provide a mapping between research data in the data folders, and participant information. The manifests also create a mapping between data and associated pipeline and technical information about workflows. There are three main manifests that are mandatory for every archival collection:

- file_manifest.csv
- participant_manifest.csv
- participant-crosswalk.txt

Additional manifests are only required if needed for the data or collection type. These files are detailed in the next sections. The graphic below illustrates the linking between the files:

![ID Crosswalks between file_manifest.csv, participant_manifest.csv and participant-crosswalk.txt](media/project_template/manifests_linkages.png)

**Within an [Arcus Scientific Lab](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/arcus_orientation.md#1)**

- Managed by Arcus, you will not need to create these for yourselves
- This will only appear in the lab if archival data is delivered

### manifests/file_manifest

The file\_manifest.csv matches the biosample\_id to each file in the data folders. Below is more detail about each section in the file:

- biosample\_id is an ID number for each file. For some studies, each file is derived about specific biosamples, so we suggest using the sample id. ideally, biosample\_id links to the CHOP biobank. When you cannot link the the biobank, treat biosample\_id as the IDs you use for samples taken from participants. For studies where there are no biosamples, the biosample\_id can be the file name.
- file_type is the type of file, indicated by the file extension
- protocol is only for omics data, select the omics data example below for more information
- file\_path is the file path for each file in the **data\\** folders. File paths should start with **data\\** and end with the full file name with extension

The **file_manifest.csv** may look different depending on the type of research. Please select below if you need more information about either omics or clinical data for this directory: 

- [ ] omics data
- [ ] clinical data
<script output="data_type_fm">"@input"</script>

<script modify="false">
try {
  let data_type = @input(`data_type_fm`)

  if(data_type[0]) {
    send.liascript(`## Omics Data

For Omics data, the **file\\_manifest.csv** matches biosample IDs to data files and experimental protocols, described in _yaml_ files. More information about the protocols files is available in the references section of this module. Many files might share the same experimental protocol. These _yaml_ protocol files describe experiment and data processing details. See below for the columns in a file\\_manifest:

| column                  | definition                                                                                                                                                                                                                                                                                                                       | type   |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| biosample\\_id            | This ID links to PARTICIPANT\\_MANIFEST.                                                                                                                                                                                                                                                                                           | String |
| file\\_type               | Each experiment template has a list of required file types. Use those terms.                                                                                                                                                                                                                                                     | String |
| protocol                | Each experiment template has protocol yaml files or capture kit information used to describe experiment metadata. This column points to the file path of the protocol or the capture kit information for this file. Paths should start with references/procotols/ or data/ref-data/platform-data                                 | String |
| file\\_path               | Use one file path per row. It should start with data/.                                                                                                                                                                                                                                                                           | String |
| file\\_groups             | Files in the same group are related. Paired fastq files belong in the same group. A bam file and its index belong in the same group. Plink files belong in the same group.                                                                                                                                                      | String |
| derived\\_from\\_file\\_group | This column describes relations between file groups. We want to capture consecutive pipeline steps. For example, a bam file is derived from a paired fastq group. Use the name of the file_groups used to construct this file. Delimit multiple groups with a semicolon. Use NA when there are no prior step files to reference. | String |


    `)
  } else send.clear()
} catch(e) { }
</script>

<script modify="false">
try {
  let data_type = @input(`data_type_fm`)

  if(data_type[1]) {
    send.liascript(`
    ## Clinical Data

Since clinical research efforts don't always collect biospecimen data, the columns in the file\\_manifest are simpler than an Omics contribution. See below for the columns required in the file\\_manifest:

| column                  | definition                                                                                                                                                                                                                                                                                                                       | type   |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| biosample\\_id            | This ID links to PARTICIPANT\\_MANIFEST.                                                                                                                                                                                                                                                                                           | String |
| file\\_type               | Each experiment template has a list of required file types. Use those terms.   | String |
| file\\_path               | Use one file path per row. It should start with data/.                         | String |

    `)
  } else send.clear()
} catch(e) { }
</script>

### manifests/participant_manifest

The participant\_manifest.csv identifies which participants information links to each of the files in the file\_manifest. Below is more detail about each section of the file:

- local\_participant\_id is a local identifier the study team used to identify the patient
- The biosample\_id will be the same as the one listed in the file\_manifests.csv. Linking a local\_participant\_id to a biosample_id identifies which patients information is related to the file.
- cohort is optional, please fill this in if there is additional cohort information or identification needed.

The **participant_manifest.csv** may look different depending on the type of research. Please select which type of data from below you need more information about for this directory:

- [ ] omics data
- [ ] clinical data
<script output="data_type_pm">"@input"</script>

<script modify="false">
try {
  let data_type = @input(`data_type_pm`)

  if(data_type[0]) {
    send.liascript(`## Omics Data

The **participant\\_manifest.csv** matches participants (or patients) to cohorts and biosample IDs from the **file\\_manifest.csv**. Ideally, biosample\\_id links to the CHOP biobank. When you cannot link to the biobank, treat biosample\\_id as the IDs you use for samples taken from participants. If you deal with only one sample type, you might use the participant\\_id. If you run a treatment/control experiment, you might use participant\\_id and treat participant\\_id\\_control as as a biosample ID scheme. If you work with different tissue samples from participants, you might use participant\\_id\\_tissue as a biosample ID scheme.

| column               | definition                                                                                                                    | type   |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ------ |
| local\\_participant\\_id | This ID uniquely defined a person, and can be linked to an MRN.                                                               | String |
| cohort               | Use this column to group participants into cohorts that will be compared (For example, case vs healthy control).              | String |
| biosample\\_id         | Ideally, this ID can link to the CHOP biobank. When this is not possible, use the sample ID from your project.                | String |
| family\\_id            | When participants are related, use family_id to group related participants. With trios or duos, the proband ID is often used. | String |
| family\\_role          | Use a term from [eHB\\_relationship\\_types\\_as\\_of\\_10\\_30.json](https://github.research.chop.edu/arcus/rdm-project-template/blob/master/manifests/data_dicts/eHB_relationship_types_as_of_10_30.json) to indicate mother, father, proband, sister, etc..                    | String |


    `)
  } else send.clear()
} catch(e) { }
</script>

<script modify="false">
try {
  let data_type = @input(`data_type_pm`)

  if(data_type[1]) {
    send.liascript(`## Clinical Data

Since clinical research efforts don't always collect biospecimen data, you may not use a Biorepository sample ID. When you cannot link the the biobank, treat instance\\_id as the IDs you use for samples taken from participants. The Epic Patient ID (start with Z) can be used as the local\\_participant\\_id. The list of required files we collect for this file are as follows:

- participant\\_manifest.csv
- local\\_participant\\_id
- cohort
- instance\\_id

    `)
  } else send.clear()
} catch(e) { }
</script>

### manifests/participant_crosswalk

The **participant-crosswalk.txt** manifest is a tab delimited file with no header that links local\_participant\_id in the **participant\_manifest.csv** to MRN (Medical Record Number). See below for the terms in the file:

| column               | definition                                     | type   | notes                                                          |
| -------------------- | ---------------------------------------------- | ------ | -------------------------------------------------------------- |
| local\_id\_type        | The type of participant id (local).            | String | This will always be local.                                     |
| local\_participant\_id | Id that is used in PARTICIPANT_MANIFEST        | String |                                                                |
| auth\_id\_type         | The type of participant id(chop)               | String | This will always be chop.                                      |
| auth\_participant\_id  | Authorative Id of the participant. (Often MRN) | String | Use an 8 digit MRN. Left-pad the MRN with zeroes as necessary. |

### manifests/participant\_family\_role

The **participant\_family\_role.csv** file is only needed for some omics data. If you have family data (ie sequencing data from related family members), use this file to describe [relationships](https://github.research.chop.edu/arcus/rdm-project-template/blob/master/manifests/data_dicts/eHB_relationship_types_as_of_10_30.json). See below for an example.

| local\_participant\_id | local\_relative\_id | relative\_family\_role |
| -------------------- | ----------------- | -------------------- |
| participant1         | participant2      | biological mother    |
| participant2         | participant1      | biological son       |
| participant1         | participant3      | biological father    |
| participant3         | participant1      | biological son       |
| participant1         | participant4      | biological sister    |
| participant4         | participant1      | biological brother   |

| column               | definition                                                                                                             | type   |
| -------------------- | --------------------------------------------------------------------------------------------------------------------- | ------ |
| local\_participant\_id | The local id of a participant.                                                                                        | String |
| local\_relative\_id    | The local id of a relative to the participant.                                                                        | String |
| relative\_family\_role | The familial relationship of the relative to the participant. Use terms from eHB\_relationship\_types\_as_of\_10\_30.json. | String |

### manifests/familyid_crosswalk

- This manifest should be used with trio and cohort omics data. A trio will contain three participants, a cohort can contain hundreds. This file walks the name for the trio or cohort file with the local\_participant\_id's included in it.
- This is also called a PED or pedigree file in bioinformatics workflows. A pedigree is a structured description of the familial relationships between samples, see this [link for more information](https://gatk.broadinstitute.org/hc/en-us/articles/360035531972-PED-Pedigree-format). 

<!-- data-type="none" -->
|family_id|individual_id|paternal_id    |maternal_id  |sex          |
|---------|-------------|---------------|-------------|-------------|
|LML100   |101354       |               |             |2            |
|LML100   |101355       |               |101354       |1            |
|LML101   |102454       |               |             |2            |
|LML101   |102455       |102456         |102454       |1            |
|LML101   |102456       |               |             |1            |
|LML102   |103767       |               |             |1            |
|LML102   |103768       |               |             |2            |
|LML102   |103769       |103767         |103768       |2            |
|LML103   |108976       |108977         |108978       |1            |
|LML103   |108977       |               |             |1            |
|LML103   |108978       |               |             |2            |
|LML104   |104666       |104667         |104668       |2            |
|LML104   |104667       |-9             |-9           |1            |
|LML104   |104668       |-9             |-9           |2            |


| family_id            | Required, the family_id for the trio data                                           |
| -------------------- | ----------------------------------------------------------------------------------- |
| local\_participant\_id | Required, the local\_particpant\_id for each of the participants included in the trio |
| paternal_id          | Optional, the local\_participant\_id for the father of the participant                |
| maternal_id          | Optional, the local\_participant\_id for the mother of the participant                |
| sex                  | Optional, the sex of the participant. 1 for male, 2 for female                      |

### manifests/file\_derivation.csv

The **file\_derivation.csv** manifest is only required for omics contributions with multiple filetypes generated through a bioinformatics pipeline or workflow.

**file\_derivation.csv** describes the relationships between files in a pipeline or workflow.

| column                 | definition                                                      | type   |
| ---------------------- | --------------------------------------------------------------- | ------ |
| destination\_file\_group | The files in this file group is derived from source\_file\_group. | String |
| source\_file\_group      | File group used to derive the destination\_file\_group.           | String |

### manifests/env manifest

For each script/notebook in *src/*, and each model in *models/*, there should be an env file (here env refers to a file named env with any extension, so env.yaml or env.txt, for example) that describes the environment in which it was created or run. Environment files should be named as follows: **descriptiveName\_env** and placed in a folder called environments within the *configs/environment/* directory. Either individuals files or entire folders (whichever is the appropriate level) in scripts and notebooks within the *src/* directory, or the *models/* directory will need to be added to the env manifest file, matching them with their related environment file. See the see below for more information about this file:

| column                | definition                                                                                                                                                                                                                                                                          | type   |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| programming\_filegroup | Enter the highest level folder that the environment file relates to. If the file relates to an entire directory then put the whole directory file path. If the file relates to a subdirectory enter that filepath. If it relates to a single file enter the file path and filename. | String |
| related\_environment   | Enter the environment filename. Some environment files will be entered multiple times as they relate to multiple files.                                                                                                                                                             | String |
|                       |

## src/

The src or sources folder stores the access tools required to work with the research data and repeat the analysis. The need for access tools is dependent on the type of research, not all research has rules, scripts or notebooks. Any scripts saved in the src folder require an environment manifest to document the computing environment the code is run in, see the environment manifest section of this module for more information. Subdirectory folders can be customized and added as needed, below are the common directories or data types used in scientific research:

- **notebooks**: Jupyter, Beaker, Zeppelin, WDL, CWL etc.
- **scripts**: custom software, code, tools
- **rules**: for computational workflows
- **test**: unit testing for code, customizable to team needs

<div class = "important">
<b style="color: rgb(var(--color-highlight));">Important note</b><br>
Version Control is important when working collaboratively with access tools like scripts and workflows. For a description of version control and version control systems, see the Arcus Education module, [Intro to version control](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/git_intro/git_intro.md#1)
</div>

**src** files may look different depending on the type of research. Please select which type of data below if you need more information about this directory:

- [ ] omics data
- [ ] clinical data
<script output="data_type_src">"@input"</script>

<script modify="false">
try {
  let data_type = @input(`data_type_src`)

  if(data_type[0]) {
    send.liascript(`## Omics Data

[Workflow Development Language](https://terra.bio/deciphering-a-mystery-workflow-written-in-wdl/) or WDL and [Common Workflow Language](https://www.commonwl.org) or CWL are open standard tools for managing computationally intensive bioinformatics workflows. These are not definitionally programming languages but more clearly and interoperably explain parameters for running complex omics command line operations across bioinformatics pipelines. WDL and CWL are commonly used in bioinformatics pipelines to describe and share data processing and analysis workflows. For example, the diagram below displays a Genomic Data Commons Pipeline that converts reads (CRAM or BAM) to FASTQ and (re)aligns them to the latest human reference genome.

![Genomic Data Commons Pipeline that converts reads (CRAM or BAM) to FASTQ and (re)aligns them to the latest human reference genome ](media/sample_gatk_WDL.png)

Workflows documented in WDL or CWL are incredibly useful for both understanding and recreating a bioinformatics workflow. These scripts should be saved in the _src/notebooks_ directory.

    `)
  } else send.clear()
} catch(e) { }
</script>

<script modify="false">
try {
  let data_type = @input(`data_type_src`)

  if(data_type[1]) {
    send.liascript(`## Clinical Data

Reproducibility in research is a major goal of the Arcus program and organizing and documenting code so that it can be used beyond the confines of the originally collected dataset is critical to achieving this aim. See the [DART Module on Reproducibility in Research](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/reproducibility/reproducibility.md#5) for more information on this topic. Below are some examples of the type of information commonly saved in the _src/_ directory:

- History of saved queries in SQLPad can be extracted directly from the sqlite database into the _src/scripts_ directory
- Code written in the command line interface can be saved in the _src/scripts_ directory
- Work done in the R or Jupyter notebook applications can be saved in _src/notebooks_ directory
- Though Arcus prefers to archive non-proprietary filetypes, some common data analysis programs are not easily exported out of their proprietary formats, such as Stata or SAS. If you work in Stata or SAS, a non proprietary text version of your .dta or .SAS file can be saved in the src folder so that your analysis workflow can be accessed and interpreted by a secondary user. Additionally for Sata and SAS analysis, if possible export the workflow steps as a txt file.

    `)
  } else send.clear()
} catch(e) { }
</script>

## models/

The models directory is for saving any type of machine learning models, model predictions, model summaries, data sheets for model training data. Please consult with the Library Science team on your specific model type for more information about formats and directory structure for archiving.

## references/

This directory contains general information about the research effort such as IRB documents, reference papers, sample information, lab prep information, and data dictionaries. This directory holds the technical information needed to understand the research data. Further subdirectories can be customized depending on the collection.

**references** files may look different depending on the type of research. Please select what type of data you need more information about for this directory:

- [ ] omics data
- [ ] clinical data
<script output="data_type_refer">"@input"</script>

<script modify="false">
try {
  let data_type = @input(`data_type_refer`)
  if(data_type[0]) {
    send.liascript(`
## Omics Data

For Omics data, protocols are the metadata that document the processes, tools and standards used to generate sequencing data. Protocols are important to complete, as the information will be needed for future analysis, pipelines or workflows with the data.

Arcus documents the protocol information in structured [yaml](https://yaml.org/spec/1.2.2/) files. The YAML structure and information captured depends on the sequencing method (such as High-Throughput sequencing, Microarray or Metabolics) and the file type (like FASTQ, CRAM, VCF, etc.). High-Throughput sequencing data includes whole genome sequencing, whole exome sequencing and RNA-seq data. Microarrays include SNP data. A new yaml file should be created whenever the process, tools or standards are different for a set of files. The protocol yaml is linked to the files in the file_manifest.csv file. Below are descriptions of the information requested in the protocols, a template for all of these is downloadable in a public GitHub repository, [arcus/omics-protocols](https://github.research.chop.edu/arcus/omics-protocols). This repository also describes the metadata collected, and provides resources for finding the information needed.

    `)
  } else send.clear()
} catch(e) { }
</script>

<script modify="false">
try {
  let data_type = @input(`data_type_refer`)
  if(data_type[1]) {
    send.liascript(`
## Clinical Data

If you are contributing a dataset, you should include a data dictionary in the _references/_ directory, in a subdirectory titled _data\\_dictionary_. A data dictionary documents the scope, purpose, and nuance of the data you are collecting. Some data dictionaries are extensively detailed, but even a basic minimal data dictionary is better than none at all. Data dictionaries are usually used for tabular datasets, but can be used for data in other formats as well.

Below are the fields often included in your data dictionaries. Only a few are considered truly **required** - the rest are optional but can be extremely helpful, so you should consider whether they make sense to collect in your case. You may also have additional fields to include that are not listed here; you know your data best!

- If your data model follows a specific ontology it is crucial to denote that in your included documentation.
- NIH has fantastic tools through its Unified Medical Language System (UMLS). These include [extensive vocabulary lists of nearly 200 ontologies](https://www.nlm.nih.gov/research/umls/sourcereleasedocs/index.html) and a [metathesaurus application](https://www.nlm.nih.gov/research/umls/knowledge_sources/metathesaurus/index.html) that crosswalks between validated ontologies.

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

#### Sample Data Dictionary from the [PEDSnet Data Contribution](https://chop.alationcloud.com/article/3810/)
<!-- data-type="none" -->

| table_name | field_name               | description                                                                                                | type       | phi | ordinal\\_position | crosswalk\\_needed | crosswalk\\_note |
| ---------- | ------------------------ | ---------------------------------------------------------------------------------------------------------- | ---------- | --- | ---------------- | ---------------- | -------------- |
| person     | person\\_id                | A unique identifier for each person; this is created by each contributing site.                            | BigInteger | 1   | 1                | 1                |                |
| person     | gender\\_concept\\_id        | A foreign key that refers to a standard concept identifier in the Vocabulary for the gender of the person. | Integer    | 0   | 2                | 0                |                |
| person     | gender\\_source\\_concept\\_id | A foreign key to the gender concept that refers to the code used in the source.                            | Integer    | 0   | 3                | 0                |                |

#### Sample Explanation of Tables from the PEDSnet Data Contribution

<!-- data-type="none" -->

| name             | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| adt\\_occurrence   | The adt\\_occurrence table contains information about distinct admission, discharge, or transfer events that occur as part of a clinical visit. The typical use case is to identify portions of an inpatient admission that represent different levels of care or locations within a facility, but it can be used for additional characteristics of a visits (e.g. specialty consultation). The time of each event must fall between the start and end times of the associated visit_occurrence.                                                                                                                                                                                                                                                                                                                                                                    |
| care\\_site        | The Care Site domain contains a list of uniquely identified physical or organizational units where healthcare delivery is practiced (offices, wards, hospitals, clinics, etc.).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| concept\\_ancestor | The CONCEPT\\_ANCESTOR table is designed to simplify observational analysis by providing the complete hierarchical relationships between Concepts. Only direct parent-child relationships between Concepts are stored in the CONCEPT\\_RELATIONSHIP table. To determine higher level ancestry connections, all individual direct relationships would have to be navigated at analysis time. The CONCEPT\\_ANCESTOR table includes records for all parent-child relationships, as well as grandparent-grandchild relationships and those of any other level of lineage. Using the CONCEPT\\_ANCESTOR table allows for querying for all descendants of a hierarchical concept. For example, drug ingredients and drug products are all descendants of a drug class ancestor. This table is entirely derived from the CONCEPT, CONCEPT\\_RELATIONSHIP and RELATIONSHIP tables. |

    `)
  } else send.clear()
} catch(e) { }
</script>

## reports/

The reports directory holds published papers and content used for producing papers, presentations, websites, metrics, etc. It can additionally hold the following information:

- Figures & tables: generated metrics and graphics for supporting reports
- Log.md: computational notebook (if one was used to create the content)
- Methods.md: version controlled methods section for the project
- Further subdirectories can be customized based on the needs of the collection.

## requirements/

- Any module or library dependencies for workflows.
- Additional requirements files can be added as needed.

## configs/

This directory holds configuration files for workflows or applications. Sub-directories can be added as needed for the collection.

### configs/environments

Environment means the analysis environment for a script or model.

- For each script/notebook in src, each model in models, there should be an environment manifest and file that describes the environment in which it was created or run.
- Environment files should be named as follows: descriptiveName_env.\* and placed in a folder called environments within the configs/ directory.
- Either individuals files or entire folders(whichever is the appropriate level) in scripts and notebooks within the src/ directory, the models/ directory, or the data/endpoints folder will need to be added to the env_manifest.csv file, matching them with their related environment file.
- All environmental files should be documented in an environment manifest, see the [manifests/environment manifests](#manifestsenv-manifest) for more information

**Arcus Lab Images**

- There should also be a file named lab-image-tag within a folder titled lab-image within the configs/ directory that contains the tag of the Arcus Lab Image that the Lab was using.
- Though unlikely, if artifacts use more that one image than follow the directions above (in the environments section): add a descriptive name to each lab-image-tag file, and add the file paths and related files or directories to the env_manifest linking them together.

# Concluding Quiz

1. True or False: Data in the raw directory can be edited.

[( )] TRUE
[(X)] FALSE

---

<div class = "answer">

FALSE. This directory holds authoritative source data that should never be deleted. This folder is where the original, unmodified data for the research project is stored.

</div>
***

2. True or False: MRNs are preferred for use as both the local biosample and/or participant id and the authoritative id.

[( )] TRUE
[(X)] FALSE

---

<div class = "answer">

FALSE. MRNs should only be used as the authoritative id in the participant-crosswalk.txt to protect patient privacy and to minimize data leaks.

</div>
***

3. Which folders in the project template are minimally required?

[[]] references
[[]] src
[[X]] data
[[X]] manifests
[[]] configs
[[]] models
[[]] reports
[[]] requirements

---

<div class = "answer">

Only data and manifests are required but more is always better. References and src are probably the two most common non-required folders generated over the course of research.

</div>
***

4. I am contributing a clinical dataset to Arcus. I have a python script that was used to transform my raw datset for further analysis. What directory should this file be saved in?

[[src]]

---

<div class = "answer">

The src or sources folder stores the access tools required to work with the research data and repeat the analysis, like scripts. Remember, any scripts saved in the src folder require an environment manifest to document the computing environment the code is run in, see the [environment manifest page](#manifestsenv_manifestcsv) for more information.

</div>
***
