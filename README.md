# Diabetes Readmission Prediction

# Abstract
A diabetic clinical dataset will be used to predict whether a diabetic patient would be readmitted to the hospital or not. It is important to know if a patient will be readmitted in some hospital. The reason is that the doctor or patient can change the treatment, in order to avoid a readmission. In this context, we can see different objective functions for the problem. We can try to figure out situations where the patient will not be readmitted, or if they are going to be readmitted in less than or in more than 30 days. As the data includes race, age and sex, so we will also determine the vulnerable group among them. Apache Spark cluster-computing framework will be utilized to build the models. The language for this project would be Python. The Multivariable Logistic Regression (MLR) and Random Forest (RF) algorithms will be used to fit the relationship. We will also evaluate the performance of the algorithms.

# Introduction
## Context
After getting discharged from a hospital within a certain amount of time if a patient gets readmitted again that is considered as a hospital readmission. Hospital readmission rate can be a major indicator of patient’s health, hospital quality and cost of treatment. For example, if a patient was never been re-admitted, it’s a very good sign. Whereas if the patient is re-admitted within the 30 days of discharge represents a possibility of inappropriate treatment. On the other hand, getting readmitted after 30 days can indicate both the quality of treatment given and/or the state of the patient.
## Problem statement
In order to determine the factors that lead to higher readmission of patients, we will be analyzing a dataset, that represents 10 years (1999-2008) of clinical care at 130 US hospitals and integrated delivery networks.  Analysis of this valuable but heterogeneous and difficult data is challenging as it has missing value and contains inconsistent records. Nonetheless, it is very important to utilize these huge amounts of medical data to find new information.
## Objective
Being able to determine factors that lead to higher readmission in such patients, and correspondingly being able to predict which patients will get readmitted can help hospitals save millions of dollars while improving quality of care. So, with that background in mind, we used the dataset to answer these two questions. First, what kind of factor will be the greatest predictor of hospital readmission in diabetic patients and secondly how the limited feature in the dataset could compromise the quality of the predictions of hospital readmission.
## Related Work
Several research work and analysis has been conducted with this dataset, most notably the study to determine the impact of Hba1c in hospital readmission rate [1]. Some analysis has also be performed on the [Kaggle dataset]( https://www.kaggle.com/iabhishekofficial/prediction-on-hospital-readmission) to predict hospital re-admissibility. 

# Materials and Methods
## Dataset
A 10 years of clinical care diabetic dataset from the Health Facts database (CERNER Corporation, Kansas City, MO) is used in this project. Initially, the data was collected by Center for Clinical and Translational Research, Virginia Commonwealth University on behalf of CERNER throughout 130 USA hospitals and integrated delivery networks over the period between 1999 to 2008. As the the actual data is gathered by integrated delivery network health systems, so it includes all patients information. So, for specific interest it was required to extract new dataset from the database by following some specific criteria. For our purpose, the following criterion are considered to get new dataset:

1. it is an inpatient encounter (a hospital admission),
2. it is a diabetic encounter, that is, one during which any kind of diabetes was entered to the system as a diagnosis,
3. the length of stay was at least 1 day and at most 14 days,
4. laboratory tests were performed during the encounter,
5. medications were administered during the encounter.

Using above 5 criterion, the obtained dataset contain 101,766 encounters for to analyze factors related to readmission as well as other outcomes pertaining to patients with diabetes. From the information available in the database, 55 features that describe the diabetic encounters were picked. The few of the attributes are patient number, race, gender, age, admission type, duration of stay in hospital, lab test, HbA1c test result, diagnosis, number of medication, diabetic medications. 

In our project, we will be using this new dataset and details of data can be found our  reference paper [1]. The dataset is available in online https://www.hindawi.com/journals/bmri/2014/781670/ (as a Supplementary Material) and UCI Machine Learning Repository  (https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008). 

## Technologies and algorithms
The most widely used, fast, flexible and user friendly cluster-computing framework, Apache Spark, will be utilized to run. The language for this project would be Python. The Multivariable Logistic Regression (MLR) and Random Forest (RF) algorithms will be used to fit the relationship between the measurement of HbA1c and type of readmission. MLR is easy to implement and RF is perfect for both cluster-computing and parallel-computing as each tree is independent each others and can run independently. We will also evaluate both of these algorithms. 

# References
[1] Beata Strack, Jonathan P. DeShazo, Chris Gennings, Juan L. Olmo, Sebastian Ventura, Krzysztof J. Cios, and John N. Clore, “Impact of HbA1c Measurement on Hospital Readmission Rates: Analysis of 70,000 Clinical Database Patient Records,” BioMed Research International, vol. 2014, Article ID 781670, 11 pages, 2014.
