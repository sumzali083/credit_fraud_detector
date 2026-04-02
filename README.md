# credit_fraud_detector
Dataset: Credit Card Fraud Detection Dataset  
Source: Kaggle (Machine Learning Group - ULB)  
Link: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

# Credit Card Fraud Detection

## Overview

This project looks at detecting fraudulent credit card transactions using machine learning. The dataset is very imbalanced, meaning there are way more normal transactions than fraud ones, which makes the problem harder.

The aim was to build a model that can identify fraud as accurately as possible, especially focusing on not missing fraud cases.

---

## Dataset

* Around 284,000 transactions
* Only 492 are fraud (~0.17%)
* Features include:

  * Time and Amount
  * V1–V28 (anonymised features)
  * Class (0 = normal, 1 = fraud)

---

## What I did

### Data exploration

* Loaded the dataset and checked structure using `.head()`, `.info()`, etc
* Checked for missing values (none found)
* Looked at class distribution and confirmed strong imbalance

### Preprocessing

* Split the data into features (X) and target (y)
* Used a train/test split with stratification
* Scaled the Time and Amount columns

---

## Models

### KNN (baseline)

* Used as a first model to get a starting point
* Fraud recall: 0.72
* Missed quite a few fraud cases

---

### Random Forest (final model)

* Performed better than KNN
* Fraud recall: 0.83
* Fraud precision: 0.95
* Fewer missed fraud cases (17 instead of 27)

---

## Results

Random Forest clearly performed better than KNN.

Main improvement:

* Caught more fraud cases
* Reduced missed fraud
* Better overall balance between precision and recall

---

## Key takeaway

Accuracy isn’t very useful here because the dataset is so imbalanced.

It’s more important to focus on:

* Recall (how many frauds we catch)
* Confusion matrix (how many we miss)

---

## Conclusion

KNN worked as a basic model, but Random Forest gave much better results for fraud detection.

If this was used in a real system, the Random Forest model would be preferred because it misses fewer fraud cases.

---

## Future improvements

* Try handling imbalance better (e.g. resampling)
* Test other models
* Tune hyperparameters
* Add visualisations

---

## Tools used

* Python
* Pandas
* Scikit-learn
* VS Code / Jupyter

---

## Author

Summer Ali
