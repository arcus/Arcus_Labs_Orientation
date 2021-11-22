# How to use this guide

**If you're here because you've just started your first Arcus Lab:**

Congratulations! This goal of this guide is to get you up and running with your new lab, regardless of your research background and expertise.

Everyone should start with the **Quickstart** section, since that will bring you up to speed fast on what to expect when you first open your lab and how to get started. If you're already comfortable with data science tools like SQL, R, python, and version control, then the Quickstart section may be enough to get you going. Most researchers will benefit from working through some or all of the other sections as well, though.

- **New to data science** introduces helpful tools and tips for working on data science projects that will be useful to scientists coming from other types of research. Even if you have experience in data science already, you may find it worthwhile to skim the subtopics in that section so you know what's available should you want to come back to it to reference later.
- **New to version control** will help you get started with git, a powerful program for helping you keep track of your research documents over time. If you don't currently use git or another form of version control, we strongly recommend you work through that section. Version control is an extremely valuable tool for reproducible research, and although there is a bit of a learning curve, it really pays off.
- **New to SQL**, **New to R** and **New to python** introduce you to the three languages most important to your work in an Arcus Lab: SQL, R, and python. You will need at least some familiarity with SQL in order to access your data, but you can pick whether to learn python or R. If you're new to SQL, R, and python, we recommend you focus on SQL first, since that's the first thing you'll need to be able to apply in your own lab.

As you learn about your lab, save a record of your studies and which resources are most valuable for your group. This can be a google doc, notebook, etc., whatever works best for you to keep track of your studies. If you like, you can start by copying this orientation document and then adding your own notes and deleting or editing parts that aren't useful to your group. **You'll find a copy of this document in your Arcus lab --- it's there for you to edit and make your own.** This is a markdown document; feel free to just write in it however you like and ignore the formatting, or if you want to learn markdown formatting, you can do so very quickly. It is a simple system that lets you add basic formatting to plain text documents, and there is a [great cheatsheet here](https://daringfireball.net/projects/markdown/basics). No matter how you take notes, the goal is to compile a personalized list of tips and resources that you'll be able to go back to for you own reference and/or to train others in your lab.

**If you don't have an Arcus lab and you're just here to browse and learn:**

Welcome! All of the examples here are designed for Arcus Labs, but much of this material is broadly applicable, even to folks who aren't working with Arcus. We hope you find it helpful. If you would like to learn more about what Arcus is and what we do, check out this [overview video](https://digitalrepository.chop.edu/arcus/1/) or this [Arcus-101 guide](https://education.arcus.chop.edu/guides/arcus-101/).

# Quickstart

This is a quick overview of an Arcus lab. What it covers:

- What to expect: Timeline for starting a new lab
- Using your lab
- Requesting data for your lab
- Ongoing communication
- Overview of tools in your lab
- How to set up your project

What the quickstart guide does NOT cover:

- How to write SQL queries to access your data
- How to analyze your data in R or python
- How to use Jupyter notebooks or R-markdown notebooks to document your analysis code
- How to use version control on your lab files
- Explanations of **why** you would want to do any of the above rather than using more traditional tools like Excel, SAS, or Stata

These topics (and more!) are part of the more extended overview (especially "[New to data science?](new-to-data-science)"), which will be especially useful to researchers coming to Arcus without previous experience in data science.  

## Training lab vs. computational lab

There are two kinds of labs available from Arcus, and they serve very different purposes.

