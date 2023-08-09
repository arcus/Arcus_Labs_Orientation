## data/

- Research data: Information collected during the course of research processes used for analysis
- Maintains descriptions of authoritative source data and their associated files and metadata in both raw and processed formats

### data/raw

- Arcus-delivered data goes here.
- Study team generated data brought into Arcus goes here.
- Authoritative source data that should never be deleted.
- Organize in subdirectories if necessary.

#### data/raw omics example

- Most sequencing providers will generate a [**fastq**](https://maq.sourceforge.net/fastq.shtml) file or [**cram**](https://samtools.github.io/hts-specs/CRAMv3.pdf) file. These files contain genomic sequences called reads. With paired reads, there are two fastq files per sample. Cram files are single files aligned to a reference genome.
- We collect the compressed fastq form fastq.gz, which can be made with lossless compression utility tools like gzip. fastq metadata are described in the fastq directory.
- Cram files are human readable and highly space efficient by using reference-based compression of sequence data. These files enable us to run a complete re-analysis of the data. Cram files require a companion index file, crai.

#### data/raw clinical example

### data/interim

- Managed by study team.
- Unregulated space for intermediate and temporary files.
- Not necessary to save long-term.
- Recommend establishing retention schedules for regular review/clean-up.

### data/interim/ omics example

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

| programming_filegroup | Enter the highest level folder that the environment file relates to. If the file relates to an entire directory, then put the whole direcotry file path. If the file relates to a suddirectory, enter that filepath. If it relates to a single file, enter the file path and filename. |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| related_environment   | Enter the environment filename. Some environment files will be entered multiple times as they relate to multiple files.                                                                                                                                                                |

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
