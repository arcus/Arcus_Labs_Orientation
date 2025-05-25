<!--
author:   Arcus Education
email:    arcus-support@chop.edu
version:  1.0.0
language: en
narrator: US English Female
title: Arcus Quickstart

link:  https://cdn.jsdelivr.net/gh/arcus/Arcus_Labs_Orientation@main/assets/styles.css
link:  https://cdn.jsdelivr.net/gh/arcus/education_modules@main/assets/styles.css
script: https://kit.fontawesome.com/83b2343bd4.js
script: https://cdn.jsdelivr.net/npm/mermaid@9.4.3/dist/mermaid.min.js
-->

# Arcus Labs: Quick Start

Ready to start a research project with Arcus, or have you been given a computational lab and want to know what to do next? This quick start guide will jump start your Arcus journey! 

If you have questions about Arcus Labs that aren't answered here, please see our [Arcus Lab User Guide](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/arcus_orientation.md#1) for more detailed documentation.

What is an Arcus Lab?
---
An Arcus Lab is a resource provided through the Research Institute in which data from various sources (including research datasets and data from the electronic health record) can be collected in one secure computational environment alongside a variety of useful tools for the analysis of those data. 

The goal is to provide you, the researcher, with an environment that supports reproducible data analysis projects and simplifies sharing research insights, cohorts, data, and methods, so that you can get the most out of your data!


## Start a research project with Arcus

To work with data provided by Arcus, you'll need an Arcus Computational Lab (called an Arcus Lab for short).

