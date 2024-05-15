<!--

author:   Rose Hartman
email:    hartmanr1@chop.edu
version: 1.0.0
logo: https://commons.wikimedia.org/wiki/File:20210304191333_IMG_3364-01.jpg
language: en
narrator: UK English Female
mode: Textbook
title: Annotation Guidelines

comment:  This is the full description of the ontology used to annotate identifying information in clinical notes for Arcus Projects. 

@version_history 
No previous versions.
@end

-->

# Annotation Guidelines

**Who this is for:** 
This is the annotation guidelines to be used by human coders who will be checking the annotations produced by NLP (natural language processing) models. 
The annotations are an attempt to find identifying information in clinical notes. 

**What this covers:**
This document is a full description of the ontology used to code notes, with definitions and examples for each category.  

## Key terms

**Document**: 
A document is a single note in a patient's electronic health record. 
When you open the brat annotation tool, it will display one document (note) at a time.

**Span**: 
A span is a single continuous piece of a note. 
It may be a single word, or a part of a word, or it may contain several words in a row. 

**Label**: 
The labels are the categories of information we want to identify within the notes. 
For example, patient name (PATIENT) is one label, and zip code (ZIPCODE) is another. 

**Annotation**: 
Creating an annotation means highlighting a span in the text, and then associating that span with a label. 
For example, consider the following fake note: "Raul presents with fever that doesn't respond to tylenol as well as cough, congestion, and fatigue." 
We would create an annotation in this note which would be the span "Raul" and it would get the label "PATIENT".
You also have the option to add additional information about an annotation, by clicking [Unsure](#unsure) or [NonIndentifying](#nonindentifying) and/or by writing a note in the annotation notes box.

**HIPAA**: 
[Health Insurance Portability and Accountability Act](https://www.hhs.gov/hipaa/for-professionals/index.html). 
This is a law in the United States that protects certain health information, establishing strict rules around the use and disclosure of PHI. 

**PHI**: 
Protected Health Information. 
PHI is a specific term for the kind of information that is protected by the [HIPAA Privacy Rule](https://www.hhs.gov/hipaa/for-professionals/privacy/index.html). 
PHI is "individually identifiable health information".

## General tips

**Distinguish health information from identity information.** 
HIPAA protects PHI, but health information that's not linkable to any individual person (de-identified) is not protected. 
The goal when de-identifying clinical data is to remove or mask all of the information that could be used to *identify* who the note is about (and [HIPAA provides specific guidance](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html) about this) while keeping as much of the *health* information as possible.

**HIPAA is the baseline.** 
You may be familiar already with the [18 categories of identifying information listed under the HIPAA safe harbor method](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#safeharborguidance). 
Most of the text you'll be annotating will fall into one of those categories, but we're also annotating some things that are *not* required to be removed under HIPAA, such as provider names, ages under 90, and location information coarser than state. 
It's crucial that we cover all the HIPAA categories, but know that these guidelines also intentionally extend beyond HIPAA in a few ways. 

**When in doubt, annotate.** 
If you're not sure whether or not a span is identifying, annotate it (and use the [unsure](#unsure) option to flag it for review).
It's always better to over-annotate than under-annotate.

**Shortened versions still count.** 
Things like initials, last four digits of social security, partial usernames, etc. all still count and should be annotated. 

**There's a lot of jargon.** 
Clinical notes are often written in a combination of medical terminology and shorthand that can be very hard to parse for folks that aren't used to it. 
Some of the most frequent abbreviations are: 

- Pt = patient (also sometimes Physical Therapy, depending on context)
- Dx = diagnosis
- Hx = history (as in, a history of respiratory infection)
- Sx = symptoms
- Rx = treatment or prescription 
- and [many more](https://medlineplus.gov/appendixb.html)!

You'll also notice surprising or confusing formatting in notes, often the result of forms or templates. 

**Your input matters!** 
As a coder, you will spend a lot of time reading the text of the notes -- much more time than most other researchers on the project, probably. 
You are in a uniquely valuable position to be able to notice unexpected patterns or problems in the text data, or in the annotation procedures.
If you think something is off, please bring it to the attention of the rest of the team. 
Thank you for practicing with a questioning attitude! 

## Ontology

Here is the full coding ontology, as you'll see it in the brat annotation tool:

```
NAMES
	PATIENT
	STAFF
	HOSPITAL
	DEPARTMENT
	ORGANIZATION
	OTHER IDENTIFYING (Ex. Family Names)
LOCATION (Geographic Subdivisions)
	STREET (Number and Name)
	CITY
	COUNTY
	ZIPCODE
	STATE
	COUNTRY
DATES
	MONTH
	DAY
	YEAR
	OTHER IDENTIFYING (Ex. Holiday Names)
AGES
	AGE-90PLUS
MEDICAL RECORD NUMBERS
OTHER MISC (Numbers/Codes/Characteristics)
	ID
	USERNAMES
TELEPHONE NUMBERS
FAX NUMBERS
ACCOUNT NUMBERS
CERTIFICATE LICENSE NUMBERS
HEALTH PLAN BENEFICIARY NUMBERS
SOCIAL SECURITY NUMBERS
EMAIL
WEB URLS
DEVICE IDENTIFIERS AND SERIAL NUMBERS
VEHICLE IDENTIFIERS
IP ADDRESSES
BIOMETRIC IDENTIFIERS
PHOTOGRAPHS AND IMAGES
```

Each of the labels above is explained in more detail in the sections that follow. 
You also have the option to add [additional information](#additional-options) to any annotation as needed, in the form of "Unsure" and "NonIdentifying" tags. 
And there's a notes box in the brat annotator, so you can record additional notes about an annotation as needed there. 

### NAMES

Annotate every instance of a name. 
This includes any combination of first names, last names, and initials of people. 
It also includes names of hospitals or facilities, and departments, centers, etc. as well as other organizations. 
The span should only include the name itself, not titles or credentials (although when something like "Jr" is part of someone's name, that would be included). 

Note that when a name occurs within something else, like an email or username, then just use the label for the larger span (e.g. EMAIL or USERNAME); you don't need to also label the name. 

Whenever possible, use the more specific labels: 

- PATIENT
- STAFF
- HOSPITAL
- DEPARTMENT
- ORGANIZATION
- OTHER IDENTIFYING (Ex. Family Names)

Examples of PATIENT, with the span bolded:

- 4yo boy **Henry**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> came in complaining of headache
- Patient: **D. Ramos**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Name **Matthew Shapiro III**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Working with **HB**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> on her coordination, strength, and balance. 

Examples of STAFF, with the span bolded:

- Seen by Dr. **Gloria de la Vega**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, MD, Children's Hospital of Philadelphia ADHD Management Center
- Vitals Q4, checked by **MJ**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> at 8:03pm

Examples of HOSPITAL, with the span bolded:

- Seen by Dr. Gloria de la Vega, MD, **Children's Hospital of Philadelphia**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> ADHD Management Center

Examples of DEPARTMENT, with the span bolded:

- Seen by Dr. Gloria de la Vega, MD, Children's Hospital of Philadelphia **ADHD Management Center**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Pt came to **ER**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> for persistent fever (4 days), admitted to **PICU**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Sample sent to **dermatology**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->

Note that sometimes the same phrase might refer to a department or not depending on context. 
For example, "she was seen in **dermatology**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->" should be labeled DEPARTMENT, but "she had a number of dermatology tests" wouldn't be labeled because in that case it refers to the general medical field of dermatology, not the department at this hospital. 

The label ORGANIZATION is for entities other than hospitals or other healthcare facilities.
The most common examples are employers or schools (of the patient, or relatives, or household members).
Examples of ORGANIZATION, with the span bolded:

- Pt was in the **army**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Patient's mom works at **Costco**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Is enrolled at **Brook Elementary**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Receives services through **Step Up Philly**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->

The label OTHER IDENTIFYING is for people connected with the patient (other than healthcare workers, who should be labeled as STAFF), for example, names of family members, friends, neighbors, supervisors or coworkers, etc.
Examples of OTHER IDENTIFYING, with the span bolded:

- Pt was brought in by neighbor, **Zahir**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, who found him collapsed in backyard.
- Dear Mr. **Tsui**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, I am writing to follow up on your child's recent appointment at our clinic. 
- Mom reports that pt's younger sister, **Rae**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, has had similar sx.

When the name is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care (including past, present, or future care), then it should also be checked as "[NonIdentifying](#nonindentifying)". 
For example, "Pt loves **Peppa Pig**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, it helps to play that when you need to adjust his dressing" should have the label NAMES on the span "Peppa Pig" but it should also be checked as "NonIdentifying". 

### LOCATION

Annotate every instance of a specific geographical location.
These are usually addresses (like "123 Asparagus St., Philadelphia, PA"), but it could include other spans that indicate a specific location (like "34th and Main", "Brigantine Beach", or "The Sears Tower"). 

Whenever possible, use the more specific labels: 

- STREET (Number and Name)
- CITY
- COUNTY
- ZIPCODE
- STATE
- COUNTRY

For location information that can't be described with the more specific labels, just use LOCATION.

When the a location is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care (including past, present, or future care), then it should also be checked as "[NonIdentifying](#nonindentifying)". 
For example, "Pt correctly identified **Paris**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> as the capital of **France**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> but failed two other cognitive checks" should have the label LOCATION on the two spans indicated, but each should also be checked as "NonIdentifying". 

### DATES

Annotate every instance of a date.
When the date is in a recognizable format -- either just digits, like "11-3-23", or a combination of digits and words like "Nov 3, 2023" -- then label the entire span as DATES. 
This includes things like date of birth or admission date, but also things like report date, appointment date, and dates from lab samples or test results. 
Examples of DATES, with the spans bolded:

- Patient DOB: **2/4/20**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Pt was born **May 3**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, admitted **May 10**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->. 
- Immunized TDAP **5/3**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Well child appts **1999-04-03**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, **2000-04-10**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, **2001-04-23**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Next session **November 4, 2023**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->

When date components (day, month, year) occur in isolation, instead of labeling them with DATES, label them with MONTH, DAY, or YEAR. 
Here are examples of date components occurring in isolation, with the spans bolded: 

- Sessions scheduled for the **14**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->, **15**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> and **16th**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> of next month
- First noticed rash in **March**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> 
- Attempted corrective surgery in **1999**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> and again in **2003**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->

When the date information is not formatted as a typical date, but it is more specific than a year (e.g. "Thanksgiving", "winter", "Ramadan", "flu season"), use the label "OTHER IDENTIFYING (Ex. Holiday Names)".
This may also include notable events that were less than a year ("Pearl Harbor", "2008 Market Crash").
Here are examples of OTHER IDENTIFYING (Ex. Holiday Names), with the spans bolded:

- Sx started about 3 weeks ago, dad remembers noticing congestion during **spring break**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Pt was injured in **Hurricane Sandy**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Was hospitalized **Christmas Eve 2021**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->

The following do NOT count as DATES and should not be labeled:

- Things that may occur multiple times a year ("Tuesday", "weekend", "during pt's period", "3 weeks ago", etc.), and therefore could not be pinpointed in time if year information were added.
- Times of day ("morning", "8:34pm", etc.) 
- Special events that don't have a specific date associated with them ("patient's birthday"). Note that something like "first day of school" should be labeled as a date because even though we don't know the specific date it refers to, we know it's some time in the early fall, which is more specific than a year. 
- Decades or other spans longer than a year ("in the 90s").

### AGES

Annotate every instance of age. 
Note that HIPAA does not consider age to be PII unless it is 90 or greater, but we're still labeling every instance of age.
When HIPAA-protected ages occur (anything 90 or greater), then instead of using the label AGES, use AGE-90PLUS.

When age is listed with units (like year/month/week/day), the span should include the number and units, but not the word "old". 
For ranges (for example, "15-18mos"), the span is the whole range, including both numbers and the hyphen (and units, if applicable).
Examples of age, with the span bolded: 

- **4y**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->o boy presents with abdominal pain
- Patient's mother was adv age at his birth (**46**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->).
- Pt is **2 years 3/12 months**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> old
- when she was approximately **24 years**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> old
- At **24 months**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> patient underwent chemo
- pt diagnosed at **day six**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> of life
- Dad reports that at **9w**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> patient fell off changing table and hit her head, but no signs of tbi
- Enrolled in the program from **4-8y**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Mammograms recommended at age **40**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->

The following do NOT count as age and should not be labeled:

- gestational age 
- school grade level (e.g. 4th grade)
- age periods (newborn, teenage, middle-age, etc.)

When the an age is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care (including past, present, or future care), then it should also be checked as "[NonIdentifying](#nonindentifying)". 
This most frequently occurs as a result of template text ("NEGATIVE: Infant **< 12 weeks**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> and temp higher than 100.4"), or when referring to general ages ("Most children have 1-3 words in their productive vocabulary by **15 months**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->").
These spans should still be labeled as AGES, but they should also have "NonIdentifying" checked. 

### MEDICAL RECORD NUMBERS

Annotate every instance of a medical record number (MRN). 

### OTHER MISC

Annotate every instance of a number, code, username, or other identifying value or characteristic. 

Whenever possible, use the more specific labels: 

- ID
- USERNAMES

Examples of ID, with the span bolded:

- Clinical trial ID: **GH09-334**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Abbott Elementary, Student ID **123999**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->

Examples of USERNAMES, with the span bolded:

- Patient is active on social media (**@cool_patient**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->) and does most of his socializing through those platforms
- Note entered via MyChart, user **gsmith3**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->

Also use this label for any "identifying characteristic" that isn't captured in the rest of the ontology. 
In that case, just use the label OTHER MISC. 
Examples of other identifying characteristics could be anything that doesn't fall into another label category but could be used to re-identify the patient. 
For more detail, see [What constitutes “any other unique identifying number, characteristic, or code” with respect to the Safe Harbor method of the Privacy Rule?](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#uniquenumber)
Examples of OTHER MISC, with the span bolded: 

- Pt complains of BL wrist stiffness and pain. She is an **Olympic swimmer (won two gold and two silver medals in the 2016 games!)**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->. Work closely with both patient and coach to develop a treatment plan that takes her training into account. 
- His aunt is the **first recipient of the Nobel Peace Prize**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> in this decade.


### TELEPHONE NUMBERS

Annotate every instance of a telephone number. 
These are usually 7 or 10 digits (depending on whether or not the area code is provided), and may be separated into groups of three, three, and four by spaces or hyphens, and optionally parentheses for area codes. 

There are some special phone numbers that follow a different format, but should still be labeled as telephone numbers. For example: 

- For assistance, dial **4-CHOP**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Call **911**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> right away if the individual collapses, has a seizure, has trouble breathing, or can’t be awakened.
- Text HOME to **741741**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> for immediate crisis support.

When the phone number is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care (including past, present, or future care), then it should also be checked as "NonIdentifying". 
In the three examples above, the first should just be labeled as TELEPHONE NUMBERS, and the second and third should be labeled as TELEPHONE NUMBERS and also checked as "NonIdentifying".

### FAX NUMBERS

Annotate every instance of a fax number. 
These are the same format as telephone numbers, and are usually mis-identified as telephone numbers by the NLP models, so the label needs to be changed to FAX NUMBERS. 

### ACCOUNT NUMBERS

Annotate every instance of an account number.
These are most frequently patient account numbers, often related to billing. 

### CERTIFICATE LICENSE NUMBERS

Annotate every instance of a certificate or license number.

### HEALTH PLAN BENEFICIARY NUMBERS

Annotate every instance of a health plan beneficiary number. 

### SOCIAL SECURITY NUMBERS

Annotate every instance of a social security number (SSN). 
These are generally nine digits, separated into a group of three, then two, then four by hyphens or spaces (e.g. 123-45-6789).

Note that partial SSNs (such as just the last four digits) should also be labeled. 

### EMAIL

Annotate every instance of an email address. 
Examples of emails, with the span bolded: 

- Pt asked us to also send results to her at **cool_patient@gmail.com**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Yuri Sharif, MD **sharify@chop.edu**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Pt reports he has received multiple alarming emails from **medicaid@hotmail.com**<!-- style="background-color: rgba(var(--color-highlight), .2)" --> about his coverage; talked with pt about phishing attempts and encouraged him to reach out to the tech support group at his library for help. 

When the email is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care, then it should also be checked as "NonIdentifying". 
In the three examples above, the first two should just be labeled as EMAIL, and the third should be labeled as EMAIL and also checked as "NonIdentifying".

### WEB URLS

Annotate every instance of a web address. 
Examples of URLs, with the span bolded:

- Instructed patient to review resources on our website **https://www.chop.edu/centers-programs/center-management-adhd**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- Pt does hourly online transcription work at **www.rev.com**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->
- As per national guidelines (**www.aap.org/**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->), screening should begin at age 3. 

When the URL is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care, then it should also be checked as "NonIdentifying". 
In the three examples above, the first two should just be labeled as WEB URLS, and the third should be labeled as WEB URLS and also checked as "NonIdentifying".

This category rarely occurs. 

### DEVICE IDENTIFIERS AND SERIAL NUMBERS

Annotate any ID or serial number on a device. 
Note that this does NOT include model or brand of a device -- only something that would refer to a single, specific item.

And example of a device identifier would be something like the following: 

- Pt is enrolled in the CDD trial and has a pacemaker (**ID-32443**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->)

The following would NOT count as a device identifier or serial number and should NOT be labelled: 

- Pt has a Kappa 400 pacemaker
- Has been using the GE panda warmer, but switching now to omnibed to see if that helps.

This category rarely occurs. 

### VEHICLE IDENTIFIERS

Annotate any span that would identify a particular vehicle, such a license plate number, or a unique description. 
Make, model, or color of a vehicle ("a grey prius") would generally not count as a vehicle identifier unless the combination is rare enough to be identifying. 

This category rarely occurs. 

### IP ADDRESSES

Annotate any IP address. 
They are generally four numbers (from 0-255) separated by periods, like "**163.116.80.111**<!-- style="background-color: rgba(var(--color-highlight), .2)" -->".

This category rarely occurs. 

### BIOMETRIC IDENTIFIERS

Annotate any biometric identifiers, like fingerprints, retina scans, or DNA.

This category rarely occurs. 

### PHOTOGRAPHS AND IMAGES

Annotate any photos or images.

This category rarely occurs. 

## Additional Options

For each annotation, you also have the option to add one or more categories in addition to the label. 
These show up as check boxes under the list of labels in the brat annotator. 

The options are "Unsure" and "NonIdentifying".

### Unsure

Clinical notes are hard to read, and you will occasionally encounter spans where you can't tell what they should be labeled as (is this an MRN or an account number?), or if they should even be labeled at all (maybe it's actually just a diagnosis code?). 

When you encounter a span where you're not sure whether it should be annotated or not, or if you think it should be annotated but you can't tell which label to use, then label it with your best guess and check the "Unsure" option. 
This will flag it in the data, and it can be included in regular review and discussion meetings to talk through tricky annotations.

Don't over-use the Unsure option -- if you find you frequently feel like you are unsure of your annotations, that suggests there's a problem with the ontology, the coding training, or both. 
Please bring that to the attention of the rest of the research team, and thank you for contributing to the improvement of the coding process! 

**Tip**:
The "Unsure" option is only available at the coarse coding levels (for example, NAMES, but not PATIENT or STAFF).
Do not bother to code unsure spans with the more fine-grained label options; just use the coarse category that's your best guess and check "Unsure".

### NonIndentifying

Sometimes notes contain spans that do match the above categories, but are completely unrelated to the patient. 
In these cases, the span should still be annotated with the relevant label, but you should also check the box "NonIdentifying". 

The most common example of this is template text, such as in triage forms. 
The person conducting the triage runs though a checklist, and the results of that checklist are saved in a note. 
Items on the checklist might be things like "Fever in infant < 12 weeks" -- the span "< 12 weeks" is an age, but it's not about the patient at all, it's just a generic cutoff. 

Another example occurs in references to general guidelines or standards. 
For example, the note "Recommended catch up schedule (https://www.cdc.gov/vaccines/schedules/hcp/imz/catchup.html) for missed vaccines" includes a URL, so it should be annotated with the label WEB URLS, but it should also be checked as "NonIdentifying" since that URL is not identifying the patient, it's just a reference. 
It doesn't provide information about who the patient is (or their relatives, employer, or household members) or any information about where they received care. 

The note "AAP recommends ASD screening for children with no productive language at 18mo" would have two spans that should be checked "NonIdentifying": 
"AAP" should get the label NAMES (it's an organization, the American Academy of Pediatrics), and "18mo" should get AGES (note that "ASD" is an abbreviation for Autism Spectrum Disorder and should not be annotated), and both would be checked "NonIdentifying". 

**Tip**:
The "NonIdentifying" option is only available at the coarse coding levels (for example, NAMES, but not PATIENT or STAFF).
Do not bother to code nonidentifying spans with the more fine-grained label options; just use the coarse categories and check "NonIdentifying".

## References

https://lhncbc.nlm.nih.gov/scrubber/annotation/pdf.papers/Guidelines.2016.06.28.pdf

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4765667/

