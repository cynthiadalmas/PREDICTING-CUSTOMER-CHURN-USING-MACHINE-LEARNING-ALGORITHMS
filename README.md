# PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS
This project entails building a classifier model to predict whether a customer will stop doing business with Syria Tel, a telecommunications company. This is a binary classification problem.  Most naturally, telecommunication businesses would be interested in reducing how much money is lost when a customers does not stick around for a long time.

![CS](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/e2beeb0f-90f1-4ac4-a1ac-c7519f5a96b0)

**BUSINESS PROBLEM**

Customer churn is a major problem and one of the most important concerns for large telecommunication companies. Due to the direct effect on the revenues of the companies, especially in the telecom field, companies are seeking to develop means to predict potential customer to churn.

Therefore, finding factors that increase customer churn is important to take necessary actions to reduce this churn.

Syria Tel Company is nevertheless affected by customer churning as well.

The main contribution of my work is to developing a churn predictive model which assists telecom operators to predict customers who are most likely subject to churn.

The models developed in this project uses machine learning techniques to classify and predict customers who churn as 1 and no churn as 0.

In order to measure the performance of the model, classification metrics such as Precision, recall,F1-Score, the ROC and Area Under Curve (AUC) standard measure is adopted, and the AUC value obtained is 0.85.

**DATA UNDERSTANDING**

The dataset contains call details of 3333 customers with 21 features and a dependent churn parameter with two values: Yes/No.
Some features include information about the number of incoming and outgoing messages and voicemail for each customer.

**DATA PREPARATION**

**Exploratory Data Analysis was done on the following:**

- Previewing the data
- Descriptive statistics of the data
- Renaming columns
- Dropping uncessary columns
- Checking and handling missing values
- Checking for duplicates
- Checking the data shape
- Checking and handling outliers
- Checking for the data class balance
- Plotting charts histograms,bra graghs,violin charts,pie charts etc to check the distribution of dependent and independent variables
- Performing Uni-variate, Bi-variate and Multivariate analysis.
  
**MODELING**

**Five machine learning algorithms were used in this project to predict churn factor:**

- Logistic regression Model
- Decision tree Model
- Random Forest Model
- Bayes Networks Model
- XGBOOST Model
** Only one model that gave the best/highest metrics was chosen**

**Model EVALUATION**

Finally, the models are evaluated to check whether the models accomplished their intended tasks, the following metrics are used to assess their effectivenes
Accuracy - percentage of the total variables that were correctly classified. Use the formula Accuracy = (TP+TN) / (TP+TN+FP+FN)
False positive rate - how often the model predicts a positive for a value that is actually negative. Use the formula False Positive Rate = FP / (FP+TN)
Precision - percentage of positive cases that were true positives as opposed to false positives. Use the formula Precision = TP / (TP+FP)
Recall - percentage of actual positive cases that were predicted as positives, as opposed to those classified as false negatives. Use the formula Recall = TP/(TP+FN)
Area under curve - method of visualizing true and false positive rates against each other.

**SUMMARY**

EDA, Feature creation by combining features,Data splitting, Hyperparamter tuning & outlier detection, Cross Validation Score were performed.
Six models were fit on the churning dataset and the best model which is Decision Tree was selected

**STEP 1: EXPLORATOTY DATA ANALYSIS**

**Checking the distribution of independent and ependent variables.**

![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/907c70c8-ef97-48e9-8e78-d668759a186b)

- Most variables follow a normal distribution.

**Checking the relationship amongst the variables**

![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/4193d563-469b-4b84-8133-d35fb479a7ec)

- Most variable are correlated.

**Determining which factors caused customers to churn**

![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/a37e7998-6d1c-4966-81ff-3b6eb1b59956)

- The factors include: Total Charges, Total minutes.

  
**Determining the percentage of customers who churned.**

![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/b4aebfb1-4aa4-45de-8646-e0e4b694aa89)

- 86% of the customers stayed,while 14% of he customers left the company.
  
**Checking the states and area codes where customers were most likely too churn.**
  
  ![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/cea27fb2-61f5-4d62-8188-7116d1463c11)

  - Area code 510 and 415 are likely to leave the company.

    ![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/bda75af2-71f9-4311-8f48-c4666de874f0)

 - WV.MN,& NY are had majority of customers in using the tele communication services

  
**Determining the correlation between variables using a correlation heatmap**

![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/7b59578f-c5c9-41f2-a1d3-e79675699fe1)

 - There is perfect correlation between total minutes and total charges.

 **MODELING**

**1. NAIVE BAYES THEOREM**

   ANALYZING THE CONFUSION ATRIX FOR NAIVE BAYES MODEL.

   ![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/4ef30b06-712e-4dd1-9a41-90dcc196ff84)

   - This confusion matrix indicates that no true positives were predicted. Naive Bayes did not work well.
  
**CLASSIFICATION METRICS OF THE NAIVE BAYE'S MODEL**
     
  <img width="415" alt="81149fb1b390b5fdf283fb460e8958a" src="https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/a403ef68-9799-4cf2-bcd5-7526faef5375">

  
**2. DECISION TREE MODELl**

**The tree splits**
 
  **ANALYZING THE CONFUSION MATRIX FOR DECISION TREE MODEL.**

   ![image](https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/1ae55b93-7f11-4dd6-bd75-6b458ab4db0f)

   - From this confusion matrix that the model correctly predicts many true negatives.
   - It appears slightly more likely to predict a false positive than a false negative.
   - The decision tree model also predicts lesser false positive.
   
**CLASSIFICATION METRICS OF THE DECISION TREE MODEL**
   
   <img width="391" alt="1036592d2a7c3ef6ef6d498c54a6887" src="https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/5536f1c6-843d-449c-b6e0-c2b2eff781fd"> 

     - The model has 95% accuracy of predicting whether a customer will churn or not.

 **3. LOGISTIC REGRESSION MODEL**
   
**ANALYZING THE CONFUSION MATRIX FOR THE LOGISTIC REGRESSION MODEL.** 

 <img width="254" alt="50ecbae6d322bf79039d37297d3b635" src="https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/e7fb6917-da71-440b-9c11-02f252c03212">


**CLASSIFICATION METRICS FOR THE LOGISTIC REGRESSION MODEL.**

   <img width="470" alt="219d0d15b2fab7218b82479b377e2eb" src="https://github.com/cynthiadalmas/PREDICTING-CUSTOMER-CHURN-USING-MACHINE-LEARNING-ALGORITHMS/assets/128845927/086a2a61-bca8-456a-8c1d-a19f098e499a"> 

**MODEL EVALUATION**
   - AFTER evaluating the model performances and metrics. Decision tree model proved to be the best model for predcitng churn among customers.

**FINDINGS**

- Decision tree model was the best to predict churning among customers in this analysis.
- The classification metrics of the model were: Accuracy-94%,Precision-95%, Recall-94% and F1-Score-95%.

**RECOMMENDATIONS**

- I would recommend that Syria Tel Company should use large datasets to test the performance model.
- Syria Tel company can do product development more frequently to keep up with the consistent change in customer taste.
- Add more enticing features to products according to daily trends in fashion,music, entertainment,sports,holidays.
- Invest more on advertising to maintain awareness amongst it's customers ang even gain new ones.
- Take customer service seriously, analyze daily calls and ensure all reported issues are resolve in a timerly manner. This is because the analysis showed, most customers who churn, had contacted the Customer service more that once.
- Reduce charges on minute rate to prevent the 19% of customers who churned due to charges incurred from churning.

**FOR MORE INFOMATION PLEASE REVEIW Notebook and Presentation attached. 

     

  
