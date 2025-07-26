# 🔐 Cyberattack Impact Classification Using Machine Learning

This project applies machine learning to **automatically classify the impact of cyberattacks** based on textual descriptions using a `RandomForestClassifier`. It combines manual feature engineering, text preprocessing, and model training to help predict the category of impact such as `Credential Compromise`, `System Compromise`, `Data Leakage`, and more.

---

## 📊 Project Summary

- **Domain**: Cybersecurity + Natural Language Processing (NLP)
- **Dataset**: 14,000+ real-world incident descriptions
- **Tech Stack**: Python, scikit-learn, pandas, joblib
- **Goal**: Predict the `Impact_Grouped` category from free-form incident text
- **Accuracy Achieved**: **94.6%** on unseen test data
- **Use Case**: Useful in SOC dashboards, threat triage systems, and security automation tools

---

## 🎯 Problem Statement

Security teams often deal with **textual descriptions of incidents** with vague or unstructured impact statements. The manual process of categorizing these for severity and triage is slow and inconsistent. This project aims to:

> 🧠 Train a model that can **automatically predict the class of a cyberattack impact** using only its description.

---

## 💡 Approach

### 1. Data Labeling
- Manual and rule-based categorization of raw `Impact` values into high-level impact groups like:
  - Credential Compromise
  - System Compromise
  - Data Leakage
  - Unauthorized Access
  - Account Compromise
  - Denial of Service
  - AI/LLM Privacy Breach
  - and more...

### 2. Preprocessing
- Convert impact descriptions to lowercase
- Remove punctuation/special characters
- Tokenization & vectorization using `TfidfVectorizer`

### 3. Model Training
- **Model**: `RandomForestClassifier` from `sklearn.ensemble`
- **Vectorizer**: `TfidfVectorizer` from `sklearn.feature_extraction.text`
- Train-test split: 80/20
- Evaluation: `Accuracy`, `Classification Report`, and `Confusion Matrix`

---

## 🧪 Results

