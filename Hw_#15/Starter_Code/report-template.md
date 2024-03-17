# Module 12 Report Template

## Overview of the Analysis    

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis:

    - To evaluate the performance of two logistic regression machine learning models in predicting the credit
      risk associated with loans.

    - To predict whether loaning to a certain individual would be credit-worthy or high-risk 

* Explain what financial information the data was on, and what you needed to predict:

    - The financial data focused on loan size, interest rate, borrower income, debt-to-income ratio, 
      number of accounts, derogatory remarks, and total debt. 

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`):

    -  To predict the loan status, either as a healthy loan (0) or high-risk loan (1).

* Describe the stages of the machine learning process you went through as part of this analysis:

1. Splitting the data into training and testing datasets
2. Creating and fitting a logistic regression model with the original data
3. Evaluating the model's performance using accuracy, precision, and recall scores
4. Resampling the data using RandomOverSampler to address class imbalance
5. Creating and fitting another logistic regression model with the resampled data
6. Evaluating the performance of the resampled model using the same metrics

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms):

    - Methods used in this analysis include LogisticRegression and RandomOverSampler for resampling.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores:

Accuracy: The overall accuracy of the model is 0.99, indicating that it correctly classifies 99% of the instances.
Precision:

 - Healthy loans (0): The model has a precision of 1.00, which means it's excellent at identifying true positives with very few false positives.
 - High-risk loans (1): The model has a precision of 0.87, indicating its moderate effectiveness in identifying high-risk loans with some false positives.
Recall:

 - Healthy loans (0): The model has a recall of 1.00, which means it's correctly identifying nearly all instances of healthy loans with very few false     negatives.
 - High-risk loans (1): The model has a recall of 0.89, indicating its effectiveness in identifying high-risk loans with some false negatives.


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?

    - According to the findings, the logistic regression model, trained using resampled data (referred to as Model 2), exhibits superior performance compared to the model trained with unaltered data (referred to as Model 1), especially concerning the prediction of high-risk loans. Model 2 displays elevated precision and recall metrics for high-risk loans, attributes that are paramount in mitigating prospective financial liabilities for the lending institution.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

    - Yes it does, depending on which side of the coin we are trying to land on, the performance could be seen as positive or negative towards a respective goal. That being said, in this case I think it would be better for a company to find the 0's rather than the 1's because (assuming the parameters for finding a 0 candidate are solid and have a high probability of the client re-paying the loan) then we could just automate the application process so that 0's are automatically approved while those who do not meet the categories of 0 for whatever reason get denied. 

If you do not recommend any of the models, please justify your reasoning:

    - It is advised to employ the logistic regression model trained utilizing resampled data (referred to as Model 2) for the analysis of credit risk, given its notable advancement in the prediction of high-risk loans in contrast to the initial model. This particular model is anticipated to assist the organization in proficiently evaluating loan applications and in making judicious decisions pertaining to loan approvals or rejections, thereby effectively managing credit risk.