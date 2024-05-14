<!--

author:   Rose Hartman
email:    hartmanr1@chop.edu
version: 0.0.0
language: en
narrator: UK English Female
mode: Textbook
title: Annotation Guidelines

comment:  

estimated_time_in_minutes: 30

@pre_reqs
None.
@end

@learning_objectives

- 

@end


@sets_you_up_for

@end

@depends_on_knowledge_available_in

@end

@version_history 
No previous versions.
@end

-->

# Annotation Guidelines

**Who this is for:** 
This is the annotation guidelines to be used by human coders who will be checking the annotations produced by [NLP](#nlp) (natural language processing) models. 
The annotations are an attempt to find identifying information in clinical notes. 

**What this covers:**
This document is a full description of the ontology used to code notes, with definitions and examples for each category.  

## General tips

**HIPAA is the baseline.** 
You may be familiar already with the 18 categories of identifying information listed under the HIPAA safe harbor method. 
Most of the text you'll be annotating fall into one of those categories, but we're also annotating some things that are *not* required to be removed under HIPAA, such as provider names, ages under 90, and location information coarser than state. 
It's crucial that we cover all the HIPAA categories, but know that these guidelines also intentionally extend beyond HIPAA in a few ways. 

**When in doubt, annotate.** 
If you're not sure whether or not a span is identifying, annotate it (and use the [unsure](#unsure) option to flag it for review).
It's always better to over-annotate than under-annotate.

**Your input matters!** 
As a coder, you will spend a lot of time reading the text of the notes -- much more time than most other researchers on the project, probably. 
You are in a uniquely valuable position to be able to notice unexpected patterns or problems in the text data, or in the annotation procedures.
If you think something is off, please bring it to the attention of the rest of the team. 
Thank you for practicing with a questioning attitude! 

## Ontology

Here is the full coding ontology, as you'll see it in the brat annotation tool. 

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

### NAMES

Label every instance of a name. 
This includes any combination of first names, last names, and initials of people. 
It also includes names of hospitals or facilities, and departments, centers, etc. as well as other organizations. 
The span should only include the name itself, not titles or credentials (although when something like "Jr" is part of someone's name, that would be included). 

When possible, use the more specific labels: 

- PATIENT
- STAFF
- HOSPITAL
- DEPARTMENT
- ORGANIZATION
- OTHER IDENTIFYING (Ex. Family Names)

Examples of PATIENT, with the span bolded:

- 4yo boy **Henry** came in complaining of headache
- Patient: **D. Ramos**
- Name **Matthew Shapiro III**
- Working with **HB** on her coordination, strength, and balance. 

Examples of STAFF, with the span bolded:

- Seen by Dr. **Gloria de la Vega**, MD, Children's Hospital of Philadelphia ADHD Management Center
- Vitals Q4, checked by **MJ** at 8:03pm

Examples of HOSPITAL, with the span bolded:

- Seen by Dr. Gloria de la Vega, MD, **Children's Hospital of Philadelphia** ADHD Management Center

Examples of DEPARTMENT, with the span bolded:

- Seen by Dr. Gloria de la Vega, MD, Children's Hospital of Philadelphia **ADHD Management Center**

Note that sufficiently generic departments do NOT need to be labeled. 
The most common example is "ED" or "ER", referring to Emergency Department/Emergency Room, but other common examples are "radiology", "OT/occupational therapy", etc. 
In general, a department is generic if knowing the name of the department would not help you to identify the hospital or facility (e.g. "ER" could refer to almost any hospital, but "Anxiety Behaviors Clinic (ABC)" is something that might be particular to a given hospital).


Examples of ORGANIZATION, with the span bolded:

- Pt was in the **army**
- Patient's mom works at **Costco**
- Is enrolled at **Brook Elementary**
- Receives services through **Step Up Philly**


### LOCATION

Label every instance of a specific geographical location.
These are usually addresses (like "123 Asparagus St., Philadelphia, PA"), but it could include other spans that indicate a specific location (like "34th and Main", "Brigantine Beach", or "The Sears Tower"). 

When possible, use the more specific labels: 

- STREET (Number and Name)
- CITY
- COUNTY
- ZIPCODE
- STATE
- COUNTRY

For location information that can't be described with the more specific labels, just use LOCATION.

When the a location is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care (including past, present, or future care), then it should also be checked as "NonIdentifying". 
For example, "Pt correctly identified **Paris** as the capital of **France** but failed two other cognitive checks" should have the label LOCATION on the two spans indicated, but each should also be checked as "NonIdentifying". 

### DATES

Label every instance of a date.
When the date is in a recognizable format -- either just digits, like "11-3-23", or a combination of digits and words like "Nov 3, 2023" -- then label the entire span as DATES. 
This includes things like date of birth or admission date, but also things like report date, appointment date, and dates from lab samples or test results. 
Examples of DATES, with the spans bolded:

- Patient DOB: **2/4/20**
- Pt was born **May 3**, admitted **May 10**. 
- Immunized TDAP **5/3**
- Well child appts **1999-04-03**, **2000-04-10**, **2001-04-23**
- Next session **November 4, 2023**

When date components (day, month, year) occur in isolation, instead of labeling them with DATES, label them with MONTH, DAY, or YEAR. 
Here are examples of date components occurring in isolation, with the spans bolded: 

- Sessions scheduled for the **14**, **15** and **16th** of next month
- First noticed rash in **March** 
- Attempted corrective surgery in **1999** and again in **2003**

When the date information is not formatted as a typical date, but it is more specific than a year (e.g. "Thanksgiving", "winter", "Ramadan", "flu season"), use the label "OTHER IDENTIFYING (Ex. Holiday Names)".
This may also include notable events that were less than a year ("Pearl Harbor", "2008 Market Crash").
Here are examples of OTHER IDENTIFYING (Ex. Holiday Names), with the spans bolded:

- Sx started about 3 weeks ago, dad remembers noticing congestion during **spring break**
- Pt was injured in **Hurricane Sandy**
- Was hospitalized **Christmas Eve 2021**

The following do NOT count as DATES and should not be labeled:

- Things that may occur multiple times a year ("Tuesday", "weekend", "during pt's period", "3 weeks ago", etc.), and therefore could not be pinpointed in time if year information were added.
- Times of day ("morning", "8:34pm", etc.) 
- Special events that don't have a specific date associated with them ("patient's birthday"). Note that something like "first day of school" should be labeled as a date because even though we don't know the specific date it refers to, we know it's some time in the early fall, which is more specific than a year. 
- Decades or other spans longer than a year ("in the 90s").

### AGES

Label every instance of age. 
Note that HIPAA does not consider age to be PII unless it is 90 or greater, but we're still labeling every instance of age.
When HIPAA-protected ages occur (anything 90 or greater), then instead of using the label AGES, use AGE-90PLUS.

When age is listed with units (like year/month/week/day), the span should include the number and units, but not the word "old". 
Examples of age, with the span bolded: 

- **4y**o boy presents with abdominal pain
- Patient's mother was adv age at his birth (**46**).
- Pt is **2 years 3/12 months** old
- when she was approximately **24 years** old
- At **24 months** patient underwent chemo
- pt diagnosed at **day six** of life
- Dad reports that at **9w** patient fell off changing table and hit her head, but no signs of tbi
- Pt began speaking at **2y3m**
- Mammograms recommended at age **40**

The following do NOT count as age and should not be labeled:

- gestational age 
- school grade level (e.g. 4th grade)
- age periods (newborn, teenage, middle-age, etc.)

When the an age is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care (including past, present, or future care), then it should also be checked as "NonIdentifying". 
This most frequently occurs as a result of template text ("NEGATIVE: Infant **< 12 weeks** and temp higher than 100.4"), or when referring to general ages ("Most children have 1-3 words in their productive vocabulary by **15 months**").
These spans should still be labeled as AGES, but they should also have "NonIdentifying" checked. 

### MEDICAL RECORD NUMBERS

Label every instance of a medical record number (MRN). 

### OTHER MISC

Label every instance of a number, code, username, or other identifying value. 
Examples of other unique codes, with the span bolded:

- Clinical trial ID: **GH09-334**
- Patient is active on social media (**@cool_patient**) and does most of his socializing through those platforms
- Note entered via MyChart, user **gsmith3**

### TELEPHONE NUMBERS

Label every instance of a telephone number. 
These are usually 7 or 10 digits (depending on whether or not the area code is provided), and may be separated into groups of three, three, and four by spaces or hyphens, and optionally parentheses for area codes. 

There are some special phone numbers that follow a different format, but should still be labeled as telephone numbers. For example: 

- For assistance, dial **4-CHOP**
- Call **911** right away if the individual collapses, has a seizure, has trouble breathing, or can’t be awakened.
- Text HOME to **741741** for immediate crisis support.

When the phone number is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care (including past, present, or future care), then it should also be checked as "NonIdentifying". 
In the three examples above, the first should just be labeled as TELEPHONE NUMBERS, and the second and third should be labeled as TELEPHONE NUMBERS and also checked as "NonIdentifying".

### FAX NUMBERS

Label every instance of a fax number. 
These are the same format as telephone numbers, and are usually mis-identified as telephone numbers by the NLP models, so the label needs to be changed to FAX NUMBERS. 

### ACCOUNT NUMBERS

Label every instance of an account number.
These are most frequently patient account numbers, often related to billing. 

### CERTIFICATE LICENSE NUMBERS

Label every instance of a certificate or license number.

### HEALTH PLAN BENEFICIARY NUMBERS

Label every instance of a health plan beneficiary number. 

### SOCIAL SECURITY NUMBERS

Label every instance of a social security number (SSN). 
These are generally nine digits, separated into a group of three, then two, then four by hyphens or spaces (e.g. 123-45-6789).

Note that partial SSNs (such as just the last four digits) should also be labeled. 

### EMAIL

Label every instance of an email address. 
Examples of emails, with the span bolded: 

- Pt asked us to also send results to her at **cool_patient@gmail.com**
- Yuri Sharif, MD **sharify@chop.edu**
- Pt reports he has received multiple alarming emails from **medicaid@hotmail.com** about his coverage; talked with pt about phishing attempts and encouraged him to reach out to the tech support group at his library for help. 

When the email is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care, then it should also be checked as "NonIdentifying". 
In the three examples above, the first two should just be labeled as EMAIL, and the third should be labeled as EMAIL and also checked as "NonIdentifying".

### WEB URLS

Label every instance of a web address. 
Examples of URLs, with the span bolded:

- Instructed patient to review resources on our website **https://www.chop.edu/centers-programs/center-management-adhd**
- Pt does hourly online transcription work at **www.rev.com**
- As per national guidelines (**www.aap.org/**), screening should begin at age 3. 

When the URL is NOT related to the patient (or relatives, employer, or household members of the patient) or to the healthcare providers or facilities providing care, then it should also be checked as "NonIdentifying". 
In the three examples above, the first two should just be labeled as WEB URLS, and the third should be labeled as WEB URLS and also checked as "NonIdentifying".

This category rarely occurs. 

### DEVICE IDENTIFIERS AND SERIAL NUMBERS

Label any ID or serial number on a device. 
Note that this does NOT include model or brand of a device -- only something that would refer to a single, specific item.

And example of a device identifier would be something like the following: 

- Pt is enrolled in the CDD trial and has a pacemaker (**ID-32443**)

The following would NOT count as a device identifier or serial number and should NOT be labelled: 

- Pt has a Kappa 400 pacemaker
- Has been using the GE panda warmer, but switching now to omnibed to see if that helps.

This category rarely occurs. 

### VEHICLE IDENTIFIERS

Label any span that would identify a particular vehicle, such a license plate number, or a unique description. 
Make, model, or color of a vehicle ("a grey prius") would generally not count as a vehicle identifier unless the combination is rare enough to be identifying. 

This category rarely occurs. 

### IP ADDRESSES

Label any IP address. 
They are generally four numbers (from 0-255) separated by periods, like "**163.116.80.111**".

This category rarely occurs. 

### BIOMETRIC IDENTIFIERS

Label any biometric identifiers, like fingerprints.

This category rarely occurs. 

### PHOTOGRAPHS AND IMAGES

Label any photos or images.

This category rarely occurs. 

## References

https://lhncbc.nlm.nih.gov/scrubber/annotation/pdf.papers/Guidelines.2016.06.28.pdf

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4765667/

## Quiz: What is identifying information?

Which of the following pieces of information would typically count as **identifying information** in the Safe Harbor method? 
Select all that apply.

[[X]] Patient's last name
[[ ]] The treating physician's last name
[[X]] Patient's sister's first name
[[X]] The email address of the patient's employer
****


If you struggled with this question, go back and review the [Guidance on Satisfying the Safe Harbor Method](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#safeharborguidance) again.

****