When you [request an Arcus Lab](https://support.arcus.chop.edu/servicedesk/customer/portal/6/create/307), we evaluate your proposed study to make sure that our services are a good fit for your project, then build the computational environment and provision the data for your team so you can start work. 
This process takes time and coordination across multiple groups within Arcus. 
Here's what you can do to make the process as smooth as possible: 

<div class = "version-update">

- Check first: [Is Arcus a good fit for your proposed study?](#is-arcus-a-good-fit-for-your-proposed-study%3F) 
- Save time: [Hone your data request beforehand](#hone-your-data-request-beforehand)
- Know the rules: [Security, privacy, and the Arcus Terms of Use](#security%2C-privacy%2C-and-the-arcus-terms-of-use)

</div>

### Is Arcus a good fit for your proposed study?

<div style = "background-color:white;">

<script style="display: block" run-once="true" modify="false">
mermaid.initialize({});

var svg = mermaid.render(
'arcus_fit_flowchart',
`flowchart TB
 accTitle: Is Arcus a good fit for your proposed study?
 accDescr: In order for Arcus to be  a good fit for your proposed study, everyone on your team must have (or be able to get) CHOP login credentials, your proposed project must be research, and your team must be prepared to work with Arcus tools. 
  A[Does everyone on your team have,\\nor can acquire through NTP status,\\nCHOP credentials?] --Yes--> B[Is your proposed project research?];
  A --No--> C([Arcus might not be the best fit, but we\\nencourage you to reach out for a conversation\\nabout how we might meet your needs.]);
  B --Yes--> D[Is your team prepared to clean and\\nanalyze your data using Arcus tools,\\nor hire someone who is?]
  D --Yes---> E([Arcus is likely a good\\nfit for your project!]);
  B --No--> C;
  D --No--> C;
`,
function(g) {
    return true;
})

"HTML: " + svg
</script>

</div>

Let's go into a bit more detail about each of these questions. 

#### Does everyone on your team have CHOP login credentials?
Anyone who will need access to the data in an Arcus Lab will need to have CHOP credentials. 
You will not be able to share the data with outside collaborators unless they first [get NTP status](https://forum.arcus.chop.edu/t/can-someone-from-outside-of-chop-be-a-collaborator-in-an-arcus-lab/779) with CHOP. Be sure to advise your collaborator to check both the email they provide to get NTP status **and** their new CHOP email for updates!

Additionally, you will not be allowed to export data from your Arcus Lab; everyone who needs access to the data will have to log into your Arcus Lab using their CHOP credentials. However, you **can** start the request for your Arcus Lab before all of the non-CHOP workforce members of your team have obtained NTP status! Just keep in mind that any delays in the NTP process may delay delivery of your Arcus Lab. 

#### Is your proposed project research?
Arcus is funded by CHOP's Research Institute, so we don't support non-research projects (such as operational analysis). 
If you want to analyze data for something other than research, contact the [Data Trust & Enablement team](https://chop365.sharepoint.com/sites/DataTrustEnablement) instead. 

#### Is your team prepared to clean and analyze your data using Arcus tools?
Arcus provides access to *raw* data.
Your team will likely need to do substantial data cleaning work before you can analyze the data to answer your research question. 

You will need at least one of the following: 

- Someone on your team who is ready to do the data cleaning and analysis work using the [tools in an Arcus Lab](https://forum.arcus.chop.edu/t/what-applications-are-available-in-arcus-labs/781)
- Someone on your team with the time and motivation to learn to use Arcus tools, with the support of [Arcus Education](https://arcus.chop.edu/i-want-to/arcus-education)
- Funding for data cleaning and analysis support, such as from the [Clinical Reporting Unit (CRU)](https://www.research.chop.edu/clinical-reporting-unit), the [Data Science and Biostatistics Unit (DSBU)](https://www.research.chop.edu/data-science-and-biostatistics-unit), or the [Translational Research Informatics Group (TRiG)](https://www.research.chop.edu/dbhi-translational-informatics) (collectively, these groups are also known as the Collaborative Research Units, or CoRU)

If you do not have any of the above, Arcus may not be the best fit for your project.

### Hone your data request beforehand
While Arcus staff will meet with you after you have proposed your project in order to establish exactly what data you'll need to answer your research question, you can speed up this process by defining your research question and cohort in advance. Arcus has tools for this, such as the [Cohort Discovery Tool](https://arcus.chop.edu/apps/cohort-discovery), the [Clinical Data Query application](https://arcus.chop.edu/apps/clinical-data-query), and [Gene, CHOP's Data Catalog](https://chop.alationcloud.com/). However, if you'd like some help with this process, don't hesitate to [reach out to the Arcus Data Team](https://outlook.office365.com/owa/calendar/ArcusDataRepositoryOfficeHours@CHOP365.onmicrosoft.com/bookings/). 

### Security, privacy, and the Arcus Terms of Use
The first thing you'll need to do before you get access to an Arcus lab, it's important that you familiarize yourself with and sign the [Arcus Terms of Use](https://arcus.chop.edu/terms-of-use). 

Additionally, before you can see any data or get access to an Arcus lab, you'll need to make sure that you are authorized to have access to the data that you are requesting. This means you'll either need IRB approval for your study or a determination that IRB oversight is not required because your study is not considered human subjects research (like if your are using certain de-identified datasets, for example). To help you with this process, Arcus has written some [sample language to include in your IRB submissions and grant applications](https://arcus.chop.edu/web-static/documents/Arcus_Grant_Language.pdf).


## Using your Arcus Lab

So once your project has been approved and you have an Arcus lab, what then? 
We also have many resources to help you get the most out of your Arcus lab. 

### Learn to use the tools in your lab

Your Arcus Lab is a flexible and powerful platform.
For a list of available tools and options, see [Arcus Lab Options Overview](https://forum.arcus.chop.edu/t/arcus-lab-options-overview/840).
Arcus Education provides support to researchers learning to use the tools in their Arcus Lab. 

You'll find short, practical video tutorials on your lab's dashboard, in the **Education Resources** section, to help you get started. 
Be sure to check them out!
For example, the three videos below (only available if you're on CHOP's network) answer many of the most common questions we see from new Arcus researchers.

!?[Introduction to SQLPad](https://assets.arcus.chop.edu/arcus_education_assets/training_lab_videos/sqlpad_captioned.mp4)
!?[Introduction to Python and Jupyter](https://assets.arcus.chop.edu/arcus_education_assets/training_lab_videos/python_jupyter_captioned.mp4)
!?[Introduction to R and RStudio](https://assets.arcus.chop.edu/arcus_education_assets/training_lab_videos/r_rstudio_captioned.mp4)

For a more general overview, we suggest you check out our "New to" documents:

- **[New to data science](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_to_data_science.md#1)** is a document that introduces helpful tools and tips for working on data science projects that will be useful to scientists coming from other types of research. Even if you have experience in data science already, you may find it worthwhile to skim the subtopics in that section so you know what's available should you want to come back to it to reference later.
- **[New to version control](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_to_version_control.md#1)** is a document that will help you get started with git, a powerful program for helping you keep track of your research documents over time. If you don't currently use git or another form of version control, we strongly recommend you work through that section. Version control is an extremely valuable tool for reproducible research, and although there is a bit of a learning curve, it really pays off.
- **[New to GitHub](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_to_version_control.md#1)** covers the difference between Git, the popular version control system, and GitHub, a website for hosting Git repositories. CHOP researchers also have access to a special version of GitHub, CHOP's Enterprise GitHub. This guide explains your options and walks through exploring a repository on CHOP's Enterprise GitHub, as well as how to create your own repository and connect it to your Arcus Lab.
- **[New to SQL](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_to_sql.md#1)**, **[New to R](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_to_r.md#1)** and **[New to Python](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_to_python.md#1)** are documents that introduce you to the three languages most important to your work in an Arcus Lab: SQL, R, and python. You will need at least some familiarity with SQL in order to access any tabular data in your lab (data that takes the forms of rows and columns). Depending on your research needs, you can pick whether to learn Python or R or use some of both. If you're new to SQL, R, and Python, we recommend you focus on SQL first, since that's the first thing you'll need to be able to apply in your own lab.
- **[New to Omics](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_to_omics.md#1)** will get you started if you're using the Arcus Omics Training Lab. The instructions in this document presuppose that specific files, containing pre-defined data, exist and that you're working in the Omics Training Lab.
- **[New to Text Data](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/new_to_text.md#1)** is a very cursory introduction to some topics related to working with text data.

### Get 1:1 support

[Schedule office hours, an educational consultation, or a lab walkthrough with Arcus Data Education](https://outlook.office365.com/book/BKG-StandardArcusEducationOfficeHours@chop.edu/), where you can talk with an Arcus Data Science Educator about your specific questions.

### Attend an Arcus On-Ramp workshop

We offer a regular rotation of Arcus On-Ramp workshops, all featuring hands-on practice with real data in an Arcus lab. 
If you're new to Arcus, these workshops are a great way to get up to speed fast.

**Important note:** Because these workshops involve work with real (deidentified) patient data, you need to have completed CITI training and attested the Arcus terms of use before you can attend. 
If you're unsure if you've met both requirements, you can [check your Arcus status online](https://arcus.chop.edu/access-status). 

[Sign up to attend an Arcus On-Ramp workshop](https://arcus.chop.edu/education/webinar-signup#).

The notebooks we use for the workshops are also available online (you'll need to be on CHOP's network to access them), so you can work through that content on your own and/or return to review it after attending a workshop:

- [Retrospective EHR Analysis: Build the SQL Query](https://github.research.chop.edu/arcus/notebooks/blob/onramp_patient_encounter/arcus_on_ramp/Build_SQL_query.md)
- [Retrospective EHR Analysis: Analysis in R](https://github.research.chop.edu/arcus/notebooks/blob/onramp_patient_encounter/arcus_on_ramp/Analyze_in_R.Rmd)
- [Retrospective EHR Analysis: Analysis in Python](https://github.research.chop.edu/arcus/notebooks/blob/onramp_patient_encounter/arcus_on_ramp/Analyze_in_Python.ipynb)

### Arcus Users Group

Connect with Arcus staff and other Arcus users in our [Arcus Users Group](https://teams.microsoft.com/l/team/19%3AUa9xxH-Wc6tcXYT0Ju3M-6M_f0yk4yR2qcAbIPF16hM1%40thread.tacv2/conversations?groupId=00909f4a-1401-46fd-9f0a-531498e1aef6&tenantId=a6112416-07b0-41a5-9bb1-d146b575c975).



