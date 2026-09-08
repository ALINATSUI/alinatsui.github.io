---
title:  "Caishen: Fraud Detection on 6.3M Transactions"
excerpt:  "Gradient boosting fraud classifier tuned via GridSearchCV, achieving F1 = 0.741 on a severe class imbalance 6.3M row transaction dataset"
permalink:  "/projects/fraud-detection/"
---
**Overview**

#### Analyzes a 6.3 million row synthetic transactions dataset to predict fraudulent transactions while minimizing false positives, on a severaly imbalanced target -- only ~0.07% of transactions are fraudulent. 

**Workflow**
- Exploratory data analysis (univariate, bivariate and multivariate)
- Feature engineering (one-hot encoding for categorical features)
- Preprocessing and 70/30 train/test split
- Model training with Gradient Boosting
- Hyperparameter tuning via GridSearchCV
- Evaluation focused on F1 score, not accuracy


### Results
The tuned Gradient Boosting model achieved:  
- F1 score: 0.741
- Accuracy: 99.94%
- Confusion matrix: 1,905,408 true negatives
                    914 false positives  
                    829 false negatives  
                    1,635 true positives

F1 was prioritized over accuracy since fraud makes up only ~0.07% of transactions -- a model that simply predicted "not fraud" every time would already score ~99.93% accuracy while catching zero fraud. 

## Project Evidence

![Confusion Matrix](/assets/images/ConfusionMatrix.png)



![](/assets/images/Amt_Values_and_Frequency.png)



![](/assets/images/fraud_rate_by_type.png)



![](/assets/images/Txn_Amt_By_Type.png)


## Tech Stack
<span class = "tech-stack">
`Python` · `pandas` · `scikit-learn` · `Seaborn` · `Matplotlib` · `Rich` </span>