The first is computational labs, also called scientific labs. These are secure computational environments built for a specific team to conduct research. These are custom-built and there is a detailed approval process for use. For a more detailed explanation, see [the Arcus Computational Labs job aid](https://arcus-education-internal.s3.amazonaws.com/job-aids/arcus-lab-job-aid.pdf). Computational labs are also the focus of the rest of this guide.

The second type of lab is a training lab. These are just like computational labs except they are **not** intended for conducting research, and therefore have both limited resources and a very fast approval process. Training labs do provide access to real patient data, but only in **deidentified** form and **not the whole database of patients**. The goal of training labs is to create a space where researchers can do quick proof-of-concept checks before starting a full research program, and to give potential Arcus users a chance to try the system out. For a more detailed explanation, see the [Arcus training labs job aid](https://assets.arcus.chop.edu/education/job-aids/arcus-training-lab.pdf).


## What to expect: Timeline for starting a new computational lab

This section covers the typical stages from initial request to deployment of a new Arcus computational lab. If you aren't interested in this process, or if you already have a lab ready, you may wish to skip directly to this section's [knowledge check](#knowledge-check-1).

### The initial request

Your first point of contact with Arcus may be informal conversations with one or more Arcus staff members to determine whether or not your project would be a good fit, or you may go directly to [submitting a request for a new scientific project](https://pm.arcus.chop.edu/servicedesk/customer/portal/1) (note that you need to be behind CHOP's firewall to submit a request).

### Review and assessment

When you submit a request for a lab, it goes through a preliminary review and then a more formal project assessment before your lab is created and made available to you.

The preliminary review is just to determine whether or not to engage in the full project assessment.

If your request is greenlighted for assessment, then you will be assigned a Project Owner among the Arcus staff who will help guide you through the project assessment. The goal of the project assessment is to clarify the needs for the project to make sure that it is something Arcus will be a good fit for.

A major goal of the project assessment is to identify what, specifically, the scientific team will need from Arcus in terms of data, software, training, and support. One component of the project assessment is a **data needs assessment**, to discuss the definition of the cohort to be studied and what information on those patients will be needed (e.g. diagnoses, medications, notes, procedures, demographics, flowsheets). There will also be a **data contribution assessment** to discuss possible data contributions to the [Arcus Archives](https://education.arcus.chop.edu/arcus-data-catalog/) at the end of the project; researchers using Arcus are expected to contribute their data when appropriate ([read more about the data contribution process here](https://assets.arcus.chop.edu/education/job-aids/arcus-data-sharing-sop.pdf)).
The project assessment will also include a **privacy review** to identify and mitigate any potential privacy risks ([read more about the privacy review here](https://discourse.arcus.chop.edu/t/what-is-a-privacy-review-and-what-does-the-process-entail/190)).

The project assessment can vary greatly in length, with particularly well-defined and straightforward projects being assessed in a matter of days and more complex projects or projects that are still in early stages of development taking months. For researchers working under a deadline (e.g. for a grant application), Arcus will try to accommodate your timeline; one of the first questions your Project Owner will ask you during the project assessment is if there are any time constraints we should be aware of.

### Access to Arcus

Before your lab can be approved, everyone who will have access to your lab will need to have verification of their CITI training on file (this is a requirement for all Arcus users and will be the case even if you'll only be accessing deidentified data). They will also need to agree to the Arcus Terms of Use.

To check that they meet these requirements, everyone who will need access to your lab should go to [https://arcus.chop.edu](https://arcus.chop.edu) (only accessible behind CHOP's firewall) and log in with their CHOP credentials using the button in the top right corner of the screen. If your CITI training is on file and you've agreed to the Terms of Use, then you should see two green checkmarks under "Your Account".

![Arcus home screen showing green checkmarks for CITI training and Arcus Terms of Use](media/Arcus_login.png)

### When your lab is approved

When the project assessment is complete and your lab is approved, then the team of Arcus developers will build a computational lab environment for you, based on the needs determined during your project assessment.

When the lab is built, the Arcus data team will provision your lab with the required data, as determined during your project assessment. For more information about the data in Arcus, see [requesting data for your lab](#requesting-data-for-your-lab).

You'll receive an email letting you know when your lab is available, and providing the URL for you to access your lab. Your Project Owner can meet with you and your team to introduce you to the lab environment.

### Knowledge check 1

True or False: In most cases, your new Arcus lab will be made available to you immediately after your request.

[( )] True
[(X)] False
***
> There is a preliminary review and then a more detailed project assessment to determine whether or not Arcus can support your project before your lab will be issued.
>
> Note that if you're on a tight timeline, Arcus may be able to work with you to speed things up. Talk to your Project Owner.
***

Which of the following are required to access **identified** patient data via Arcus? Select all that apply.

[[X]] CITI training on human subjects research
[[X]] read and agree to the Arcus Terms of Use

Which of the following are required to access **deidentified** data via Arcus? Select all that apply.

[[X]] CITI training on human subjects research
[[X]] read and agree to the Arcus Terms of Use
***
> Everyone who will use your lab must have CITI training on file in order to access Arcus, regardless of the nature of the research.
***

Which of the following best describes Arcus data contributions?

[( )] Researchers using Arcus will have the option to contribute their data at the end of the project if they wish to do so
[(X)] Researchers using Arcus are required to contribute their data unless it would be inappropriate to do so
[( )] Researchers using Arcus are required to contribute their data unless it would be inappropriate to do so, and for the data immediately available to other Arcus users without access restrictions
***
> Researchers using Arcus are expected to contribute their data to the Arcus Archive, but there are a number of options in place to restrict access as appropriate, including the option to place a purpose-specific embargo or require approval according to scientific review criteria before access.
>
> During your project assessment, you will meet with an archivist from the Arcus team to discuss potential data contributions from your project, and they will work with you to come up with an appropriate data storage and reuse plan. [See this job aid for more information about data contributions to Arcus](https://assets.arcus.chop.edu/education/job-aids/arcus-data-sharing-sop.pdf).  
***

## Using your lab

Your Arcus lab is a secure computational environment that exists in your browser. You don't need to download or install anything, you (and your team members) just go to your lab's URL and you'll have everything you need there to access and analyze your data. Note that you always need to be behind CHOP's firewall to access your lab.

### What's in your lab

When you go to your lab's URL, you will be prompted to log in with your CHOP credentials. Then you will see the landing page for your lab.

![An Arcus lab landing page](media/lab_landing_page.png)

#### Project Members

In the top left corner, you'll see a list of approved users for your lab. This will include everyone on your research team, your Project Owner, all of the members of the Arcus Education team (Arcus Education staff help with training and troubleshooting for all of the scientific labs), and any other Arcus staff associated with your project.

If you notice someone missing from that list who should have access, or if you see someone you don't think should have access, alert your Project Owner.

#### Lab status

When your lab is running, you'll see a clock counting down until it will shut down. Labs cost a fair amount of computational power when they're running, so they are set to automatically pause after a period of time to save resources. If you need to keep your lab active for longer than that, you can always extend the time.

![An Arcus lab currently running, showing clock](media/lab_clock.png)

If you finish using your lab before the clock runs out, please pause your lab using the button in the top right corner of your screen.

![Pause lab button at the top right corner of Arcus Lab landing page](media/pause.png)

#### The lab environment

The top right part of the screen includes links to the tools in your lab environment itself. When you first access your lab, the tools will be greyed out with a note letting you know that your lab is paused. If you click on the tool section, it will load your lab. Note that it may take a moment for your lab to load.

Once your lab is running, you can open any of the tools by clicking on them.

You won't see any data files in your lab when you log in; instead, you will be able to access the data via SQL queries and bring it into an analysis environment (e.g. using R or python). For initial exploration of your data, SQLPad is probably the best place to start. You can see examples of how to access your data via SQLPad, RStudio, and python Jupyter notebooks in the [training videos](#training-videos).

#### Training videos

This is a very important section for new Arcus users.

Beneath the lab environment links, you will see a list of training videos available. These step through everything you need to get started in your lab. If you are new to Arcus, you will likely find most of your questions answered in these training videos.

![Arcus Education training videos](media/training_videos.png)

Topics currently covered in the training videos include:

- Logging in
- Data dictionaries and intro to SQLPad
- Obtaining data in SQLPad
- Saving queries in SQLPad
- Ingesting and analyzing data in Jupyter
- Ingesting and analyzing data in RStudio
- Working with files using a file browser


### Knowledge check 2

Which of the following best describes an Arcus lab?

[( )] Your Arcus lab is a secure environment for you to access data, which you can then download and analyze on your computer
[( )] Your Arcus lab is a piece of software you will have to install on your machine to be able to use
[(X)] Your Arcus lab is a secure environment for you to access and analyze your data within your web browser without downloading or installing anything
***
> An Arcus lab is a secure computational environment that exists in your browser, so you don't have to install any software on your computer to be able to use it. You access and analyze your data all within this secure environment.
>
> Note that "the systems and tools developed for Arcus are designed to further your work while protecting patient/study subject privacy and institutional security" (from the [Arcus Terms of Use](https://arcus.chop.edu/terms-of-use)). You may not download the data to analyze or store elsewhere.
***

True or False: Each member of your team will have their own Arcus lab, but they'll all have access to the same data.

[( )] True
[(X)] False
***
> You will have one URL for your lab, and each member of your team will access it there.
>
> Each team member will have personal folders within the lab that they can use to save work in progress or personal notes, but we strongly recommend that
***

Which of the following is available on the landing page for your Arcus lab? Select all that apply.

[[X]] A list of the people who have access to your lab
[[ ]] A summary of your data files
[[X]] A clock showing time remaining until your lab pauses
[[X]] A list of training videos that show you how to get started in your new lab
[[X]] Links to open the software available to use in your lab
[[X]] A link to the Arcus Help Center
***
> Remember that you won't directly see your data in your lab (on the landing page, or in the applications). To access your data you need to use SQL queries to bring it into your analysis environment.
***

If you're new to Arcus, what is the best place on the landing page to start?

[[the training videos]]
[[?]] Hint: Check [this section](#training-videos) again.
<script>
  let input = "@input".trim();
  /video/i.test(input);
</script>
***
> The [training videos](#training-videos) walk through everything you need to get started in your lab. Most questions new users have are covered in those videos.  
***

## Requesting data for your lab

An initial data needs assessment takes place during the [project assessment](#review-and-assessment), which will determine the data that is provisioned to your lab to start. However, many researchers find that they need to modify their data request at some point during the life of their project. For both the initial data needs assessment and any further data requests, there are a number of useful tools in place.

You can work on defining your [clinical cohort](https://education.arcus.chop.edu/arcus-clinical-cohorts/) by using the [Arcus cohort discovery tool](https://assets.arcus.chop.edu/education/job-aids/arcus-cohort-discovery.pdf). If you need help using Arcus cohort discovery, you can ask your Project Owner or submit a ticket at the [Arcus Help Center](https://pm.arcus.chop.edu/servicedesk/customer/portal/6/create/63) for assistance.

To explore the tables and variables available in the [Arcus Data Repository (ADR)](https://education.arcus.chop.edu/arcus-data-repository/), you can use the [ADR Data Model Browser](adr-mdm.arcus.chop.edu). Note that the data model browser is most useful for folks who have already built some familiarity with the ADR --- if you're still finding your way around, then please reach out to Arcus staff for help deciding which tables and variables you will need.

You are not limited to what's in the ADR! Many researchers bring in other data sources to analyze in Arcus. Talk to your Project Owner about any additional data needs (genomics data, [images](https://pm.arcus.chop.edu/servicedesk/customer/portal/6/group/50), data from other previous or ongoing research projects, etc.).

When you are ready to place a request for additional data, you may do so through the [Arcus Help Center](https://pm.arcus.chop.edu/servicedesk/customer/portal/6/create/188). Keep in mind that all data requests are subject to review by the privacy team.

### Knowledge check 3

True or False: Each Arcus computational lab provides access to all of the data in the Arcus Data Repository (ADR)

[( )] True
[(X)] False
***
> Each Arcus lab is provisioned just with the data required for that project as determined in the data needs assessment. If you find you need additional data, you can always request more.
***

True or False: Arcus labs are limited to analysis of data from the ADR.

[( )] True
[(X)] False
***
> Although Arcus makes access to the ADR very easy, it's not your only option! Most researchers use a combination of ADR data and data from other sources.
***

True or False: The Arcus Data Repository (ADR) contains everything from Epic Clarity.

[( )] True
[(X)] False
***
> The ADR is a streamlined selection of information from Epic Clarity, not the entire thing. It includes the patient information most commonly requested by researchers (a sort of "greatest hits" of electronic health records), such as demographics, diagnoses, medications, encounters, etc.
>
> If you're used to working in Epic, this means there will be fields you're used to seeing that won't be in the ADR. If you want information that's not in the ADR, just ask and the Arcus data team should be able to add it to your lab for you.
***

## Ongoing communication

Once you have an approved lab request, your primary point of contact is your assigned **Project Owner**. This person will be an Arcus staff member, and their role is to act as a concierge connecting you with troubleshooting support and training to help make your scientific project experience a success. Whenever you have questions, reaching out to your Project Owner is a good place to start.

There are also a number of other ways for you to contact Arcus for support, including submitting a ticket in the help center and posting a question on Discourse.

The **Arcus Help Center** ([https://support.arcus.chop.edu/](https://support.arcus.chop.edu/)) is the system Arcus uses to organize and track requests from lab users and issues that need to be resolved. There is a link to the Arcus Help Center on your lab's landing page, in the top left section titled "[Lab status](#lab-status)". The Help Center is especially useful for defined, specific issues, such as the following:

- submitting a bug report if you think something is malfunctioning in your lab
- requesting a new user be added to your lab
- requesting additional data be supplied to your lab, including images
- requesting lab enhancements, such as additional memory

You can also submit general help questions there, although if you're not sure where to start, talking with your Project Owner first may be more efficient. You need to be behind CHOP's firewall to access the Arcus Help Center.

**Arcus Discourse** ([https://discourse.arcus.chop.edu/](https://discourse.arcus.chop.edu/)) is a question-and-answer site (it uses the same format as [StackOverflow](https://stackoverflow.com/), for those familiar with that). Users can post questions there, and Arcus staff will generally respond with answers very quickly during normal working hours. See this section for [tips on how to post a troubleshooting question to maximize the chance of getting a useful response](link). Arcus staff also use Discourse to post announcements about technical updates and fixes to labs, as well as how-to guides for frequently asked questions. You need to be behind the CHOP firewall to access Arcus Discourse.

### Knowledge check 4

Which of the following best describes the role of the Project Owner?

[( )] They are the lead researcher on the project
[(X)] They act as a reference and point of connection between the project researcher(s) and Arcus staff
[( )] They are available to assist with research project tasks like writing and checking code
***
> The Project Owner acts as a concierge, connecting scientific project users with the right Arcus staff to resolve their issues, and checking to make sure the project is progressing smoothly.
>
> Project Owners don't assist with research tasks like writing code or analyzing data, although they can help connect researchers to training and resources so they can do those things themselves.
***

True or False: The only way you should get in touch with Arcus is via your Project Owner.

[( )] True
[(X)] False
***
> Although your Project Owner is often the best place to start, you are welcome to get in touch with other Arcus staff in whatever way works best for you. Two useful avenues are the Arcus Help Desk and the Arcus Discourse site.
***

If the data in your lab don't look right to you (e.g. you see twice as many patients as you were expecting), which of the following would be good ways to ask for help? Select all that apply.

[[X]] email your Project Owner
[[X]] submit a ticket at the Arcus Help Center
[[X]] post a question on Discourse
***
> Any of these are fine ways to seek help!
>
> If you have a clear idea of what's going wrong, the most efficient approach might be to submit a ticket in the Help Center for the Data team describing the problem.
> If you're not sure what's going wrong, then approaching your Project Owner first may save time as they may be able to help you narrow down the issue and direct it to the right person.
> If you post on Discourse, the people responding there won't have access to the details of your lab (as your PO or the Data team would), but they can help if you troubleshoot if you think the error may be in your SQL query, for example.
>
> No matter what, whatever way you pick to ask for help, you can expect to be treated with compassion and respect. Whoever you get in touch with will do their best to connect you with the right solution as quickly as possible.
***

Which of the following can you do when you are **outside** of CHOP's firewall? Select all that apply.

[[X]] email your Project Owner
[[ ]] submit a ticket at the Arcus Help Center
[[ ]] post a question on Discourse
***
> The Arcus Help Center and Arucs Discourse are only available behind the firewall, so you'll need to be on CHOP's network or on the VPN to access them.
***

## Overview of tools

In the Available Tools section of your lab landing page, you'll see a list of the tools in your lab. Each has a small question mark icon next to it; if you click the question mark icon, it will show more details about that tool, including links to documentation to help you get started.

![Available Tools section of an Arcus Lab landing page](media/tools.png "Available Tools section of an Arcus Lab landing page, where the question mark icon next to SQLPad has been clicked to show details")

Most Arcus users will use SQLPad and either RStudio or Jupyter, but other tools may not be needed. If you're not familiar with any of these tools, we recommend you start with SQLPad.

[SQL](https://education.arcus.chop.edu/sql-intro/)
[R or python?](https://education.arcus.chop.edu/statistical-programming-languages/)

distinguish between platforms/engines/environments and languages

## How to set up your project: Files, directories, and version control

Arcus projects use a project template implemented by our Library Science team. It's a basic recommended file directory structure for organizing all of the various files related to your study.

It's designed to save researchers time, improve reproducibility, and make it easier to adhere to best practice guidelines like the [NIH's data sharing policy](https://grants.nih.gov/grants/policy/data_sharing/). It will also make things much smoother when it comes time to [contribute data to Arcus](https://assets.arcus.chop.edu/education/job-aids/arcus-data-contribution-guide.pdf).

Your lab will come with the project template already in place, so all you have to do is set up your workflows to conform to the template.

To get learn more, read [this discourse post about Arcus's Project Template](https://discourse.arcus.chop.edu/t/the-arcus-project-template/255).  

In addition to the project template, there are a number of other Research Data Management best practices you can implement to save yourself time.

### File naming

The Arcus Library Science team has compiled some excellent resources to help you decide on a file naming and organization system that will suit your needs.

- [File naming tips sheet](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/fileNaming_bestPractices_MIT.pdf)
- [File naming conventions and activity sheet](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/arcus_rdm_filenaming_activity.pdf)
- [Recommended practices for README files](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/Arcus_RDM_READMEBestPractices.pdf)

### Data documentation

The Arcus Library Science team has put together some great templates and best practices for good data documentation:

- [Recommended practices for data dictionaries](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/Arcus%20RDM%20Data%20Dictionaries%20Best%20Practices.pdf)
- A [basic ETL (extract, tansform, load) template](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/arcus_rdm_etl_template.csv), and the [README](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/arcus_rdm_etl_template_README.txt) that goes with it
- A [data collection/processing template](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/Arcus_RDM_DataCollection_Processing_Template.txt), and its [README](https://storage.googleapis.com/arcus-edu-libsci/Arcus%20RDM%20Resources/Arcus_RDM_DataCollection_Processing_README.pdf)

For more background on this topic, see this [post that answers the question "What is metadata?"](https://education.arcus.chop.edu/what-is-metadata/).

### Version control

An important aspect of research data management is the history of your files.

[https://education.arcus.chop.edu/version-control-curriculum/](https://education.arcus.chop.edu/version-control-curriculum/)
[https://education.arcus.chop.edu/git-101/](https://education.arcus.chop.edu/git-101/)
[https://education.arcus.chop.edu/git-102/](https://education.arcus.chop.edu/git-102/)

For R users, check out this excellent resource: [Happy Git with R](https://happygitwithr.com/). It is a full and detailed set of instructions for how to get started using git if you're already using R and RStudio.

# New to data science?

Arcus Education [quickstart guide for data science](https://education.arcus.chop.edu/guides/data-sci-101/)

How open is your science? [Take the quiz.](https://plos.org/how-open-is-your-science/)
[the p-acker app with fake data](https://shinyapps.org/apps/p-hacker/) and another [p-hacker app using real data](https://projects.fivethirtyeight.com/p-hacking/)

## Pivoting to data science
- Typing computer commands when you’re used to point and click
- Programming when you’re used to spreadsheet data analysis
- Version control and text files when you’re used to MS Office
- Learning a lot of new things at once: How to prioritize, how to schedule
- New rewards, and new frustrations

literate statistical programming resources
[https://education.arcus.chop.edu/modules/r-markdown/](https://education.arcus.chop.edu/modules/r-markdown/)
[https://education.arcus.chop.edu/rmd-101/]](https://education.arcus.chop.edu/rmd-101/)

[writing readable code](https://education.arcus.chop.edu/readable-code/)

## Problems in the data
- Clinical data at CHOP: What is where? [https://education.arcus.chop.edu/clinical-data-at-chop/](https://education.arcus.chop.edu/clinical-data-at-chop/) NEEDS UPDATE [https://education.arcus.chop.edu/modules/arcus-LIS/](https://education.arcus.chop.edu/modules/arcus-LIS/)
- Data dictionaries and variable names, translating Epic to Arcus
- Different information across different tables
- Errors, outliers, and typos
- Multiple versions of a variable [https://education.arcus.chop.edu/date-pairing-in-r/](https://education.arcus.chop.edu/date-pairing-in-r/)
- Information stored across rows, or across columns
- Variable types
- Missing values: None, NULL, NaN, etc. [https://education.arcus.chop.edu/do-patterns-in-missing-data-matter/](https://education.arcus.chop.edu/do-patterns-in-missing-data-matter/)
- Sanity checks: What to do when you’ve got the data

## Framing your questions so the computer will understand
- Breaking ideas down into steps (pseudocode)
- Finding where to start (what is already in the data vs. what will you need to refine/calculate/reformat)
- Working directories: finding files [https://education.arcus.chop.edu/file-paths/](https://education.arcus.chop.edu/file-paths/)
- Conventions for naming files, and things to avoid (spaces)
- Translating ideas into questions, and questions into tests

## Getting help and troubleshooting
- How much troubleshooting is normal?
- Imposter syndrome, stereotype threat, and other psychological challenges [https://xkcd.com/385/](https://xkcd.com/385/)
- Troubleshooting on your own: Where to look and what to type?
- Getting help from someone else: Who to talk to and how to ask?
- Arcus help desk
- Research help desk
- Discourse and Slack
  Pros and cons of different approaches. Writing questions vs. spoken, asking one person vs. asking a community (discourse, slack, office hours, email, user groups, web sources like SE, talking to peers, talking to PO, talking to Arcus staff, talking to Arcus ed team)

### The reproducible example

When you encounter an issue with your code and want to ask for help, you'll find the concept of the **reproducible example** to be very useful.

A reproducible example is a piece of code that 1) demonstrates your problem and 2) is entirely self-contained, so someone else could copy just that code and run it on their own machine and reproduce your problem. Crucially, just copy-pasting the lines of code from your script that are giving you trouble will usually **not** work as a reproducible example.

To illustrate, let's consider an example of a user having trouble with the `xtabs` function in R. You don't need to understand the code to follow this example, this is just to show different methods of asking a question. Let's take a look at a few different ways they could ask for help.

#### Attempt 1

> Hi, I'm trying to get a crosstab table from my data using the `xtabs` function, but it's not working. I'm getting an error that says "‘sum’ not meaningful for factors". Can you help?

Although this is a clear and specific request, someone trying to answer this question actually doesn't have a lot to go on --- the problem might be in the data themselves, or there might be a mistake in how the user is writing the code, or maybe the code is actually fine and the problem is just that the user is misunderstanding what this function does so they're using `xtabs` when actually they should be using a different function altogether. Or it could be something else entirely! It's impossible to know.

The way to fix code --- your own or someone else's --- is to test it until it works. Even very experienced programmers don't typically write code without checking that it does what they think it will.

If you want someone to help with your code, you need to give them the chance to run it.

#### Attempt 2

> Hi, I'm trying to get a crosstab table from my data using the `xtabs` function, but it's not working.
>
> Here's the code I'm running and the error I get:
```
> xtabs(A ~ B, my_data)

Error in Summary.factor(1:5, na.rm = TRUE) :
  ‘sum’ not meaningful for factors
```

Although it looks like this is providing a lot more information than the request in Attempt 1, it's actually not. We can see exactly what the user did here, which is somewhat helpful, but since we don't know what the variables A and B are like, we can't tell whether there's a problem in how they're being used in this function.

Having access to your code doesn't mean someone will be able to run it.

#### Attempt 3

> Hi, I'm trying to get a crosstab table from my data using the `xtabs` function, but it's not working. I'm getting an error that says "‘sum’ not meaningful for factors". Can you help?
>
> Here's an example of the issue using the `warpbreaks` data:
```
> xtabs(wool ~ tension, warpbreaks)
Error in Summary.factor(c(1L, 1L, 1L, 1L, ... :
  ‘sum’ not meaningful for factors
```

Here, the user is relying on one of the many [example datasets that come built into R](http://www.sthda.com/english/wiki/r-built-in-data-sets) for just this reason. That means anyone who has R installed will already have the `warpbreaks` data ready and available, whether they realize it or not. If you like, you can open R right now and copy-paste `xtabs(wool ~ tension, warpbreaks)` and you'll see the error the user reports.

This is now a **reproducible example**, and it will be much easier for folks to help figure out what's causing the error.

Note that in addition to using **built-in datasets** like those that come with R, you can also make a reproducible example by **creating example data right in your example code** or by **linking to a publicly available external dataset**.

#### Reproducible, minimal, and readable!

Although having your example be reproducible is key, you can write even better examples if you also work to keep them **minimal**, meaning there isn't any extra code beyond what is needed to illustrate your problem, and **readable**, meaning you've taken steps to make your example as easy as possible for someone else to read, like using simple, clear variable names.

For more details on what makes a good example, see these [instructions on StackOverflow](https://stackoverflow.com/help/minimal-reproducible-example).

#### But isn't that a lot of work just to ask a question?

It's true: Good examples take time and thought to write. Since you can't just copy-paste your own code, you usually need to re-write the relevant bit of code from scratch, keeping just the elements important to your problem and making sure anyone helping you will be able to run it on their own machine.

Writing reproducible examples is time consuming, but you'll find it pays off because you're much more likely to get useful answers to your question, often with working code based on your example which you can then take back and apply in your own script.

Also, remember that you're asking someone else to take time to think about your problem for you --- it's an act of respect to show you've done the work to make it as easy as possible for them to help you.

And sometimes the tinkering that goes into creating a reproducible example will actually solve your problem for you! In trying to create a minimal, reproducible version, you may figure out what the problem was all on your own.  

#### An advantage of doing your work in the browser: Everyone is working in the same environment

There are many advantages to doing your work in an Arcus lab, including increased security, storage, and computing power, but another advantage is that when you ask for help, you can get support from someone who can work in the **exact same environment** you're working in and access the **exact same data**. This removes many of the barriers to being able to replicate issues.

That means that something like Attempt 2 above might actually be sufficient, as long as you're asking for help from someone who has access to your computational lab. Whether you're going back and forth between your team members or working on an issue with Arcus staff, you can make your troubleshooting much more efficient by all working in the same environment with the same data. This can save your team a tremendous amount of time over the life of your project.

## Checking your work: Once you have code, how do you know if it’s right?

- [Data Preparation](https://education.arcus.chop.edu/data-preparation/)
- Peeking at the data
- Summarizing the data (especially count and range)
- Comparing the data (especially xtabs)
- Visualizing the data / Plotting

# New to version control and git?
[https://education.arcus.chop.edu/version-control-curriculum/](https://education.arcus.chop.edu/version-control-curriculum/)
[https://education.arcus.chop.edu/git-101/](https://education.arcus.chop.edu/git-101/)
[https://education.arcus.chop.edu/git-102/](https://education.arcus.chop.edu/git-102/)

For R users, check out this excellent resource: [Happy Git with R](https://happygitwithr.com/). It is a full and detailed set of instructions for how to get started using git if you're already using R and RStudio.

# New to SQL?

For an example of how to use SQL in your Arcus lab, start with the [training video](#training-videos) on your lab's landing page.

[https://education.arcus.chop.edu/sql-intro/](https://education.arcus.chop.edu/sql-intro/)

- Order of lines of code, especially for joins

# New to R?
[https://education.arcus.chop.edu/modules/r-art-of-learning/](https://education.arcus.chop.edu/modules/r-art-of-learning/)
[https://education.arcus.chop.edu/r-lab-for-beginners/](https://education.arcus.chop.edu/r-lab-for-beginners/)
[https://education.arcus.chop.edu/modules/r-demyst/](https://education.arcus.chop.edu/modules/r-demyst/)
[https://education.arcus.chop.edu/functions-in-r/](https://education.arcus.chop.edu/functions-in-r/)
[https://education.arcus.chop.edu/ordinary_linear_regression/](https://education.arcus.chop.edu/ordinary_linear_regression/)
[https://education.arcus.chop.edu/swirl-clinical-data/](https://education.arcus.chop.edu/swirl-clinical-data/)
[https://www.edx.org/course/data-science-r-basics](https://www.edx.org/course/data-science-r-basics

[Importing your data into R](https://bookdown.org/pdr_higgins/rmrwr/importing-your-data-into-r.html)

# New to python?
[https://education.arcus.chop.edu/python-lab-for-beginners/](https://education.arcus.chop.edu/python-lab-for-beginners/)
[https://education.arcus.chop.edu/modules/python-demyst/](https://education.arcus.chop.edu/modules/python-demyst/)
[https://education.arcus.chop.edu/jupyter101/](https://education.arcus.chop.edu/jupyter101/)
[https://education.arcus.chop.edu/modules/python-seaborn/](https://education.arcus.chop.edu/modules/python-seaborn/)
