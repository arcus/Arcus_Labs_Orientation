<!--
link:  https://storage.googleapis.com/chop-dbhi-arcus-education-website-assets/css/styles.css
script: https://kit.fontawesome.com/83b2343bd4.js

Title: New to R?
-->

# New to R?

**What is R?  RStudio?**

R is a free, open source language that is specifically focused on statistical data analysis.  It is [increasing in market share among researchers](https://r4stats.com/articles/popularity/) (second only to SPSS and outpacing SAS, Stata, JMP, Matlab, and other solutions you may have used) and has multiple advantages over "point and click" statistical data analysis.

RStudio is a free tool made by Posit (formerly RStudio) that makes using R much simpler than using R alone.  RStudio is provided as a tool in Arcus labs and is nearly identical to the RStudio you might be accustomed to using in CHOP's HPC, on CHOP's RStudio Connect server, or on your computer.  It allows you to analyze data stored in your lab for your research project.

![""](media/rstudio.png)<!-- style = "border: 1px solid rgb(var(--color-highlight)); max-width: 600px;  margin-right: 2rem; margin-bottom: 2rem;"-->


In R, you write scripts.  Scripts are computer code that record a series of operations you want to perform on your data.  Operations could include things like:

* Ingesting data (bringing it into R) from an outside source like a .csv or a database
* Cleaning data (say, removing rows in which not every likert scale question was answered)
* Performing statistical tests (like a T-test on subjects and controls)
* Visualizing data (for example, creating an ROC)
* And much more!

**Why is R Popular?**

By using a script, you simply execute the code that could have multiple steps, such as combining data, de-identifying and cleaning data, performing analysis and statistical tests, and creating visualizations. If more data get added, you simply run the script again. You already did the hard work of writing the script, so now all you have to do is essentially hit "run".

If you realize that your workflow needs a bit of tweaking toward the beginning, you can update that part of your script and leave the rest untouched. Again, you just run the script with your changes, and you've saved yourself a lot of time compared to when changing something far upstream of your analysis meant hours of manual cleaning of data or re-creation of new files.

**What Makes R Difficult?**

Unless you recently left graduate school, you probably learned a different paradigm of data analysis, one that depended on point-and-click software.  Or perhaps you don't work directly with data but hire a statistician to do that work for you.  Learning to "DIY" is rewarding but can definitely feel frustrating, especially when you already have a system that works.  It is difficult to transition from using a system you're comfortable with to one that you're less adept at.  We do think that the gains of using R, in terms of research reproducibility, greater publication options, and more fine-grained control over things like visualizations, outweigh the annoyances of having to learn to write code.

## CHOP Has an R User Group!

![""](media/chopr_hex.png)<!-- style = "border: 1px solid rgb(var(--color-highlight)); max-width: 200px; float: left; margin-right: 2rem; margin-bottom: 2rem;"-->

CHOP has a vibrant R User Group made up of employees from all over the institution who use R for many different use cases.  This is a great place to start connecting with other people, asking for help, and seeking advice.

Please fill out this form to [join the CHOPR User Group](https://bit.ly/chopRusers)!  This will add you to the Outlook distribution list for emails as well as give you instructions on how to add yourself to our Slack workspace, where people ask coding questions (and answer them!).

Joining the R User Group means you'll be informed about periodic intro to R workshops, R User Group talks, and other resources you'll find useful.  Especially if you're the only person in your lab who uses R, it can be important to find a community of practice that can help guide you.  The R User Group, along with Arcus, provides introduction to R training periodically.  To learn more about the Introduction to R for Clinical Data course, visit the [R101 course website](https://arcus.github.io/intro-to-r-for-clinical-data/).

As you gain expertise, we also invite you to participate by leading an R User Group meeting!  You don't have to be an expert for years in order to share your skills.  Even if you only know a little, you know more than some people, and you can share pitfalls to avoid and the routes to success for data analysis tasks you conducted on your type of research data.

## Arcus-Specific R Training

Arcus On-Ramp 
-----

If you're already an Arcus user (you've signed our Terms of Use and completed CITI training), you can sign up for our Arcus On-Ramp webinars.  In these webinars, you work in a real Arcus lab analyzing CHOP's electronic health record (EHR) to replicate an actual published study. Workshops focus either on exploring the data and defining a query for your study using SQL, or running the analysis in R/Python. No coding experience is required to attend. Registration closes one week before each workshop so we have time to add registered attendees as users in the webinar training lab.  To sign up, please visit [https://arcus.chop.edu/education/webinar-signup/](https://arcus.chop.edu/education/webinar-signup/).  This link is only available for Arcus customers on the CHOP network.

Lab Training Videos 
-----

![""](media/training_videos.png)<!-- style = "border: 1px solid rgb(var(--color-highlight)); max-width: 600px; float: left; margin-right: 2rem; margin-bottom: 2rem;"-->

For an example of how to use R in your Arcus lab, start with the training videos on your lab's landing page.

These are very introductory, but help you understand specifically how to work with your Arcus lab.  

We strongly encourage you to watch **all of the videos**, in order, even the ones that don't refer to R specifically.  It's only about an hour of your time, and we think it will answer many of your questions and save time in the long run.

## Additional Resources

The training videos barely scratch the surface of how to get started.  We did that on purpose, so that they're short enough that everyone can watch them.

But they aren't enough to get you started **really** learning R.  You have several options when it comes to growing in your R skills.

There are a number of university classes, online courses and live workshops that go in depth about how to use R.  Simply search for courses at the university or MOOC (e.g. Coursera) you prefer to use.

If you prefer something a bit more "just in time", however, we suggest the R modules from the [DART (Data and Analytics for Research Training) program](https://arcus.github.io/education_modules/).

DART includes dozens of data science modules that are each 1 hour or less in duration and with a narrow focus and clear learning objectives.  They are asynchronous and you can take them at any time!

<div class = "cool-fact">

Arcus Education's DART program is the result of [an NIH grant aimed at educating biomedical researchers](https://www.research.chop.edu/announcements/dbhi-and-drexel-collaborate-to-advance-biomedical-data-science-education).
If you'd like to learn more about DART, fill out our [interest form](https://redcap.link/dart-interest) or email us at dart@chop.edu.

</div>

**Training modules:**

To begin learning R, we recommend starting with these modules: 

* [R Basics: Introduction](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_basics_introduction/r_basics_introduction.md)
* [R Basics: Transform Data](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_basics_transform_data/r_basics_transform_data.md)
* [R Basics: Visualize Data](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_basics_visualize_data/r_basics_visualize_data.md)
* [Reshaping Data in R: Long and Wide Data](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_reshape_long_wide/r_reshape_long_wide.md)
* [Missing Values in R](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_missing_values/r_missing_values.md)
* [Data Visualization in ggplot2](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/data_visualization_in_ggplot2/data_visualization_in_ggplot2.md)
* [Summary Statistics in R](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_summary_stats/r_summary_stats.md)


<br>
<details>
<summary><strong>For a deeper introduction to Data Analysis in R, click to see the full 18 module pathway.</strong></summary>
<br>
<hr>
<br>
<table>
<thead>
<tr>
<th>Order</th>
<th>Module</th>
<th>Description</th>
<th>Estimated Time</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/reproducibility/reproducibility.md">Reproducibility, Generalizability, and Reuse</a></td>
<td>This module provides learners with an approachable introduction to the concepts and impact of <strong>research reproducibility</strong>, <strong>generalizability</strong>, and <strong>data reuse</strong>, and how technical approaches can help make these goals more attainable.</td>
<td>60 min</td>
</tr>
<tr>
<td>2</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/how_to_troubleshoot/how_to_troubleshoot.md">How to Troubleshoot</a></td>
<td>Learning to use technical methods like coding and version control in your research inevitably means running into problems.  Learn practical methods for troubleshooting and moving past error codes and other difficulties.</td>
<td>30 min</td>
</tr>
<tr>
<td>3</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_basics_introduction/r_basics_introduction.md">R Basics: Introduction</a></td>
<td>Introduction to R and hands-on first steps for brand new beginners.</td>
<td>60 min</td>
</tr>
<tr>
<td>4</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_basics_visualize_data/r_basics_visualize_data.md">R Basics: Visualizing Data With ggplot2</a></td>
<td>Learn how to visualize data using R&#39;s <code>ggplot2</code> package.</td>
<td>60 min</td>
</tr>
<tr>
<td>5</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_basics_transform_data/r_basics_transform_data.md">R Basics: Transforming Data With dplyr</a></td>
<td>Learn how to transform (or wrangle) data using R&#39;s <code>dplyr</code> package.</td>
<td>60 min</td>
</tr>
<tr>
<td>6</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/tidy_data/tidy_data.md">Tidy Data</a></td>
<td>Tidy is a technical term in data analysis and describes an optimal way for organizing data that will be analyzed computationally.</td>
<td>45 min</td>
</tr>
<tr>
<td>7</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/directories_and_file_paths/directories_and_file_paths.md">Directories and File Paths</a></td>
<td>In this module, learners will explore what a directory is and how to describe the location of a file using its file path.</td>
<td>15 min</td>
</tr>
<tr>
<td>8</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_basics_practice/r_basics_practice.md">R Basics Practice</a></td>
<td>Use the basics of R coding, data transformation, and data visualization to work with real data.</td>
<td>60 min</td>
</tr>
<tr>
<td>9</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_reshape_long_wide/r_reshape_long_wide.md">Reshaping Data in R: Long and Wide Data</a></td>
<td>A module that teaches how to reshape tabular data in R, concentrating on some typical shapes known as "long" and "wide" data.</td>
<td>60 min</td>
</tr>
<tr>
<td>10</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_missing_values/r_missing_values.md">Missing Values in R</a></td>
<td>A practical demonstration of how missing values show up in R and how to deal with them. Note that this module does <strong>not</strong> cover statistical approaches for handling missing data, but instead focuses on the code you need to find, work with, and assign missing values in R.</td>
<td>45 min</td>
</tr>
<tr>
<td>11</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_summary_stats/r_summary_stats.md">Summary Statistics in R</a></td>
<td>Learn to calculate summary statistics in R, and how to present them in a table for publication.</td>
<td>30 min</td>
</tr>
<tr>
<td>12</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/data_visualization_in_open_source_software/data_visualization_in_open_source_software.md">Data Visualization in Open Source Software</a></td>
<td>Introduction to principles of data visualization and typical data visualization workflows using two common open source libraries: ggplot2 and seaborn.</td>
<td>20 min</td>
</tr>
<tr>
<td>13</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/data_visualization_in_ggplot2/data_visualization_in_ggplot2.md">Data Visualization in ggplot2</a></td>
<td>This module includes code and explanations for several popular data visualizations, using R&#39;s ggplot2 package. It also includes examples of how to modify ggplot2 plots to customize them for different uses (e.g. adhering to journal requirements for visualizations).</td>
<td>60 min</td>
</tr>
<tr>
<td>14</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/intro_to_nhst/intro_to_nhst.md">Introduction to Null Hypothesis Significance Testing</a></td>
<td>This is an introduction to NHST for biomedical researchers.</td>
<td>40 min</td>
</tr>
<tr>
<td>15</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/statistical_tests/statistical_tests.md">Statistical Tests in Open Source Software</a></td>
<td>This module provides an overview of the most commonly used kinds of statistical tests and links to code for running many of them in both R and python.</td>
<td>20 min</td>
</tr>
<tr>
<td>16</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_practice/r_practice.md">R Practice</a></td>
<td>Use the basics of R coding, data transformation, and data visualization to work with real data.</td>
<td>60 min</td>
</tr>
<tr>
<td>17</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/demystifying_machine_learning/demystifying_machine_learning.md">Demystifying Machine Learning</a></td>
<td>An approachable and practical introduction to machine learning for biomedical researchers.</td>
<td>60 min</td>
</tr>
<tr>
<td>18</td>
<td><a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/bias_variance_tradeoff/bias_variance_tradeoff.md">Understanding the Bias-Variance Tradeoff</a></td>
<td>The bias-variance tradeoff is a central issue in nearly all machine learning analyses. This module explains what the tradeoff is, why it matters for machine learning, and what you can do to manage it in your own analyses.</td>
<td>20 min</td>
</tr>
</tbody>
</table>
<br>
<hr>
<br>
</details>
<br>


Additionally, beyond the NIH grant, we have other articles and miscellany we suggest, whether those are resources we've created in Arcus, or things we recommend from the larger R community.

**Compendia of Resources**:

* Our ["R 101" Guide](https://education.arcus.chop.edu/guides/r-101/) includes links to articles, webinars, and other materials on a variety of topics.

**Other Resources**:

* [EdX Data Science in R](https://www.edx.org/course/data-science-r-basics)
* [Coursera Data Science in R Specialization by Johns Hopkins University](https://www.coursera.org/specializations/jhu-data-science)
* [Importing your data into R](https://bookdown.org/pdr_higgins/rmrwr/importing-your-data-into-r.html)
* [R for Data Science (English)](https://r4ds.had.co.nz/)
* [R for Data Science (Spanish)](https://es.r4ds.hadley.nz/)
