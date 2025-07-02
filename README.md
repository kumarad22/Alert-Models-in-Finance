# 🧾 Credit Risk Classification – MBA786A Group Project

> A supervised learning project aimed at classifying credit applicants as "Good" or "Bad" credit risk using various binary classification algorithms and evaluation metrics.

---

## 👥 Team Members

- **Sabari S (208170829)** – Q1 Code
- **Deeksha Rawat (210303)** – Preprocessing & Q4 (Code + Report)
- **Shorya Agarwal (221023)** – Q2 (Code + Report), Q3 Report
- **Kumar Aditya (220559)** – Q3 Code
- **Harsh Nirmal (220431)** – Q1 Report

---

## 📊 Dataset Overview

- 62 features related to credit applicants (e.g., Duration, Amount, Age)
- Binary target variable: **Good (0)** or **Bad (1)**
- Imbalanced distribution: ~70% "Good", ~30% "Bad"

---

## 🧪 Project Objectives

- Build robust models to predict credit risk
- Compare multiple classifiers: Logistic Regression, Decision Tree, Random Forest, Bagging, KNN, and SVM
- Evaluate trade-offs between **recall**, **precision**, **accuracy**, **FPR**, and **AUC**
- Address **class imbalance** using SMOTE

---

## 🔍 Methods & Models Used

### ✅ Logistic Regression

- Evaluated at thresholds: 0.20, 0.35, 0.50
- Best performance at **0.35**:
  - Accuracy: 78%
  - Precision: 0.63
  - Recall: 0.68
  - AUC: 0.7104

### 🌳 Tree-Based Models (Q2)

- **Classification Tree**:
  - Accuracy: 70%
  - AUC: 0.6296

- **Bagging**:
  - Accuracy: 73.67%
  - AUC: 0.7818

- **Random Forest**:
  - Accuracy: 76.33%
  - AUC: **0.7962** ✅ (Best)

### 📈 K-Nearest Neighbors (KNN, Q3)

- K = 1, 3, 5, 10 (with standardized features)
- Best AUC = 0.777 at K=10 (with selected features)

### 🔲 Support Vector Machine (SVM, Q4)

- Grid Search: C = 0.1, Gamma = 1, Kernel = Linear
- Accuracy: 79.17%
- Precision: 0.69
- Recall: 0.477
- Used SMOTE to improve recall to 77.7%

---

## ⚖️ Imbalanced Dataset Handling

- Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance classes
- Helped improve recall significantly for minority class (Bad credit)
- Trade-off: Slightly more false positives, but fewer missed bad cases

---

## 📉 Metrics Tracked

- Accuracy
- Precision
- Recall (TPR)
- False Positive Rate (FPR)
- AUC (Area Under ROC Curve)

---

## 📌 Results Summary

| Model            | Accuracy | Precision | Recall | FPR  | AUC    |
|------------------|----------|-----------|--------|------|--------|
| Logistic (0.35)  | 78%      | 0.63      | 0.68   | 0.18 | 0.7104 |
| Decision Tree    | 70%      | 0.50      | 0.45   | 0.19 | 0.6296 |
| Bagging          | 73.67%   | 0.76      | 0.42   | 0.09 | 0.7818 |
| Random Forest ✅ | 76.33%   | 0.69      | 0.39   | 0.07 | **0.7962** |
| KNN (K=10)       | 73.00%   | 0.77      | 0.42   | —    | 0.777  |
| SVM              | 79.17%   | 0.69      | 0.477  | 0.09 | ~0.75 (est.) |

✅ **Best Model:** Random Forest (balanced performance + highest AUC)

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install numpy pandas scikit-learn matplotlib seaborn imbalanced-learn
