### Lessons from the H1N1 Pandemic
A machine learning model by Jade Adams and Stephen William, students at the Flatiron School.


### Business Problem

The Center for Disease Control and Prevention seeks to combat vaccine hesistancy in the United States. It has hired us to investigate a comprehensive dataset from our last major national pandemic, the H1N1 virus, and find a model and correlation characteristics with getting vaccinated or not. It will use this model to hone resources in on areas and populations of the United States with a high likelihood for vaccine hesistancy


### Dataset Characteristics

The dataset consists of 26,000 respondents demographic information, opinions on the H1N1 pandemic and vaccine, and their decision to get vaccinated or not. There is in total 40 rows of information per respondent, including marital status, sex,race, income, occupation, health care coverage, and more. Opinion characteristics were all ordinal: they answered questions with a scale of 1-5. 

A printout of our data:

<class 'pandas.core.frame.DataFrame'>
Int64Index: 26707 entries, 0 to 26706
Data columns (total 26 columns):
 #   Column                       Non-Null Count  Dtype  
---  ------                       --------------  -----  
 0   h1n1_concern                 26615 non-null  float64
 1   h1n1_knowledge               26591 non-null  float64
 2   behavioral_avoidance         26499 non-null  float64
 3   behavioral_face_mask         26688 non-null  float64
 4   behavioral_wash_hands        26665 non-null  float64
 5   behavioral_large_gatherings  26620 non-null  float64
 6   behavioral_outside_home      26625 non-null  float64
 7   behavioral_touch_face        26579 non-null  float64
 8   doctor_recc_h1n1             24547 non-null  float64
 9   doctor_recc_seasonal         24547 non-null  float64
 10  chronic_med_condition        25736 non-null  float64
 11  child_under_6_months         25887 non-null  float64
 12  health_worker                25903 non-null  float64
 13  opinion_h1n1_vacc_effective  26316 non-null  float64
 14  opinion_h1n1_risk            26319 non-null  float64
 15  opinion_h1n1_sick_from_vacc  26312 non-null  float64
 16  age_group                    26707 non-null  object 
 17  education                    25300 non-null  object 
 18  race                         26707 non-null  object 
 19  sex                          26707 non-null  object 
 20  income_poverty               22284 non-null  object 
 21  marital_status               25299 non-null  object 
 22  rent_or_own                  24665 non-null  object 
 23  employment_status            25244 non-null  object 
 24  household_adults             26458 non-null  float64
 25  household_children           26458 non-null  float64
dtypes: float64(18), object(8)
memory usage: 5.5+ MB


Of the 26,000 respondents, 21% of them received the H1N1 vaccine.

![Getting Started](images/Unknown-6.jpg)

### Key Takeaways

Using the dataset, we built a logistic regression pipeline that could predict with 75% accuracy whether someone wass vaccinated or not depending on their characteristics. We found the following characteristics improved a respondent's likelihood on getting vaccinated:

1. Their doctor reccomended them the vaccine
2. Their level of concern about the pandemic was high
3. Their belief in the efficacy of the vaccine was high

Below is a confusion matrix of our final model. 


![Getting Started](images/Unknown-5.jpg)



## Exploratory Data Analysis

### Reccomendations for the CDC

It is important then for the CDC to improve doctor outreach and regulations to make sure primary care physicians are encouraging their patients to get the COVID-19 vaccine, as this was singlehandedly the most important determiner of whether someone was vaccinated or not.

