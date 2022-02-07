# Capstone_Project
A shared repo
## Google Slides Presentation
https://docs.google.com/presentation/d/1DSq2EQ9AHUXf6Mmc_AwmwmjLqB2UXpBOd--rOGcSHMQ/edit#slide=id.p
## Link to Dashboard
https://public.tableau.com/app/profile/yuta.chung.umemoto/viz/PredictingHeartDisease/Dashboard1?publish=yes
## Project Outline
### Purpose
For our analysis, we are analyzing a dataset of potential factors that can lead to cardiovascular disease. We chose this topic because it could potentially help people. We wanted to do something that felt important and could be a benefit to society. Heart disease is a serious issue that potentially affects a large number of people. In fact, Cardiovascular diseases (CVDs) are the number 1 cause of death globally, taking an estimated 17.9 million lives each year, which accounts for 31% of all deaths worldwide. People who are at risk need early detection and management. This where a machine learning model can be greatly beneficial. We hope that our analysis and observations can at least help with this issue.
### Description of Source of Data
Our dataset was found on kaggle. This dataset was created by combining five other datasets based on eleven common features. The five datasets used were Cleveland, Hungarian, Switzerland, Long Beach (VA), and the Stalog heart dataset. This is currently the largest heart disease dataset currently suitable for analysis.
### Questions We Hope to Answer
Heart failure is a common event caused by CVDs (Cardiovascular diseases) and this dataset contains 11 features that can be used to predict a possible heart disease. The main question we want answered is whether a person is likely to have a heart disease that can lead to heart failure. In order to find this out, we want to get more specific insights into which features play the biggest roles in heart diseases. For example, what are the top three features from the dataset in showing a correlation to CVDs? In contrast, which three features contribute the least to heart diseases? Is heart failure more of a concern in males or females? How much of a risk factor is age? Which age ranges are most susceptible to CVDs and heart failure?
### Data Exploration Phase
The dataset we found from Kaggle was largely cleaned before we got a chance to use it. There were no duplicate rows. There were no missing or null values. There were missing values in the cholesterol column but they were already changed to zeros. In addition, no datatype conversion was necessary.\
![data_exploration](https://user-images.githubusercontent.com/87148177/152887956-3bc1358f-110c-46c0-9a85-03f1ab9954a0.png)
### Analysis Phase
We knew we wanted to use a classification model for the machine learning aspect because we were predicting a discrete outcome: whether a patient has a heart
disease or not. We tested or data with three different models and noticed that the Logistic Regression model had the highest accuracy score. In addition, we thought 
Logistic Regression would be more viable than the Deep Learning model because of the relatively small size of the dataset and its number of features. Lastly, Logistic Regression was chosen over the Support Vector Machine because SVM is more accommodating to outliers, which is not ideal for our purposes.\
![train_test](https://user-images.githubusercontent.com/87148177/152889115-02f3e098-a322-4522-beb2-3df0e40537f9.png)
### Technologies, Languages, Tools, and Algorithms Used
We used a variety of tools, languages, technologies and algorithms to accomplish our task. We used Jupyter Notebook and Pandas to load our dataset into a dataframe in order to look at and clean the data. For the machine learning aspect, we used a handful of sklearn modules such as train_test_split, StandardScaler, OneHotEncoder, accuracy_score, LogisticRegression, and SVC. In addition, we used Tensorflow. Lastly, we used mongoDB for our database and Tableau to create the visualizations.
### Machine Learning Model
The dataset we have found to train our machine learning model was already provided in a very clean format. Regardless, the initial steps were taken again to confirm if the data is ready to be split and trained by checking for null values and duplicates in which none were found. With the data being cleaned, we narrowed down the machine learning models to three options. The three models were support vector machine, logistic regression, and a deep learning model. At an initial attempt to understand which model would provide us the best results in terms of accuracy, the data was split and trained to check how each model performs. At the end, it was found that the logistic regression model had provided the best accuracy out of the three, though not by a large margin. The three models were quite close in their results in terms of their accuracy. On top of determining which model to use based on pure numbers, we have still concluded that the logistic regression model is the most appropriate for the dataset we have 
taken because of the size and relatively low number of features in our dataset. With consideration to the dataset we would not consider the need to build a deep learning model because of the level of complexity in comparison to building a simple logistic regression model. This leads us to our other option which would be the support vector machine which is fairly similar to logistic regression which considers the probability of an occurence while taking account of the features while a support vector machine will find a boundary to split the dataset into two categories. For this dataset this would mean to find if the patient has heart disease or not. The reason why logistic regression was chosen from the support vector machine, aside from having a higher accuracy, was due to the fact that SVMs are able to accomodate for outliers and the plane that separates the two categories would yield to outliers. In healthcare we do not want to yield to outliers and want to spot any patients that have any potential to have 
any kind of serious illness or health related issue. This leads us to the logistic regression model being our final candidate to support our machine learning model choice to help predict if the patient will have heart disease or not based on our features. To reiterate, the dataset we have used to train this model is small in terms of how big data is defined, which leads us to having to split the data a little differently to accomodate the size. The model will be split using a 60:40 ratio rather than the standard 80:20 due to the size. This will help alleviate any chances of splitting the data into two completely separate categories which may lead to inaccurate results or accuracy. This will also likely help in achieving a similar accuracy score everytime the data is split to ensure an accuracy score that can be reproduced no matter how the data is split every time.
### Results
We found that the three most significant predictive features in the dataset were: ASY(Asymptomatic) chest pain, a "Flat" ST Slope(slope of the peak exercise ST segment), and Fasting BS(blood sugar) < 120 mg/dl. The other types of chest pain in the dataset were: TA(Typical Angina), ATA(Atypical Angina), NAP(Non-Anginal Pain). For ST Slope, there is flat(flat), up(upsloping), and down(downsloping). In contrast to the most predictive features, the three least predictive features in the dataset were the "Up" ST Slope, NAP(Non-Anginal Pain) chest pain, and the female sex. In fact, only 21% of individuals in the dataset that have a heart disease were women. There is an overwhelming number of males in the dataset in general. In addition to sex, certain age ranges also show a strong correlation with cardiovascular disease. Specifically, ages 50-65 are particularly at risk. 
### Recommendation for Future Analysis
If we could, we would want to redo our analysis later on when there is a larger dataset available. Currently, our dataset is the larger of its kind that is available for research. However, if we could use a larger dataset we would then be able to use a more traditional 80:20 split when using machine learning models. This would most likely give us more consistent and reliable results. It could also give us a higher accuracy score, which would be hugely beneficial in the medical field. Also, if more features were present in the dataset we would be able to use deep neural networks to do our analysis.
### What We Would Do Differently
If we were to do this again, we would like to build an interactive dashboard that would allow people to input information about their current health status and receive risk-analysis feedback based on this information. If we were able to do this, our work would truly be able to help people gain insight into how at-risk their heart is. In addition, we would try out a wider range of machine learning models in search of one that could give us a higher accuracy score than we were able to get with this analysis.
