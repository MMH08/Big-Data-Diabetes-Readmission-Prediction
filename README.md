# Diabetes Readmission Prediction

# Abstract
In this project, we are predicting whether a diabetic patient would be readmitted to the hospital or not. It is important to know if a patient will be readmitted in some hospital. The reason is that the doctor or patient can change the treatment, in order to avoid a readmission.

In this context, we can see different objective functions for the problem. We can try to figure out situations where the patient will not be readmitted, or if they are going to be readmitted in less than or in more than 30 days.

# Introduction and Context
A hospital readmission is when a patient who is discharged from the hospital, gets re-admitted again within a certain period of time. Hospital readmission rates for certain conditions are now considered an indicator of hospital quality, and also affect the cost of care adversely. For this reason, Centers for Medicare & Medicaid Services established the Hospital Readmissions Reduction Program which aims to improve quality of care for patients and reduce health care spending by applying payment penalties to hospitals that have more than expected readmission rates for certain conditions. Although diabetes is not yet included in the penalty measures, the program is regularly adding new disease conditions to the list, now totaling 6 for FY2018. In 2011, American hospitals spent over $41 billion on diabetic patients who got readmitted within 30 days of discharge.

## Objective
Being able to determine factors that lead to higher readmission in such patients, and correspondingly being able to predict which patients will get readmitted can help hospitals save millions of dollars while improving quality of care. So, with that background in mind, we used a medical claims dataset (description below), to answer these questions:

(1) What factors are the strongest predictors of hospital readmission in diabetic patients?
(2) How well can we predict hospital readmission in this dataset with limited features?

## Related Work
Beata Strack, Jonathan P. DeShazo, Chris Gennings, Juan L. Olmo, Sebastian Ventura, Krzysztof J. Cios, and John N. Clore, “Impact of HbA1c Measurement on Hospital Readmission Rates: Analysis of 70,000 Clinical Database Patient Records,” BioMed Research International, vol. 2014, Article ID 781670, 11 pages, 2014.

# Materials and Methods
## Dataset
The dataset represents 10 years (1999-2008) of clinical care at 130 US hospitals and integrated delivery networks. It includes over 50 features representing patient and hospital outcomes.

Original source of the dataset: https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008

VARIABLE NAMES: DESCRIPTION

1. Encounter ID: Unique identifier of an encounter
2. Patient number: Unique identifier of a patient
3. Race Values: Caucasian, Asian, African American, Hispanic, and other
4. Gender Values: male, female, and unknown/invalid
5. Age Grouped in 10-year intervals
6. Weight: Weight in pounds
7. Admission type: Integer identifier corresponding to 9 distinct values, for example, emergency, urgent, elective, newborn, and not available
8. Discharge disposition: Integer identifier corresponding to 29 distinct values, for example, discharged to home, expired, and not available
9. Admission source: Integer identifier corresponding to 21 distinct values, for example, physician referral, emergency room, and transfer from a hospital
10. Time in hospital: Integer number of days between admission and discharge
11. Payer code: Integer identifier corresponding to 23 distinct values, for example, Blue Cross/Blue Shield, Medicare, and self-pay Medical
12. Medical specialty: Integer identifier of a specialty of the admitting physician, corresponding to 84 distinct values, for example, cardiology, internal medicine, family/general practice, and surgeon
13. Number of lab procedures: Number of lab tests performed during the encounter
14. Number of procedures: Numeric Number of procedures (other than lab tests) performed during the encounter
15. Number of medications: Number of distinct generic names administered during the encounter
16. Number of outpatient visits: Number of outpatient visits of the patient in the year preceding the encounter
17. Number of emergency visits: Number of emergency visits of the patient in the year preceding the encounter
18. Number of inpatient visits: Number of inpatient visits of the patient in the year preceding the encounter
19. Diagnosis 1: The primary diagnosis
20. Diagnosis 2: Secondary diagnosis
21. Diagnosis 3: Additional secondary diagnosis
22. Number of diagnoses: Number of diagnoses entered to the system
23. Glucose serum test result: Indicates the range of the result or if the test was not taken.
24. A1c test result: Indicates the range of the result or if the test was not taken.
25. Change of medications: Indicates if there was a change in diabetic medications (either dosage or generic name). 
26. Diabetes medications: Indicates if there was any diabetic medication prescribed.
27. 24 features for medications: The feature indicates whether the drug was prescribed or there was a change in the dosage.
28. Readmitted: Days to inpatient readmission.

## Technologies and algorithms
Technologies: Spark
Algorithms: Supervised Learning: Multivariate Logistic Regression, Random Forest


