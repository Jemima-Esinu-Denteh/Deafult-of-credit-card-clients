# Default of credit card clients

GENERAL OBJECTIVES
This study is intended to model the credit card default data of a bank using regression models to analyse the data, draw conclusions, and give feasible recommendations.

SPECIFIC OBJECTIVES 
a. To compare the predictive performance of Logistic Regression and Random Forest.
b. To study customer behaviours that lead to default. 
c. To find which variables are the best predictors of credit card default. 

SIGNIFICANCE OF THE STUDY 
This study will give policy makers a clear understanding of the factors that are most likely to lead to an increase in credit card defaults. This will enable them to take adequate measures to avoid any of such unfortunate incidents in the future. It will also inform the creditor's choices about who to offer a credit card and the maximum allowable credit that each cardholder will legally be allowed to receive. It would also provide an understanding of current and potential customers, which would guide their future plans, including their planning of offering tailored credit products to their clientele. 

LIMITATION OF THE STUDY 
This case study is limited by the time lapse of the data. The default data may not be current enough to work with since the data was gathered years back and the bank may have seen improvements or recorded setbacks in their credit card business overtime.

DATA SOURCE AND DESCRIPTION
Data used in this project is about credit card clients of a Taiwan-based bank. It was extracted from the University of California Data Repository. The link to the data repository is  https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients#. The credit card provider collated data on 30000 customers with 24 variables associated with them. 

