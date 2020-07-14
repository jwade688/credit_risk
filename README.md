# credit_risk

## Challenge Overview
- Implement machine learning models.
- Use resampling to attempt to address class imbalance.
- Evaluate the performance of machine learning models.

# Analysis of each sampling model
- When oversampling with Naive Random Oversampling, the accuracy score was 62.3%. The precision was 1% true or 99% false which will be the case note mater what model is used because of the nature of this dataset. No matter what sampling model used most loans will fall in the low risk category and very few loans will fall in the high risk category so precision will always be the same. What's valuable is the recall. In this case 63% of the actual high risk loans were correctly predicted and 62% of the low risk loans were correctly predicted. If using this model to predict high risk loans, a good amount of high risk loans slipped through and were approved based on these predictions.
- Using SMOTE oversampling produced similar results. The accuracy score was 62.4% and again the precision was 1% true or 99% false. The recall using this model did show some differences. The recall of high risk loans dropped to 60%, but the recall of low risk loans increased to 65%. Unfortunately we are hoping to improve the recall of high risk loans. 
- Undersample proved to be not the correct model for prediction loan risk results. The overall accuracy of this model was 50.7%. The precision was the same as the other models. THe recall showed the lowest overall scores with 58% for high risk loans and 44% of low risk loans
- The most successful model for this context proved to be a comination of over and under sampling using the SMOTEENN algorithm. This algorithm produced the highest accuracy, 63.4%. The next closest algorithm was Naive Random Oversampling. The precision was the same as the other models. Where this algorithm succeeded was on the high risk recall at a high 72%. This is important because it will be the most accurate in correctly predicting this category. The recall for low risk lows was 55% which was not the best of the algorithms, but that is ok for this usage. 

# Final recommendation
- I would recommend using a comination of over and under sampling using the SMOTEEN algorithm on this dataset because it had the highest overall accuracy and also the highest recall for high risk loans. If we were to look deeper into low risk loans, I might recommend using the SMOTE algorithm. 