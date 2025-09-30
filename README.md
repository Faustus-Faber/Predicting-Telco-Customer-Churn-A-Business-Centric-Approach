# Predicting Telco Customer Churn: A Business-Centric Approach

!([https://placehold.co/800x300/f0f0f0/333333?text=Telco+Customer+Churn+Analysis](https://miro.medium.com/1*WZdoYPpmiIk1AcPQ1YHWug.png))

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings & Insights](#key-findings--insights)
- [Model Performance](#model-performance)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Contributors](#contributors)

---

## Project Overview

This project presents a robust, business-centric approach to predicting customer churn in the telecommunications industry. The primary goal is to develop a machine learning model that not only accurately identifies customers likely to churn but also optimizes for the financial impact of retention efforts. By focusing on a custom business metric that balances the costs of retention with the revenue saved, this analysis provides actionable insights to help reduce customer attrition.

The key challenge addressed is the high cost associated with acquiring new customers compared to retaining existing ones. This project tackles the problem by:
1.  Identifying the key drivers of customer churn through in-depth data analysis.
2.  Building and comparing multiple predictive models.
3.  Optimizing the best model based on a cost-benefit analysis to maximize business value.

---

## Dataset

The analysis is performed on the `telco_customer_churn.csv` dataset, which contains various customer attributes and their churn status.

-   **Source:** IBM Sample Data Sets
-   **Features:** The dataset includes customer demographics, account information (tenure, contract type, payment method), services they have signed up for, and churn information.

---

## Methodology

The project follows a structured data science workflow:

1.  **Exploratory Data Analysis (EDA):** A deep dive into the dataset to uncover patterns, relationships, and key features correlated with customer churn.
2.  **Data Pre-processing:** Cleaning the data, handling missing values, encoding categorical features, and scaling numerical features to prepare it for modeling.
3.  **Feature Engineering & Selection:** Creating and selecting the most impactful features to improve model performance.
4.  **Handling Class Imbalance:** The dataset is imbalanced, with fewer churners than non-churners. This was addressed using the **SMOTE (Synthetic Minority Over-sampling Technique)** to create a more balanced dataset for training.
5.  **Model Training & Evaluation:** Several classification algorithms were trained and evaluated, including:
    -   Logistic Regression
    -   Decision Tree
    -   Random Forest
    -   Gradient Boosting
    -   Support Vector Machines (SVM)
6.  **Business-Driven Optimization:** A custom business metric was developed to evaluate models based on the financial cost of false positives (unnecessarily targeting a happy customer) and the cost of false negatives (failing to identify a churner). The model's decision threshold was tuned to maximize this business score.

---

## Key Findings & Insights

-   **Contract Type is a Major Churn Driver:** Customers on **month-to-month contracts** are significantly more likely to churn compared to those with one or two-year contracts.
-   **Tenure Matters:** New customers (low tenure) have a higher churn rate. Loyalty increases with the length of the subscription.
-   **Payment Method:** Customers using **electronic checks** show a higher propensity to churn.
-   **Service Enrollment:** Customers without services like `OnlineSecurity`, `TechSupport`, and `OnlineBackup` are more likely to churn.

---

## Model Performance

The final selected model, a **Logistic Regression classifier with SMOTE and a tuned decision threshold**, was chosen for its excellent balance of performance and interpretability.

-   **High Recall:** The model successfully identifies a high percentage of actual churners, which was the primary business goal.
-   **Optimized Business Value:** By tuning the prediction threshold based on a cost-benefit matrix, the model was optimized to maximize net savings from retention campaigns, even at the cost of a lower precision.

---

## Getting Started

To run this analysis on your local machine, follow these steps:

**1. Clone the repository:**
```bash
git clone <your-repository-url>
cd <repository-directory>
