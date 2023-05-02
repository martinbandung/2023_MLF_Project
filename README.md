# Credit Scoring
Credit Scoring. Machine Learning for Finance Final Project

Lim Choo Siong 2201213784
Martin Adrian 2201213787

## Brief Introduction
The project will explore some aspect mainly in data preprocessing and classifier. We use some different ways to input the missing value, transform the data, resampling, and also the machine learning classifier that was used. Rather than choosing only 2 or some features using PCA, we decided to try to explore some combination of the feature (2 features) and rank the result. The metrics that was mainly important were precision and f1. However, we also take into acount the roc auc (TPR vs FPR) of the model.

## Higlighted Result
Based on the analysis, the best combination of variables is var8_woe, var4, and var5. This combination has a precision score of 0.958, indicating that 95.8% of loans that the model predicts as good are actually good loans. The F1 score of 0.9595, which is the harmonic mean of precision and recall, provides a combined measure of precision and recall for the model.

|      | variable           | precision          | recall             | f1                 | auc                | auc+f1+prec        | data_fill | transformation | resample | classifier | auc+f1             |
| ---- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | --------- | -------------- | -------- | ---------- | ------------------ |
| 1534 | var8_woe,var4,var5 | 0.9580720324462888 | 0.9608936676212966 | 0.9594571111598256 | 0.66288517087805   | 2.5804143144841643 | mean      | stdscl         | upsample | DT         | 1.6223422820378754 |
| 6613 | var2,var4,var8     | 0.9571689807571852 | 0.930111038536904  | 0.9428355445817836 | 0.6725372520804107 | 2.57254177741938   | mean      | minmax         | upsample | LR         | 1.6153727966621942 |
| 6009 | var8_woe,var3,var4 | 0.9580159306946392 | 0.9543619889798858 | 0.9561574805437996 | 0.6581199702868805 | 2.572293381525319  | mean      | minmax         | upsample | DT         | 1.61427745083068   |
| 6623 | var3,var4,var8     | 0.957167893147488  | 0.9300942906429516 | 0.9428260331261028 | 0.6703405572484704 | 2.5703344835220614 | mean      | minmax         | upsample | LR         | 1.6131665903745733 |
| 6347 | var7_woe,var4,var8 | 0.9572101899082712 | 0.9303957527340936 | 0.9430056601287028 | 0.670033175983825  | 2.5702490260208    | mean      | minmax         | upsample | LR         | 1.6130388361125276 |
| 6468 | var6_woe,var4,var8 | 0.957167893147488  | 0.9300942906429516 | 0.9428260331261028 | 0.6698118083188083 | 2.569805734592399  | mean      | minmax         | upsample | LR         | 1.612637841444911  |
| 6413 | var5_woe,var4,var8 | 0.957167893147488  | 0.9300942906429516 | 0.9428260331261028 | 0.6698118083188083 | 2.569805734592399  | mean      | minmax         | upsample | LR         | 1.612637841444911  |
| 6178 | var3_woe,var4,var8 | 0.9571441106201154 | 0.9293741312030012 | 0.9424254595550218 | 0.6695536352090066 | 2.569123205384144  | mean      | minmax         | upsample | LR         | 1.6119790947640285 |
| 6634 | var4,var6,var8     | 0.957167893147488  | 0.9300942906429516 | 0.9428260331261028 | 0.6689672907630597 | 2.5689612170366507 | mean      | minmax         | upsample | LR         | 1.6117933238891626 |
| 6632 | var4,var5,var8     | 0.957167893147488  | 0.9300942906429516 | 0.9428260331261028 | 0.6687296546082259 | 2.5687235808818167 | mean      | minmax         | upsample | LR         | 1.6115556877343287 |
|      |

![Confusion Matrice](https://github.com/martinbandung/2023_MLF_Project/blob/main/images/choose/20230501_conmat_mean_DT_upsample_stdscl_var8_woe_var4_var5.png)
![TPR vs FPR](https://github.com/martinbandung/2023_MLF_Project/blob/main/images/choose/20230501_TPRvsVPR_mean_DT_upsample_stdscl_var8_woe_var4_var5.png)