# Diabetes Readmission Prediction

# Abstract
A diabetic clinical dataset is used to identify the patients who are in risk for readmission to the hospital by using predictive models.  A supervised learning approach for 3-class classification problem will be applied to identify the patients of target classes are the patients readmitted before 30 days (Class 0) , after 30 days (Class 1) or did not admit at all (Class 2) after discharge from hospital. The Logistic Regression (LR), Decision Tree (DT) and Random Forest (RF) algorithms will be used to fit the relationship. We will also evaluate the performance among the algorithms to pick best one. Python, scikit-learn machine learning library, pandas dataframe will be utilized to build the models.

# Introduction
When a patient is admitted again into a hospital within a certain interval of time after discharge from hospital is called hospital readmission. It is very important as hospital readmission rate can be a major indicator of patient’s health and life, hospital quality and cost of treatment. For example, if a patient was never been re-admitted, it’s a very good sign. Whereas if the patient is re-admitted within the 30 days of discharge represents a possibility of inappropriate treatment. On the other hand, getting readmitted after 30 days can indicate both the quality of treatment given and/or the state of the patient. 

The complex relationship between readmission and potential risk factors makes readmission prediction a difficult task. However, it is very important to know which patients are more vulnerable for readmissions, because it will help doctors to provide quick and appropriate treatment (medicine, therapy etc.) to patients which leads to reduce of admission rate.  Every hospital follows their own method or policy to handle this problem which are not enough or accurate in some cases.  It has been argued that up to two-thirds of the readmissions are preventable; therefore, advances in patient readmission prediction are worth the investment [3, 4].  Each day, hospital produce enormous amount of data around the world and now a day data science has ability to deal with these massive data set due to improvement of computing power and technology which facilitated to apply different prediction models to get results rapidly and efficiently.  

Readmission prediction has been tackled with diverse statistical approaches [5, 6] such as logistic regression [7, 8] and survival analysis [9].  Recently, huge attention has been given to reduce hospital readmission rate using predictive machine learning approaches, such as a binary classification problem [8, 10], support vector machines (SVM) [4, 11, 12], deep learning [13, 14], artificial neural network [7], and Naïve Bayes [5, 15].  

Despite this long history of studies about hospital readmission for adult patients such as for stoke [7], emergency patients [8, 9, 10], heart failure [5, 11], pediatric patients [2, 15]. There are a few studies devoted to readmission of diabetic patients [1, 12, 16]. But, a very small amount of data has been used in [12, 16] for analysis. The importance of a specific feature (HbA1c) has been discussed in [1].  

In this project, we will use 10 years diabatic data sets to model the patients who are most likely to readmit to hospital. Our tools will facilitate the identification of patients potentially at high risk to reduce readmission rate so that resources can be used more efficiently in terms of cost-benefit.

Details of data set and methods have been described in the material and methods section. In the Result and discussion, we explain performance of each model for both balance and imbalance data set. After that a short conclusion and future work will be presented. Last section will be references. 

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

[1] https://www.hindawi.com/journals/bmri/2014/781670/  \ 
[2] https://www.hindawi.com/journals/bmri/2019/8532892/ \
[3] https://www.healthaffairs.org/doi/full/10.1377/hlthaff.2014.0041url_ver=Z39.882003&rfr_id=ori%3Arid%3Acrossref.org&rfr_dat=cr_pub%3Dpubmed& \
[4] https://www.sciencedirect.com/science/article/pii/S1532046415000969 \
[5] https://jamanetwork.com/journals/jama/fullarticle/1104511 \
[6] https://www.sciencedirect.com/science/article/abs/pii/S0169260717313998?via%3Dihub \
[7] https://www.sciencedirect.com/science/article/abs/pii/S089543560100395X \
[8] https://www.tandfonline.com/doi/full/10.1080/01969722.2016.1276772 \
[9] https://www.sciencedirect.com/science/article/abs/pii/S0925231219304564 \
[10] https://link.springer.com/article/10.1007/s00521-017-3242-y \
[11] https://www.sciencedirect.com/science/article/abs/pii/S0957417415003085 \
[12] https://www.sciencedirect.com/science/article/abs/pii/S0169260718308083 \
[13] https://www.sciencedirect.com/science/article/abs/pii/S0010482518302567 \
[14] https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0195024 \
[15] https://link.springer.com/chapter/10.1007/978-3-319-21009-4_51 \
[16] http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.259.3757&rep=rep1&type=pdf
