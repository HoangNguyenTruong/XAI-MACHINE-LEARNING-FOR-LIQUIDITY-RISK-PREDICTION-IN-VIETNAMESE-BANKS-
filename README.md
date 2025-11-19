# XAI-MACHINE-LEARNING-FOR-LIQUIDITY-RISK-PREDICTION-IN-VIETNAMESE-BANKS-
This repository contains all codes (Python), dataset for liquidity risk prediction in Vietnamese banks

# Goal

Build machine learning models to develop an early warning framework for liquidity risk in Vietnamese banks and employs Explainable AI (SHAP model) to interpret the operational mechanisms of the prediction model.

# Data Description

* Quarterly panel data from 27 listed banks (2014–2024) with these features

Funding Gap ratio (FGAP): The ratio of the difference between total loans and total deposits to total assets

Liquid Assets to Total Assets ratio (LIQ): The ratio of liquid assets to total assets

Liquid Assets to Total Deposits ratio (LTD): The ratio of liquid assets to total deposits

Equity to Assets ratio (ETA): The ratio of total equity to total assets

SIZE: The scale of a bank is measured by the natural logarithm of total assets.

Return on Equity (ROE): ROE shows how much net profit a hundred units of equity capital brings to the business

Non-performing Loans ratio (NPL): The ratio of non-performing loans (loan groups 3–5) to total loans

Deposit to Assets ratio (DTA): The ratio of customer deposits to total assets 

GDP growth rate (GDP): The GDP growth rate 

Inflation rate (INF): Inflation is measured by the consumer price index

Credit growth (DC):   The credit growth rate reflects the increase in credit extended by financial institutions (primarily banks)

# Results of the project
* Model evaluation

| Model   | AUC (%) | Precision (%) | Recall (%) | F1-Score (%) | Accuracy (%) |
|---------|---------|---------------|------------|--------------|--------------|
| LR      | 88.34   | 80.77         | 25.30      | 38.53        | 64.55        |
| RF      | 89.07   | 73.58         | 93.98      | 82.54        | 82.54        |
| Xgboost | 92.42   | 84.88         | 87.95      | 86.39        | 87.83        |


<img width="988" height="277" alt="image" src="https://github.com/user-attachments/assets/604b5dd0-d2f9-422a-94cd-c6c9c614f7db" />

<img width="982" height="272" alt="image" src="https://github.com/user-attachments/assets/9998beb0-eceb-40d8-8ddf-ef328312fcf7" />

The model comparison demonstrates XGBoost as the most effective approach for predicting liquidity risk. XGBoost achieved the highest scores across all key metrics with AUC (92.42%), Precision (84.88%), Recall (87.95%), F1-Score (86.39%), and Accuracy (87.83%). 


*  The ranking of the feature importance for the whole model


<img width="957" height="675" alt="image" src="https://github.com/user-attachments/assets/832245f0-0ab6-4a5b-8d74-d2894d317a57" />


Customer Deposits to Total Assets (DTA) has the largest impact on liquidity risk, with higher values reducing risk by providing a stable funding base. In contrast, larger banks (SIZE) tend to have higher liquidity risk, possibly due to more aggressive lending or complex asset structures. Higher liquidity buffers (LIQ) lower the probability of distress, while elevated inflation (INF) increases liquidity stress. 

Similarly, high levels of Non-performing Loans (NPL) and credit growth (DC) raise liquidity risk, reflecting weaker asset quality and excessive lending. Conversely, higher Return on Equity (ROE) and Equity to Total Assets (ETA) reduce liquidity risk, indicating that well-capitalized and profitable banks are more resilient. Finally, stronger GDP growth slightly alleviates liquidity risk, showing that favorable macroeconomic conditions benefit the banking sector.

