# Telecom_Churn_Prediction
This Project Explore Key Churn Driver Utilizing Extended python Library such as SHAP and LIME

## Data
The Orange Telecom's Churn Dataset, which consists of cleaned customer activity data (features), along with a churn label specifying whether a customer canceled the subscription, will be used to develop predictive models. Two datasets are available here: The churn-80 and churn-20 datasets can be downloaded.<br>
The link to data can be found here: https://www.kaggle.com/datasets/mnassrib/telecom-churn-datasets

## Model Building & Selection
Three classification models where built including LogisticRegression, RandomForest and MLPClassifier.<br>
Overall, RandomForest performed better on the testing dataset with an accuracy of 96%. But with lesser sensitivity when compared to LogisticRegression model indicating the models ability to catch churners. <br>
RandomForest model was choosing and the prediction weight were changed in order to improve the sensitivity (0.73 -> 0.80).

## Comments On Feature Importances & Possible Churn Drivers.
### Churn Drivers
The most important feature which contributes to models prediction of a churn are;
* Number of customer service calls.
* Whether a customer is sign up on an international call plan.
* Total day voice usage/charge.

All this features are envident using the model specific and agnostic method like SHAP.

To better understand how this features impact churn, the beeswarm plot shows that;
* Higher customer service calls contribute to churn (categorically calls > 2). Which might indicate either low customer satisfaction or unresolved issues.
* Customers on international plan tend to churn more. which indicate how price-sensitive this customers maybe due to higher charges on international calls leading to bill shocks.
* Higher day usages/charges (Voice). Higher consumers are susceptible to churn since they tend to scout for cheaper offers in the market.

### Solutions.
* Prioritize Customers with higher service calls (calls >2) to attend their issues (billing dispute, networt/SIM issues etc.).
* Solve Pain point of customers on international plan by reviewing international plan pricing, offering discounted offers, and investigating customer complaint.
* Realign product offers for higher users (product personalization) and providing real-time alert on usage to prevent bill shocks.