From the image below, there are 6630 defaulters, representing 22.1% of the data, and 23335 non-defaulters, representing 77.9% of the data. This means to suggest that, there are more non-risky customers than risky customers
. 
![image](https://user-images.githubusercontent.com/68755583/156650077-f63b7a38-24dc-4ad3-b794-e9d94af49a3e.png)

DISRIBUTION OF SEX, EDUCATION AND MARRIAGE BY DEFAULT
From the figure below, we observe the distribution of Sex, Education, and Marriage by default. The distribution of Sex by Default means to suggest that out of the 6630 risky customers shown in Figure 4.1, about 2700 are males and about 3800 are females. This informs us that, majority of the defaulters are females. 
The distribution of Education by Default informs us that, out of the 6630 risky customers, 2000 have a graduate school education, about 3330 have a university education, about 1200 have a high school education, and about 100 have other educational backgrounds. This tells us that, most of the defaulters have a university education.
From the distribution of Marriage by Default, it can be deduced that out of the 6630 defaulters in Figure 4.1, about 3150 are married, about 3250 are single, and about 150 have other marital statuses.

![image](https://user-images.githubusercontent.com/68755583/156650853-6f2296f8-7cea-4843-b69a-29361ffd20dc.png)

DISTRIBUTION OF LIMIT BALANCE BY DEFAULT STATUS
From the figure below, the distribution of limit balance is positively skewed. This suggests that on average, a customer who will default has a limit balance ranging from about 20000 NT Dollars to about 30000 NT Dollars. The highest number of non-defaulters (mode) have a limit balance of less than 10000 NT Dollars. This gives also suggests that, customers with a limit balance of less than 10000 NT Dollar are most likely to not pay.

![image](https://user-images.githubusercontent.com/68755583/156651035-b169c02c-dea4-43d8-ae27-db496326429c.png)

DISTRIBUTION OF AGE BY DEFAULT STATUS
Figure below shows that the distribution of age by default status is skewed to the right. The figure shows a very low proportion of default among older people, from ages 60 to 80. There is no significant difference in the mean ages of defaulters and non-defaulters. This means that, the likelihood of default and non-default is the same across all age groups. From the distribution, customers aged around 28 show a high level of default and the mean ages of defaulters fall between 35 and 45

![image](https://user-images.githubusercontent.com/68755583/156651133-566109ed-a8fd-4290-ac13-d6e453abf19d.png)

CORRELATION ANALYSIS
Figure below shows a correlation matrix of all variables in the dataset. Bill amount in all six months have a strong positive correlation. This means that a customer with a high bill amount six months ago is most likely to have a high bill amount in the following months. Payment amounts and bill amounts are also reasonably positively correlated with credit limit balance. This can be explained as customers with higher credit limit balances being most likely to spend more. Age also has a positive correlation of 0.1 with credit limit balance. This indicates that, older people have higher credit limit balances compared to younger people. Age does not seem to have a correlation with bill amounts.

![image](https://user-images.githubusercontent.com/68755583/156651342-a1125720-9c9d-475e-8fa0-a65fd26a7c80.png)

IMPORTANT FEATURES OF THE BEST PERFORMING MODEL
In this section, we highlight important features (best predictors) of credit default. Previously, we compared Logistic Regression (default parameters), Logistic Regression (scaled data with default parameters), Logistic Regression (optimal tuning parameters), Random Forest (default parameters), Random Forest (optimal tuning parameters) and concluded from sufficient evidence that, the model with the best predictive performance was the Random Forest model (optimal tuning parameters). Thus, if asked to choose the best model to highlight the most important features of default, it would be the Random Forest model (Optimal Tuning Parameters), since all the other models are no longer relevant.
Chart showing Feature Level Importance of Random Forest (Optimal Tuning Parameters)
![image](https://user-images.githubusercontent.com/68755583/156651500-d0d9948f-c99f-426c-b173-74555693ebd2.png)

PRECISION, RECALL AND F1-SCORE FOR ALL MODELS
The Random Forest (Optimal Tuning Parameters) has the highest precision, recall and f1-score. This means, 80% of the positive predictions made by the model are actually true and 82% of actual defaulters are correctly predicted as defaulters.
The model with the least precision, recall and f1-sore is the Logistic Regression (Default Parameters).

PRECISION, RECALL AND F1-SCORE FOR ALL MODEL PREDICTION OF DEFAULT ACCOUNTS
The Random Forest (Optimal Tuning Parameters) has the highest precision score of 67%, making it the model with the highest prediction accuracy of default accounts.
The model with the least prediction accuracy of default accounts is Logistic Regression (Default Parameters).

ROC CURVE AND AUC SCORE 
From the figure below, Random Forest (Optimal Parameters) has the highest AUC score of 0.77, which implies that it outperforms all the other classification models in the prediction of default status. The least performing classification model is Logistic Regression (Optimal Tuning Parameters) with an AUC score of 0.5.

![image](https://user-images.githubusercontent.com/68755583/156652459-0bb4d97f-002a-42bb-bc26-b85f53e86069.png)


CONCLUSION AND RECOMMENDATION
This project was focused on comparing the predictive performance of Logistic Regression and Random Forest. This chapter provides a summary of the results from the data analysis and gives recommendations to all prospective users of findings in this research.

KEY FINDINGS
‘Repayment status one month ago’ is the best predictor of customer default status. This means that, if a customer’s due payment amount one month ago is long overdue, he /she is most likely to default in payment in the next month. This brings us to the second best predictor of default status; ‘repayment status two months ago’ through to ‘repayment status six months ago’. These features highlight the possibility that a customer who defaulted in the previous month will default in the next month. Considering this, a creditor would be unable to accurately predict the default status of a new client upon first contact. The creditor can however minimize the risk of financial losses due to bad customers. A good strategy the creditor can adopt is to provide a minimal credit limit at first, then observe the spending habits of the customer, and keep track of their repayment statuses for the first few months. The creditor can then choose to increase the credit limit subsequently based on the customer’s repayment status history.
The next most prominent feature that can predict default status is ‘Payment Amount one month ago’. Customer characteristics like overspending can lead to high bill amounts. To clear high bill amounts, the customer must pay more. However, if the customer pays less, then he/she is likely to default in payment in the next month. The demographic features; age, sex, marriage and education do not necessarily determine whether a customer will default or not. However, they cannot be totally overlooked in decision making by creditors.
Comparing the predictive performance of the two models, Random Forest outperforms Logistic Regression in terms of precision and in identifying variables that best predict default status. However, should the creditor want to predict the default status of customers with high certainty, the Random Forest model used would not be efficient enough to achieve that objective given that the model can be tuned to perform better. Also, there exist other models such as Neural Networks and Deep Learning Algorithms that may fair better. Another way to enhance the model’s ability to identify defaulters is by balancing the dataset. 

RECOMMENDATION
In this research work, the cut-off point for the Logistic Regression model was 0.5. This possibly explains its underperformance compared to the Random Forest model. To ensure a better performance of Logistic Regression in further research, the cut-off point should be shifted from 0.5 to either a higher or lower threshold. This would make our model more efficient in the prediction of default rate given that there is an unequal misclassification cost.
Financial institutions may take immediate actions when they identify defaulters. These actions include making phone calls and paying unannounced visits to such customers. Noticeably, these actions are meant to put defaulters in position to pay off their credits. However, they involve quite huge costs. To avoid incurring such huge losses, the bank can do a cost analysis of spending money on getting in touch with defaulters and letting off bad debts. For example, banks can choose to let go of customers with minimal outstanding balances if they realize they would incur much higher costs on constantly calling and visiting them. This way, ‘the cost’ can be invested in more meaningful ventures. Profits regained from these investments at a future date can help make up for bad debts.
A formidable customer relationship is a good way to study behaviours like spending habits of customers. The bank can achieve this by starting strong interactions to get in touch with customers based on aggregate default in first few months.





