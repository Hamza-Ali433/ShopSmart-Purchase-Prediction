# ShopSmart Purchase Prediction

## Project Overview

This project focuses on predicting whether a visitor will complete a purchase on an e-commerce website based on their browsing behaviour.

The dataset contains information about user sessions, including page visits, time spent on different sections of the website, bounce rates, exit rates, visitor type, month of visit, and other session-related attributes.

The objective is to build a machine learning model that can identify potential buyers before a purchase is made. Such predictions can help businesses improve marketing campaigns, personalize recommendations, and increase conversion rates.

---

## Problem Statement

ShopSmart is an e-commerce company that wants to better understand customer behaviour on its website.

Every day, thousands of visitors browse products, spend varying amounts of time on different pages, and interact with website content in different ways. However, not every visitor completes a purchase.

The goal of this project is to develop a classification model that predicts whether a visitor will make a purchase based on information collected during a browsing session.

---

## Dataset

The dataset contains 12,330 user sessions and includes:

* Administrative pages visited
* Administrative page duration
* Informational pages visited
* Informational page duration
* Product-related pages visited
* Product-related page duration
* Bounce rates
* Exit rates
* Page values
* Special day indicator
* Month
* Operating system
* Browser
* Region
* Traffic type
* Visitor type
* Weekend visit indicator
* Revenue (Target Variable)

Target Variable:

* 0 → No Purchase
* 1 → Purchase

---

## Project Workflow

### 1. Data Preprocessing

* Label Encoding of binary categorical variables
* One-Hot Encoding of Visitor Type
* One-Hot Encoding of Month
* Removal of duplicate and unnecessary columns

### 2. Exploratory Data Analysis (EDA)

Several visualizations were created to understand customer behaviour:

* Purchase distribution
* Numerical feature distributions
* Page Value vs Purchase
* Purchase trends by month
* Weekend vs Purchase
* Visitor Type vs Purchase

Correlation analysis was also performed to identify the most influential features.

### 3. Model Building

A Decision Tree Classifier was selected for the classification task.

The model was trained using:

* Train-Test Split (80-20)
* Stratified sampling to preserve class distribution

### 4. Hyperparameter Tuning

The following parameters were explored:

* max_depth
* min_samples_split

### 5. Cost Complexity Pruning

To reduce overfitting, Cost Complexity Pruning was applied using:

* ccp_alpha

The optimal pruning value was selected based on validation performance.

### 6. Model Evaluation

The final model was evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* Classification Report

---

## Results

Final Model Performance:

* Accuracy: 89.94%
* Precision: 71.07%
* Recall: 59.16%
* F1 Score: 64.57%

Confusion Matrix:

```text
[[1992   92]
 [ 156  226]]
```

The model achieved an F1 Score above the benchmark requirement and was able to identify purchasing customers with reasonable effectiveness while maintaining high overall accuracy.

---

## Tools and Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn

---

## Key Takeaways

* PageValues showed the strongest positive relationship with purchases.
* Higher Bounce Rates and Exit Rates were associated with lower purchase probability.
* Decision Tree pruning improved model generalization and reduced overfitting.
* Customer browsing behaviour can be effectively used to predict purchase intent.

---

