# Credit Scoring
Credit Scoring. Machine Learning for Finance Final Project

Lim Choo Siong 2201213784
Martin Adrian 2201213787

## Brief Introduction
The project will explore some aspect mainly in data preprocessing and classifier. We use some different ways to input the missing value, transform the data, resampling, and also the machine learning classifier that was used. Rather than choosing only 2 or some features using PCA, we decided to try to explore some combination of the feature (2 features) and rank the result. The metrics that was mainly important were precision and f1. However, we also take into acount the roc auc (TPR vs FPR) of the model.

## Higlighted Result
Based on the analysis, the best combination of variables is var8_woe, var4, and var5. This combination has a precision score of 0.958, indicating that 95.8% of loans that the model predicts as good are actually good loans. The F1 score of 0.9595, which is the harmonic mean of precision and recall, provides a combined measure of precision and recall for the model.
![Confusion Matrice](https://github.com/martinbandung/2023_MLF_Project/blob/main/images/choose/20230501_conmat_mean_DT_upsample_stdscl_var8_woe_var4_var5.png)
![TPR vs FPR](https://github.com/martinbandung/2023_MLF_Project/blob/main/images/choose/20230501_TPRvsVPR_mean_DT_upsample_stdscl_var8_woe_var4_var5.png)