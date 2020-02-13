# Diabetes Readmission Prediction

# Abstract
In this project, we are predicting whether a diabetic patient would be readmitted to the hospital or not. It is important to know if a patient will be readmitted in some hospital. The reason is that the doctor or patient can change the treatment, in order to avoid a readmission.

In this context, we can see different objective functions for the problem. We can try to figure out situations where the patient will not be readmitted, or if they are going to be readmitted in less than or in more than 30 days.

# Introduction
It is increasingly recognized that the management of hyperglycemia in the hospitalized patient has a significant bearing
on outcome, in terms of both morbidity and mortality. This recognition has led to the development of formalized
protocols in the intensive care unit (ICU) setting with rigorous glucose targets in many institutions. However, the
same cannot be said for most non-ICU inpatient admissions.

Rather, anecdotal evidence suggests that inpatient management is arbitrary and often leads to either no treatment at
all or wide fluctuations in glucose when traditional management strategies are employed. Although data are few,
recent controlled trials have demonstrated that protocoldriven inpatient strategies can be both effective and safe.

As such, implementation of protocols in the hospital setting is now recommended. However, there are few national assessments of diabetes care in the hospitalized patient which could serve as a baseline for change. The present analysis of a large clinical database was undertaken to examine historical patterns of diabetes care in patients with diabetes admitted to a US hospital and to inform future directions which might lead to improvements in patient safety.

# Context
# Objective
# Presentation of the problem to solve

# Related Work
Beata Strack, Jonathan P. DeShazo, Chris Gennings, Juan L. Olmo, Sebastian Ventura, Krzysztof J. Cios, and John N. Clore, “Impact of HbA1c Measurement on Hospital Readmission Rates: Analysis of 70,000 Clinical Database Patient Records,” BioMed Research International, vol. 2014, Article ID 781670, 11 pages, 2014.

# Materials and Methods
# Dataset
The dataset represents 10 years (1999-2008) of clinical care at 130 US hospitals and integrated delivery networks. It includes over 50 features representing patient and hospital outcomes. Information was extracted from the database for encounters that satisfied the following criteria.
(1) It is an inpatient encounter (a hospital admission).
(2) It is a diabetic encounter, that is, one during which any kind of diabetes was entered to the system as a diagnosis.
(3) The length of stay was at least 1 day and at most 14 days.
(4) Laboratory tests were performed during the encounter.
(5) Medications were administered during the encounter.
The data contains such attributes as patient number, race, gender, age, admission type, time in hospital, medical specialty of admitting physician, number of lab test performed, HbA1c test result, diagnosis, number of medication, diabetic medications, number of outpatient, inpatient, and emergency visits in the year before the hospitalization, etc.

Original source of the dataset: https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008

This study used the Health Facts database (Cerner Corporation, Kansas City, MO), a national data warehouse that collects comprehensive clinical records across hospitals throughout the United States. Health Facts is a voluntary program offered to organizations which use the Cerner Electronic Health Record System. The database contains data systematically collected from participating institutions electronic medical records and includes encounter data (emergency, outpatient, and inpatient), provider specialty, demographics (age, sex, and race), diagnoses and in-hospital procedures documented by ICD-9-CM codes, laboratory data, pharmacy data, in-hospital mortality, and hospital characteristics. All data were deidentified in compliance with the Health Insurance Portability and Accountability Act of 1996 before being provided to the investigators. Continuity of patient encounters within the same health system (EHR system) is preserved.

Information was extracted from the database for encounters that satisfied the following criteria.
(1) It is an inpatient encounter (a hospital admission).
(2) It is a “diabetic” encounter, that is, one during which
any kind of diabetes was entered to the system as a
diagnosis.
(3) The length of stay was at least 1 day and at most 14
days.
(4) Laboratory tests were performed during the encounter.
(5) Medications were administered during the encounter.

Criteria 3-4 were applied to remove admissions for procedures and so forth, which were of less than 23 hours of duration and in which changes in diabetes management were less likely to have occurred. It should be noted that the diabetic encounters are not all encounters of diabetic patients but rather only these encounters where diabetes was coded as an existing health condition.

# Technologies and algorithms
Technologies: Spark
Algorithms: Supervised Learning: Multivariate Logistic Regression, Random Forest


