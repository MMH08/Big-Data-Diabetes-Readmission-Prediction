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


A 10 years of clinical care diabetic dataset from the Health Facts database (CERNER Corporation, Kansas City, MO) is used in this project. Initially, the data was collected by Center for Clinical and Translational Research, Virginia Commonwealth University on behalf of CERNER throughout 130 USA hospitals and integrated delivery networks over the period between 1999 to 2008. Midwest (18 hospitals), Northeast (58), South (28), and West (16). As the the actual data is gathered by integrated delivery network health systems, so it includes all patients information. So, for specific interest it was required to extract new dataset from the database by following some specific criteria:  
(1) It is an inpatient encounter (a hospital admission).
(2) It is a diabetic encounter, that is, one during which any kind of diabetes was entered to the system as a diagnosis.
(3) The length of stay was at least 1 day and at most 14 days.
(4) Laboratory tests were performed during the encounter.
(5) Medications were administered during the encounter.

Now, the new dataset contain 101,766 encounters for to analyze factors related to readmission as well as other outcomes pertaining to patients with diabetes. From the information available in the database, 55 features that describe the diabetic encounters were picked. The few of the attributes are patient number, race, gender, age, admission type, duration of stay in hospital, lab test, HbA1c test result, diagnosis, number of medication, diabetic medications. 
In our project, we will be using this new dataset and details of data can be found our  reference paper [1]. The dataset is available in online https://www.hindawi.com/journals/bmri/2014/781670/ (as a Supplementary Material) and UCI Machine Learning Repository  (https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008). 

The dataset represents 10 years (1999-2008) of clinical care at 130 US hospitals and integrated delivery networks. It includes over 50 features representing patient and hospital outcomes.

## Technologies and algorithms
Technologies: Spark
Algorithms: Supervised Learning: Multivariate Logistic Regression, Random Forest


