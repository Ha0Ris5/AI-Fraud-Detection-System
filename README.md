# AI Fraud Detection

## Coursework 1 – Artificial Intelligence  
**Dr Zied M’nasri**  

### An Insight into How Machine Learning is Being Used to Detect and Prevent Fraud  

**Authors:**  
- Haris Mahmood: 23012399  
- Adam Akhtar: 23008644  

---

## Abstract
This report critiques the use of AI in online banking, specifically in fraud detection. It includes a real-life example, an application of machine learning, and the advantages/disadvantages of using this method.

## Introduction
Fraud is defined as an act of deception that rewards the perpetrator while denying the rights of the victim. According to Kesseler (2024), scammers manipulate victims by deceiving them into approving payments. The Nasdaq Verafin 2024 Global Financial Crime Report estimates that digital fraud schemes led to $485.6 billion in losses in 2023 alone. This report explores how AI, particularly supervised machine learning, is used to detect and prevent fraud in online banking.

## Background Learning
Studies suggest that 20% of online customers have been targeted by phishing or identity theft attempts. Banks rely on online banking to reduce operational costs and maintain services during crises (e.g., COVID-19 pandemic). Fraud, however, remains a significant issue, with a 92% increase in attempted fraud transactions and a 146% surge in fraud amounts in 2022 (Khokkar, 2024).

AI, specifically supervised learning, plays a crucial role in fraud detection. Supervised learning trains algorithms on labeled datasets to classify data and predict fraudulent transactions. Techniques such as transaction pattern analysis and chatbots detecting suspicious behavior help identify fraud. However, false positives can be an inconvenience for customers.

## Methodology and Data
Financial institutions employ supervised learning methods like decision trees and logistic regression to identify fraudulent transactions. Features such as transaction amount, location, time, user behavior, and frequency help classify transactions as fraudulent or non-fraudulent.

### Example – Supervised Learning in Financial Services
A real-life example of fraud detection is **PayPal**, which uses fraud detection models to identify suspicious activity. PayPal scores transactions based on historical data, user behavior, and risk factors to detect potential fraud.

### Machine Learning Fraud Detection Model
A **logistic regression model** was trained on a Kaggle dataset containing **284,808** credit card transactions over two days. The dataset is highly imbalanced, with fraudulent transactions being a small percentage of total records.

#### Steps to Train the Model:
1. **Import Libraries** – Pandas, Scikit-learn, Matplotlib, Seaborn
2. **Load Dataset** – `creditcard.csv`
3. **Preprocess Data** – Remove missing values, define input (`X`) and output (`Y`)
4. **Split Data** – 50% training, 50% testing (`stratify=y` ensures balance)
5. **Standardize Data** – Normalize input features
6. **Train Model** – Logistic Regression (`sigmoid` function used for classification)
7. **Evaluate Performance** – Use a confusion matrix to assess accuracy

## Data Visualization
The **confusion matrix** breaks down model performance:
- **True Negatives (TN):** Correctly predicted non-fraud transactions
- **False Positives (FP):** Non-fraud transactions incorrectly flagged as fraud
- **False Negatives (FN):** Fraud transactions wrongly classified as non-fraud
- **True Positives (TP):** Correctly predicted fraud transactions

### Classification Report
- **Precision, Recall, and Accuracy** metrics evaluate model performance.
- The logistic regression model achieved **98% accuracy** in fraud detection.

## Analysis and Discussion
### Strengths
1. **Real-time Detection** – AI enables rapid fraud identification and resource optimization.
2. **High Accuracy** – The model correctly detects fraud with **98% accuracy**, minimizing false positives and negatives.

### Limitations
1. **Dependence on Data Quality** – Accuracy depends on high-quality, comprehensive data.
2. **Handling of Imbalanced Data** – Fraudulent transactions are a small fraction of total transactions, making classification challenging.

## Conclusion and Future Work
AI shows promising potential for fraud detection with high accuracy and efficiency. However, its effectiveness relies heavily on data quality. Future research should explore techniques like **synthetic data generation and deep learning models** to improve fraud detection in financial institutions.

---

## How to Run the Model
1. Install dependencies:  
   ```bash
   pip install pandas scikit-learn matplotlib seaborn
   ```
2. Load dataset in Python:
   ```python
   import pandas as pd
   data = pd.read_csv('creditcard.csv')
   ```
3. Train the logistic regression model (see methodology section for steps).
4. Evaluate model performance using a confusion matrix.

---

## References
- Kesseler, 2024. **Nasdaq Verafin 2024 Global Financial Crime Report**.
- Khokkar, 2024. **NICE Actimize Fraud Detection Analysis**.

---

**License:** MIT
