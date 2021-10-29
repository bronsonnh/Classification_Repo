# Classification Modeling to Predict and Reduce Employee Attrition

By Nicholas Bronson

## Abstract:

This project uses a classification model to analyze and classify employees in a set of HR data for a client in the logistics sector. The goal is to create a model that will put employees in the class of “likely to leave” or “likely to stay.” After rigorous selection, I selected use of a random forest in conjunction with a KNN model due to their ability to predict employee class with a high level of recall and accuracy. I also investigated and determined top factors that were related to employee attrition and created recommendations regarding intervention strategies based on this. 

## Design:

A prospective client, MTS Shipping, a mid-sized player in the logistics sector, approached me looking for a data-oriented solution for predicting employee attrition. In the face of what the media has labeled “the great resignation,” my client has suffered higher rates of attrition than normal and provided a dataset containing data for 15000 current and former employees of the company. They are looking to understand the answers to several key questions: 

1) Who are the employees that are most likely to resign, and what are the qualities of these employees?
2) What factors have the strongest influence on whether employees will stay or leave?
3) What might appropriate and effective interventions look like, and what aspects might they target?

This project aims to answer these questions through use of classification models to determine groups of employees that are most likely to leave.

## Data:

The dataset is a 15,000-row file containing HR data for MTS Shipping. Each row represents an employee who had spent at least 2 years with the company. The target variable is labeled “left” this is a binary variable identifying employees who have left and those who have stayed. There are 9 features in the original dataset including including division, salary, satisfaction level, recency of last evaluation, number of projects, average monthly hours, time spent with the company in years, and number of work accidents. Dummy variables were used to represent categorical variables, division and salary band. 

## Algorithms:

I began this project by creating dummy variables for categorical variables and conducting exploratory data analysis using pandas. I assumed satisfaction level would be a key factor in determining which employees were likely to leave, and initial exploration showed that employees who had left the company typically had lower levels of satisfaction. I cleaned some of the data’s formatting and examined basic trends around feature characteristics and interactions using pairplots and histograms.


As a next step, I performed the K-Nearest Neighbors classification model which performed quite well once it was determined that using 9 neighbors produced the best recall and accuracy scores, which is the priority for this client, as false negatives, misclassifying employees who are likely to leave as likely to stay, will be more costly than false positives. I conducted logistic regression which performed relatively poorly after tuning C values and adjusting the probability threshold. A decision tree performed well after adjusting tree depth, with a random forest performing at an even stronger level. Using a random forest provided to provide strong levels of recall and accuracy once tuned. MTS should begin using the random forest model immediately to begin predicting attrition, the KNN model could also work fairly well if a more intrepretable model is preferable. As a final step, I gathered calculated feature importance to determine best features to target in interventions aimed at reducing attrition. 

The selected random forest’s cross validated performance is as follows: 

Recall: 97.3%,
Accuracy: 98.2%,
Precision: 95.6%,
F1: 96.4%  

The selected KNN model’s cross validated performance is as follows: 

Recall: 92.7%,
Accuracy: 93.9%,
Precision: 83.5%,
F1: 87.8% 

## Tools:

The primary tool used for this project was python and various packages including pandas, sklearn, matplotlib, and seaborn. I performed analyses in a jupyter notebook and ingested data that was acquired from Kaggle. 

## Communications:
The primary form of communication is a Google Slide deck containing an overview of the problem, a classification solution, and recommendations regarding employees that should receive intervention as well as areas that would be best to provide interventions across the company in order to reduce attrition.  


