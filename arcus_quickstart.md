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

- Check first: Is Arcus a good fit for your proposed study? 
- Save time: Hone your data request beforehand
- Know the rules: Security, privacy, and the [Arcus Terms of Use](https://arcus.chop.edu/terms-of-use).

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
- Funding for data cleaning and analysis support, such as from the [Clinical Reporting Unit (CRU)](https://www.research.chop.edu/clinical-reporting-unit), the [Data Science and Biostatistics Unit (DSBU)](https://www.research.chop.edu/data-science-and-biostatistics-unit), or the [Translational Research Informatics Group (TRiG)](https://www.research.chop.edu/dbhi-translational-informatics) (collectively, these groups are also known as the Collaborative Research Units, or CoRU).

If you do not have any of the above, Arcus may not be the best fit for your project.

### Hone your data request beforehand
While Arcus staff will meet with you after you have proposed your project in order to establish exactly what data you'll need to answer your research question, you can speed up this process by defining your research question and cohort in advance. Arcus has tools for this, such as the [Cohort Discovery Tool](https://arcus.chop.edu/apps/cohort-discovery), the [Clinical Data Query application](https://arcus.chop.edu/apps/clinical-data-query), and [Gene, CHOP's Data Catalog](https://chop.alationcloud.com/). However, if you'd like some help with this process, don't hesitate to [reach out to the Arcus Data Team](https://outlook.office365.com/owa/calendar/ArcusDataRepositoryOfficeHours@CHOP365.onmicrosoft.com/bookings/). 

### Security, privacy, and the Arcus Terms of Use
The first thing you'll need to do before you get access to an Arcus lab, it's important that you familiarize yourself with and sign the [Arcus Terms of Use](https://arcus.chop.edu/terms-of-use). 

Additionally, before you can see any data or get access to an Arcus lab, you'll need to make sure that you are authorized to have access to the data that you are requesting. This means you'll either need IRB approval for your study or a determination that IRB oversight is not required because your study is not considered human subjects research (like if your are using certain de-identified datasets, for example). To help you with this process, Arcus has written some [sample language to include in your IRB submissions and grant applications](https://arcus.chop.edu/web-static/documents/Arcus_Grant_Language.pdf).


## Using your Arcus Lab
So once your project has been approved and you have an Arcus lab, what then? We also have many resources to help you get the most out of your Arcus lab. 

- [Learn to use the tools in your lab](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/Arcus_Labs_Orientation/main/arcus_orientation.md#6) by checking out our educational modules.

- [Schedule office hours, an educational consultation, or a lab walkthrough with Arcus Data Education](https://outlook.office365.com/book/BKG-StandardArcusEducationOfficeHours@chop.edu/), where you can work with a Data Educator about your specific questions.

- [Attend an Arcus On-Ramp workshop](https://arcus.chop.edu/education/webinar-signup#), where you can see an Arcus lab in action using real EHR data. 

- Connect with Arcus staff and other Arcus users in our [Arcus Users Group](https://teams.microsoft.com/l/team/19%3AUa9xxH-Wc6tcXYT0Ju3M-6M_f0yk4yR2qcAbIPF16hM1%40thread.tacv2/conversations?groupId=00909f4a-1401-46fd-9f0a-531498e1aef6&tenantId=a6112416-07b0-41a5-9bb1-d146b575c975).



