<!--

author:   Rose Hartman
email:    hartmanr1@chop.edu
version: 0.0.0
language: en
narrator: UK English Female
mode: Textbook
title: Instructions for De-identification of Notes

comment:  

estimated_time_in_minutes: 30

@pre_reqs
None.
@end

@learning_objectives

- Know the 18 categories of information in the “Safe Harbor” method
- Be able to identify whether a note contains PHI or not
- Be able to perform manual checks of model annotations in brat

@end


@sets_you_up_for

@end

@depends_on_knowledge_available_in

@end

@version_history 
No previous versions.
@end

-->

# Instructions for De-identification of Notes

**Who this is for:** 
This is the training document for human coders who will be checking the annotations produced by [NLP](#nlp) (natural language processing) models. 
The annotations are an attempt to find identifying information in clinical notes. 

**What this covers:**
This training includes a review of what constitutes [PHI](#phi) (private health information) under [HIPAA](#hipaa), and practical instructions about how to parse clinical notes for PHI. 
There are quiz questions available to check your understanding.   

## What is PHI?

PHI is **individually identifiable health information**, so for a given piece of text to qualify as PHI it must have two things: health information, and information that identifies (or might be used to identify) the patient to which it refers.

Text describing diagnoses, procedures, symptoms, treatment, etc. is *not* PHI if it doesn't also include some information that could be used to link that health information to an individual. 
Because of this, HIPAA allows for the de-identification of clinical notes; after successfully de-identifying them, the notes are no longer PHI. 

### What counts as identifying information?

There are 18 specific kinds of identifying information listed in the "Safe Harbor" method for de-identification.

Carefully read through the [Guidance on Satisfying the Safe Harbor Method](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#safeharborguidance).


### What counts as health information?

From [HHS's definition of protected health information](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#protected): 

> the individual’s past, present, or future physical or mental health or condition,
>
> the provision of health care to the individual, or
>
> the past, present, or future payment for the provision of health care to the individual

That includes information like diagnoses, treatment, procedures, prescriptions, or symptoms for any physical or mental health condition.
It also includes information like facility or provider information, such as the name of the doctor seen or which clinic the patient came to. 
And it covers information about payment, like what kind of health insurance a patient has. 

## Quiz: What is identifying information?

Which of the following pieces of information would typically count as **identifying information** in the Safe Harbor method? 
Select all that apply.

[[X]] Patient's last name
[[ ]] The treating physician's last name
[[X]] Patient's sister's first name
[[X]] The email address of the patient's employer
[[X]] The mailing address of the patient's employer
[[ ]] The fact that the patient was seen in Radiology
[[X]] The fact that the patient's mom works for Costco
[[X]] The patient's home zip code
[[ ]] The patient's home state
[[ ]] The fact that the patient is 14 years old
[[X]] The patient's date of birth
[[X]] The fact that the patient's grandma is 91
[[X]] The patient's MRN
[[X]] The patient's health insurance number
[[X]] A photo of the patient's face
[[X]] The patient's finger prints
[[ ]] A photo of a mole on the patient's back
[[X]] The patient's clinical trial record number
[[X]] The date the patient's blood work was analyzed
[[ ]] The fact that the patient was accompanied by their mom
****

Recall that information is identifying under the Safe Harbor method if it falls into any of the 18 categories listed there and relates to the individual or to relatives, employers, or household members of the individual.

Note that some of the quiz choices here are **health information** but not **identifying information**. 
In particular, the treating physician's last name, the fact that the patient was seen in Radiology, and a photo of a mole on the patient's back would all be health information but they could probably not be used to identify the patient.

If you struggled with this question, go back and review the [Guidance on Satisfying the Safe Harbor Method](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#safeharborguidance) again.

****

## Quiz: Is this PHI?

For each of the following fake clinical notes, identify whether or not there is PHI present. 
(All of the example notes in this training are fake, written for this exercise. 
None are from real patient records.)

> HT, 3yo male, presented with headache and fever. This is his third visit to ED in a week, mom expressed concern that fever isn't resolving. 

[(X)] Yes, this has PHI
[( )] No, this does not have PHI
****

Yes, this contains both health information (symptoms, was seen in the emergency department) and identifying information (the patient's initials, "HT"). 

Note that the patient's age ("3yo") is not identifying
(although remember that age **is** identifying if it is over 89, unless it's given only as "90 or older" or equivalent). 

****

> Patient referred to OT. 
>
> SSN last 4: 1122

[(X)] Yes, this has PHI
[( )] No, this does not have PHI
****

Yes, this contains both health information (referred to OT, occupational therapy) and identifying information (the last four digits of the patient's social security number).

See [May parts or derivatives of any of the listed identifiers be disclosed consistent with the Safe Harbor Method?](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#listed).

****

> Pt immunized against polio in 09

[( )] Yes, this has PHI
[(X)] No, this does not have PHI
****

This is not PHI because although it contains health information (immunization against polio), it does not include a way to identify the individual. 

Note that dates that are the year only ("09", in this case) are not considered identifying. 
The abbreviation "Pt" is usually short for "patient", which is not identifying. 
But if it were something else (such as this person's initials) then that would be identifying. 

See [What are examples of dates that are not permitted according to the Safe Harbor Method?](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#dates).

****

> Pt complains of BL wrist stiffness and pain. She is an Olympic swimmer (won two gold and two silver medals in the 2016 games!). Work closely with both patient and coach to develop a treatment plan that takes her training into account. 

[(X)] Yes, this has PHI
[( )] No, this does not have PHI
****

Yes, this contains both health information (wrist stiffness and pain) and potentially identifying information (the fact that she won gold and silver medals in the 2016 Olympics).
Note that "BL" often stands for "bilateral", and in this context that appears to be what it means. 
If it were the patient's initials, then that would be identifying as well.

This is a situation where the identifying information is not of a typical category (name, age, MRN), but nevertheless it is specific enough that someone might reasonably be able to figure out who this patient is by looking at the list of Olympic medalists from 2016. 
In this case, her fame as an athlete is an "identifying characteristic" under HIPAA. 

See [What constitutes “any other unique identifying number, characteristic, or code” with respect to the Safe Harbor method of the Privacy Rule?](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#uniquenumber).

****

> Emergency Department, Main Hospital. 3401 Civic Center Boulevard, Philadelphia, PA 19104
> 
> Dept phone: 215-590-3480
> 
> 4yo male presents with abdominal bruising and tenderness. Dad said he fell at the playground, not sure whether or not he hit his head. Ordered ct. GHT, RN

[( )] Yes, this has PHI
[(X)] No, this does not have PHI
****

This contains health information (symptoms, was seen in the CHOP emergency department, a CT scan was ordered) but it does not contain any identifying information **about the individual, or of relatives, employers, or household members of the individual**, so it is not PHI.

Note that names of health care workers (in this case, the initials of the nurse, "GHT") are not necessarily identifying information.
Knowing the identity of the RN would probably not provide a way to identify the individual patient in this case. 
Similarly, the name, address, and phone number of the department in which the patient was seen is health information (the fact that he was seen in the CHOP emergency department), but it could not be used to identify the patient.

Keep in mind that in some cases, knowledge that a patient was treated by a particular person or at a particular facility might be identifying if it would provide information about an identifying characteristic of the patient. 
For example, knowing that a patient was treated by Dr. Ali could be identifying if it is known that Dr. Ali is the private physician for the Philadelphia Flyers ice hockey team -- knowing the year and the fact that Dr. Ali treated the patient for some specific condition or symptom could be enough to identify who the patient was by reading news coverage about the team. 
But other than rare exceptions, the presence of identifying information about health care providers does **not** make a note PHI.

See [Must a covered entity suppress all personal names, such as physician names, from health information for it to be designated as de-identified?](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#supress)

****

> DAILY NOTE 5
>
> Carlos is in recovery and doing well. Administered 600mg acetaminophen 8:34am. Grandpa had to leave for work, but asked us to please call him at 555-098-9876 immediately if Carlos's stats drop again.

[(X)] Yes, this has PHI
[( )] No, this does not have PHI
****

This contains both health information (in recovery and doing well, received acetaminophen, the fact that his stats have been dropping) and identifying information (the patient's name, "Carlos", as well as his grandpa's phone number, "555-098-9876").

Note that even though the phone number in question doesn't belong to the patient, it belongs to a relative and/or household member of the patient, and **is** therefore identifying.

Also note that the time of the acetaminophen dose (8:34am) **is not** identifying. 
A date would be identifying, but just the time on its own is not. 
Similarly, "DAILY NOTE 5" is not identifying, although a date would be.

****

> 2023-05-03 
> 
> Session 3/5
> 
> Worked on UB strength and coordination, especially crossing midline. Focusing on ADLs such as brushing teeth, donning UB clothing. 

[(X)] Yes, this has PHI
[( )] No, this does not have PHI
****

This contains both health information (the exercises done, how many sessions) and identifying information (the date of the session, "2023-05-03").

This example also includes a number of abbreviations ("UB" for "upper body", and "ADLs" for "activities of daily living"), which can be hard to parse without some experience with medical jargon.
From how they're used in the sentences here, though, it seems very unlikely that they are identifying information (such as patient initials).

Note that "Session 3/5" refers to the third of five sessions, and while it is health information it is not identifying. 
Fractions and ratios are sometimes hard to distinguish from dates.

****

> Pt has implant (ML-987650-08). Reported paternal aunt had MI at 46, paternal grandfather died of stroke. 

[(X)] Yes, this has PHI
[( )] No, this does not have PHI
****

Yes, this contains both health information (the fact that patient has an implant, family history information) and identifying information (the ID of the implanted device, "ML-987650-08").

Note that health information refers to the individual’s past, present, or future physical or mental health or condition, the provision of health care to the individual, or the past, present, or future payment for the provision of health care to the individual.
It may seem that the family history information here wouldn't qualify as health information since it isn't directly about the individual patient, but medical information about people related to the patient does provide some medical information about the patient as well -- in this case it suggests an elevated risk of cardiovascular disease. 

****

> Jan 3, 2020 18:23 
>
> BP 112/90, Temp 102.4F 

[(X)] Yes, this has PHI
[( )] No, this does not have PHI
****

This contains both health information (the patient's blood pressure and temperature) as well as identifying information (the date the individual was treated).

****

## Glossary

<a name="hipaa">HIPAA</a>: [Health Insurance Portability and Accountability Act](https://www.hhs.gov/hipaa/for-professionals/index.html). This is a law in the United States that protects certain health information, establishing strict rules around the use and disclosure of [PHI](#phi). 

<a name="phi">PHI</a>: Protected Health Information. PHI is a specific term for the kind of information that is protected by the [HIPAA Privacy Rule](https://www.hhs.gov/hipaa/for-professionals/privacy/index.html). PHI is "individually identifiable health information".

<a name="nlp">NLP</a>: Natural Language Processing. A category of machine learning models that analyze text data. 

