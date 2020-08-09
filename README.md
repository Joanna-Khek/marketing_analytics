# [OPEN] Shopee Code League - Marketing Analytics
Shopee Code League is a 2-month online coding challenge consisting of a series of competitions, online algorithm questions and online training workshops open to all undergraduate students and professionals across the region (Singapore, China, Indonesia, Malaysia, Philippines, Taiwan, Thailand and Vietnam). 

## Background Information
The aim of this project is to build a model that can predict whether a user opens the emails sent by Shopee.

Sending emails is one of the marketing channels Shopee uses to reach out to our users. Being able to predict whether a user opens an email allows Shopee to forecast and evaluate the performance of future marketing campaigns before launch. This is because when a user opens an email, the probability of the user knowing the campaign increases and this in turn increases the probability of the user making a checkout during the campaign period. Therefore, with the predicted open rates, Shopee can better develop, strategize and implement future marketing campaigns.

## Task
We provide you with data related to marketing emails (Electronic Direct Mail) that were sent to Shopee users over a certain period. It contains information about

User-specific information
Email nature
Users’ engagement on the platform
User’s reaction to the email, including whether users opened the email
Based on the data provided, you must predict whether each user will open an email sent to him/her.

## Evaluation
Submissions are evaluated on the Matthews correlation coefficient (MCC) between the predicted and the observed response.

## Approach
- 3 models (LightGBM, XGBoost, CatBoost) were built separately and then ensembled (equal weightage of 1/3 each) to obtain final prediction.
- Since the data was unbalance, setting class_weights {0: 0.2, 1: 0.8} improved the model significantly.
- Using early_stopping_rounds helped to regularise the model
- Tried feature engineering but those features did not really help improve the model.
- There were many missing values and i treated them separately instead of imputing.



