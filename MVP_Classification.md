## Minimum Viable Product: Employee Retention Classification

By Nicholas Bronson

After an initial exploratory analysis of the company data, and creation of KNN and logistic regression models. it appears that a KNN model using a k value of 8 neighbors has relatively strong predictive power with a score of 94.67% accuracy on the test data set. This model will give us the ability to predict if specific employees are likely to leave the company, however, it does not provide extensive insight into what some of the driving factors that are correlated with employees leaving the company might be. 

Please see the confusion matrix below, demonstrating that the KNN model is able to predict employees who left (represented by 1s) or who have not left (represented by 0s) with reasonably strong accuracy, and a low rate of false negatives and false positives.

![Image1](https://github.com/bronsonnh/Classification_Repo/blob/main/KNN_Confusion.png)


The 94 employees who were predicted as having left the company, but actually are still with the company would be excellent targets for interventions including perhaps a pay raise, increased PTO, or a promotion.  

Exploratory analysis suggests that employees with low satisfaction levels are more likely to leave the company, please see the figure below.

![Image2](https://github.com/bronsonnh/Classification_Repo/blob/main/Boxplot_Satisfaction.png)

Increasing employee satisfaction, and figuring out what leads to high satisfaction levels may help in reducing attrition. 

As next steps, I will utilize decision trees and random forest modeling to provide a deeper level of analysis and provide more robust and specific recommendations. 
