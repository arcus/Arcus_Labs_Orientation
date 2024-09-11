<!--
author:   Arcus Education
email:    arcus-support@chop.edu
version:  0.0.0
language: en
narrator: US English Female
title: Arcus Quickstart

link:  https://cdn.jsdelivr.net/gh/arcus/Arcus_Labs_Orientation@main/assets/styles.css
link:  https://cdn.jsdelivr.net/gh/arcus/education_modules@main/assets/styles.css
script: https://kit.fontawesome.com/83b2343bd4.js
script: https://cdn.jsdelivr.net/npm/mermaid@9.4.3/dist/mermaid.min.js
-->

## Start a research project with Arcus

To work with data provided by Arcus, you'll need an Arcus Computational Lab (called an Arcus Lab for short).

When you request an Arcus Lab, we evaluate your proposed study to make sure it's a good fit for our service, then build the computational environment and provision the data for your team so you can start work. 
This process takes time and coordination across multiple groups within Arcus. 
Here's what you can do to make the process as smooth as possible: 

- Check first: Is your proposed study a good fit for Arcus?
- Save time: Hone your data request beforehand
- Know the rules: Security, privacy, and the Arcus Terms of Use

### Is your proposed study a good fit for Arcus?

<div style = "background-color:white;">

<script style="display: block" run-once="true" modify="false">
mermaid.initialize({});

var svg = mermaid.render(
'arcus_fit_flowchart',
`flowchart TB
 accTitle: Is your proposed study a good fit for Arcus?
 accDescr: In order for your proposed study to be a good fit for Arcus, everyone on your team must have CHOP login credentials, your proposed project must be research, your project must involve human data, and your team must be prepared to work with Arcus tools. 
  A[Does everyone on your team\\nhave CHOP login credentials?] --Yes--> B[Is your proposed project research?];
  A --No--> C([Arcus is likely\\nnot a good fit]);
  B --Yes--> D[Does your project involve human data?];
  D --Yes--> E[Is your team prepared\\nto work with Arcus tools?]
  E --Yes---> F([Your project is likely\\na good fit for Arcus!]);
  B --No--> C;
  D --No--> C;
  E --No--> C;
`,
function(g) {
    return true;
})

"HTML: " + svg
</script>

</div>

**Does everyone on your team have CHOP login credentials?**
Anyone who will need access to the data has to have CHOP credentials. 
You will not be able to share the data with outside collaborators unless they first get NTP status with CHOP.
You will not be allowed to export data from your Arcus Lab; everyone who needs access to the data will have to log into your Arcus Lab using their CHOP credentials. 
It's okay to start the request for your Arcus Lab before all of the non-CHOP workforce members of your team have obtained NTP status, but keep in mind that any delays in the NTP process may delay delivery of your Arcus Lab. 

**Is your proposed project research?**
Arcus is funded by CHOP's Research Institute, so we don't support non-research projects (such as operational analysis). 
If you want to analyze data for something other than research, contact [DnA]() instead. 

**Does your project involve human data?**
We don't support non-human research. 
Human data includes things like electronic health records, data from research with human subjects, public data on humans (such as Census data), human biosamples and genomics data, etc.
We also welcome projects that analyze human data together with other sources of data. 
But if all of your data sources are from animal models or another kind of non-human data, Arcus is not a good fit.

**Is your team prepared to work with Arcus tools?**
Arcus provides access to *raw* data.
Your team will likely need to do substantial data cleaning work before you can analyze the data to answer your research question. 
You will need one of the following: 

- Someone on your team who is ready to do the data cleaning and analysis work using the [tools in an Arcus Lab]()
- Someone on your team with the time and motivation to learn to use Arcus tools, with the support of [Arcus Education]()
- Funding for data cleaning and analysis support, such as from [the Collaborative Research Units (CoRU)]()

If you do not have any of the above, Arcus is not a good fit for your project.

### Hone your data request beforehand

### Security, privacy, and the Arcus Terms of Use
