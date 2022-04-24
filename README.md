# Credit_Risk_Analysis
## Analysis Overview
In this project, we use Python to build and evaluate several machine learning models to predict credit risk.
We adopted the following process:

-Deliverable 1: Use Resampling Models to Predict Credit Risk
-Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
-Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk

## Results
### Random Oversampling

![image](https://user-images.githubusercontent.com/96096924/164995009-3ae9dc55-eeeb-413b-b81e-7724097d6f52.png)

![image](https://user-images.githubusercontent.com/96096924/164995021-a0cfa825-fa08-4750-9736-bdc31502068f.png)

The balanced accuracy score is 64.1%.
The high_risk precision is about 1% only with 60% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

### SMOTE model

![image](https://user-images.githubusercontent.com/96096924/164995196-37c55d6c-ad97-4462-a748-6aad0248fc69.png)

![image](https://user-images.githubusercontent.com/96096924/164995211-cf9611a0-13f7-4aeb-b804-7127878fdf4c.png)

The balanced accuracy score is 63.7%.
The high_risk precision is about 1% only with 60% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

### Undersampling

![image](https://user-images.githubusercontent.com/96096924/164995332-76df4078-cf88-4d9c-8f6d-f406d08350c0.png)

![image](https://user-images.githubusercontent.com/96096924/164995342-dadd4ae2-cbce-457a-9a68-c26ce7181e27.png)

Here the balanced accuracy score is down to about 51.6%.
The high_risk precision is still 1% only with 60% sensitivity which makes a F1 of 1%.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 43%.

### Combination (Over and Under) Sampling

![image](https://user-images.githubusercontent.com/96096924/164995443-d8557fa2-5ea0-49f8-9442-d019f00bb53c.png)

![image](https://user-images.githubusercontent.com/96096924/164995457-3663e6d8-43c9-4a45-b56d-0f42bbded131.png)

The balanced accuracy score is about 62.4%.
The high_risk precision is still 1% only with 70% sensitivity which makes a F1 of only 2%.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 55%.

### Balanced Random Forest Classifier

![image](https://user-images.githubusercontent.com/96096924/164995549-e9445245-4983-4d34-8902-9e122a08cf41.png)

![image](https://user-images.githubusercontent.com/96096924/164995559-248aedd9-7f8e-41ea-9691-ec445e36153f.png)

The balanced accuracy score improved to about 78.8%.
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.

### Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/96096924/164995617-360bfb96-31a9-441e-a88e-739fdbfe7f42.png)

![image](https://user-images.githubusercontent.com/96096924/164995627-2cb98ecc-1f48-483b-9bfb-9528c2363d21.png)

Now, the balanced accuracy score is high to about 92.5%.
The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

## Summary
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.
