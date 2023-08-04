## data/

- Research data: Information collected during the course of research processes used for analysis
- Maintains descriptions of authoritative source data and their associated files and metadata in both raw and processed formats

### data/raw

- Arcus-delivered data goes here.
- Study team generated data brought into Arcus goes here.
- Authoritative source data that should never be deleted.
- Organize in subdirectories if necessary.

#### data/raw omics example

#### data/raw clinical example

### data/interim

- Managed by study team.
- Unregulated space for intermediate and temporary files.
- Not necessary to save long-term.
- Recommend establishing retention schedules for regular review/clean-up.

### data/endpoints

- Managed by study team.
- Final results from research analysis.
- Files generated to support papers or grants.
- Organize in subdirectories if necessary.

#### data/endpoints omics example

#### data/endpoints clinical example

### data/ref-data

- External or public datasets not supplied by Research IS or your lab, such as census data.

#### data/ref-data/platform_data omics example

## manifests/

- Managed by Arcus
- Inventory of all raw & endpoint data
- Inventory of all participants and their related cohorts/samples/family roles, as applicable.
- Associates IDs with all data files.
- Documents relationships between files in pipelines/workflows.

### manifests/file_manifest omics examples

### manifests/file_manifest clinical example

### manifests/participant_manifest omics example

### manifests/participant_manifest clinical example

### manifests/participant_crosswalk

### manifests/participant_family_role omics example

### manifests/file_derivation.csv

### manifests/env_manifest.csv

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

### references/protocols omics examples

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
