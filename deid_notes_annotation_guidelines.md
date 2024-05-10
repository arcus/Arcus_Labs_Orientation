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

## Ontology

```
names
    HOSPITAL
    NAME
    PATIENT
    PIC-NAMES
    STAFF
    VENDOR
geographic_subdivisions
    LOCATION
dates_ages
    AGE
    DATE
telephone_numbers
    PHONE
vehicle_identifiers
    VIN
fax_numbers
    FAX
device_identifiers_and_serial_numbers
    DEVICE
email_addresses
    EMAIL
web_urls
    URL
social_security_numbers
    SSN
ip_addresses
    IP
medical_record_numbers
    MRN
biometric_identifiers
    BIOMETRIC
health_plan_beneficiary_numbers
    HEALTHPLAN
photographs_and_images
    PHOTO
account_numbers
    ACCOUNT
other_unique_identifying_number_code_characteristic
    ID
    PIC-MISC
certificate_liscence_numbers
    LICENSE
misc_other_nonidentifying_information
    NPII
    OTHER
```

### age

Label every instance of age. 
Note that HIPAA does not consider age to be PII unless it is 90 or greater, but we're still labeling every instance of age. 
When age is a year, label the number only. 
When it is more specific than a year ("3mo", "2.5 years old"), label the span including year/month/week/day information.
Examples of age, with the span bolded: 

- **4**yo boy presents with abdominal pain
- Patient's mother was adv age at his birth (**46**).
- Pt is **2 years 3/12 months** old
- when she was approximately **24** years old
- At **24 months** patient underwent chemo
- **newborn** with recurrent apnea episodes 
- pt diagnosed at **day 6** of life
- Dad reports that at **9w** patient fell off changing table and hit her head, but no signs of tbi
- Pt began speaking at **2y3m**
- Mammograms recommended at age **40**

The following do NOT count as age and should not be labeled:

- gestational age 
- school grade level (e.g. 4th grade)
- age periods (teenage, middle-age, etc.)

### date

Label every instance of a date, or date information more specific than a year (e.g. "Thanksgiving", "winter", "Ramadan", "flu season").
This may also include notable events that were less than a year ("Pearl Harbor", "2008 Market Crash").
This includes things like date of birth or admission date, but also things like report date, appointment date, and dates from lab samples or test results. 
Examples of date, with the span bolded:

- Patient DOB: **2/4/20**
- Pt was born **May 3**, admitted **May 10**. 
- Immunized TDAP **5/3**
- Well child appts **1999-04-03**, **2000-04-10**, **2001-04-23**
- Sx started about 3 weeks ago, dad remembers noticing congestion during **spring break**
- Pt was injured in **Hurricane Sandy**
- Was hospitalized **Christmas Eve 2021**

The following do NOT count as date and should not be labeled:

- Things that may occur multiple times a year ("Tuesday", "weekend", "during pt's period", "3 weeks ago", etc.), and therefore could not be pinpointed in time if year information were added.
- Day of the month without month specified ("the 3rd", etc.)
- Times of day ("morning", "8:34pm", etc.) 
- Year alone ("2020") with no month or day specified
- Special events that don't have a specific date associated with them ("patient's birthday"). Note that something like "first day of school" should be labeled as a date because even though we don't know the specific date it refers to, we know it's some time in the early fall, which is more specific than a year. 
- Decades or other spans longer than a year ("in the 90s").

### other_unique_identifying_number_code_characteristic

Label every instance of a number, code, username, or other identifying value. 
Examples of other unique codes, with the span bolded:

- Clinical trial ID: **GH09-334**
- Patient is active on social media (**@cool_patient**) and does most of his socializing through those platforms
- Note entered via MyChart, user **gsmith3**



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
