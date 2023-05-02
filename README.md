# Credit Scoring
Credit Scoring. Machine Learning for Finance Final Project

Lim Choo Siong 2201213784
Martin Adrian 2201213787

## Brief Introduction
The project will explore some aspect mainly in data preprocessing and classifier. We use some different ways to input the missing value, transform the data, resampling, and also the machine learning classifier that was used. Rather than choosing only 2 or some features using PCA, we decided to try to explore some combination of the feature (2 features) and rank the result. The metrics that was mainly important were precision and f1. However, we also take into acount the roc auc (TPR vs FPR) of the model.

## Higlighted Result
Based on the analysis, the best combination of variables is var8_woe, var4, and var5. This combination has a precision score of 0.958, indicating that 95.8% of loans that the model predicts as good are actually good loans. The F1 score of 0.9595, which is the harmonic mean of precision and recall, provides a combined measure of precision and recall for the model.
<!-- https://csvtomd.com/#/ -->
|      | variable           | precision | recall | f1    | auc   | auc+f1+prec | data_fill | transformation | resample | classifier | auc+f1 |
| ---- | ------------------ | --------- | ------ | ----- | ----- | ----------- | --------- | -------------- | -------- | ---------- | ------ |
| 1534 | var8_woe,var4,var5 | 0.958     | 0.961  | 0.959 | 0.663 | 2.58        | mean      | stdscl         | upsample | DT         | 1.622  |
| 6613 | var2,var4,var8     | 0.957     | 0.93   | 0.943 | 0.673 | 2.573       | mean      | minmax         | upsample | LR         | 1.615  |
| 6009 | var8_woe,var3,var4 | 0.958     | 0.954  | 0.956 | 0.658 | 2.572       | mean      | minmax         | upsample | DT         | 1.614  |
| 6413 | var5_woe,var4,var8 | 0.957     | 0.93   | 0.943 | 0.67  | 2.57        | mean      | minmax         | upsample | LR         | 1.613  |
| 6468 | var6_woe,var4,var8 | 0.957     | 0.93   | 0.943 | 0.67  | 2.57        | mean      | minmax         | upsample | LR         | 1.613  |

![Confusion Matrice](https://github.com/martinbandung/2023_MLF_Project/blob/main/images/choose/20230501_conmat_mean_DT_upsample_stdscl_var8_woe_var4_var5.png)
![TPR vs FPR](https://github.com/martinbandung/2023_MLF_Project/blob/main/images/choose/20230501_TPRvsVPR_mean_DT_upsample_stdscl_var8_woe_var4_var5.png)