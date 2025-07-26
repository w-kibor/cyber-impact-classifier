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
 Accuracy: 94.6%

### Top performing classes:

Credential Compromise (F1: 0.98)

Backdoor Access (F1: 0.97)

System Compromise (F1: 0.95)

AI/LLM Privacy Breach (F1: 0.92)

📈 *Weighted Average F1-Score*: **0.95**

## 🚀 How to Use
1. Clone the repository
```
git clone https://github.com/your-username/cyber-impact-classifier.git
cd cyber-impact-classifier
```
2. Install dependencies
```
pip install -r requirements.txt
```
3. Run the Notebook or Script

If using a Jupyter Notebook:
```
# Open and run Cyber_Attack_Impact_Prediction.ipynb
```
If using a Python script:
```
python train_model.py
```
4. Make Predictions
```
example = ["SQL injection on admin panel"]
vector = vectorizer.transform(example)
prediction = clf.predict(vector)
print("Predicted Impact Group:", prediction[0])

```
### 🧰 Prerequisites
#### Make sure you have the following installed:

Python 3.7+

pip (Python package installer)

#### You can install the required packages using:
```
pip install -r requirements.txt
```
#### Typical packages you might include in requirements.txt:

pandas

scikit-learn

numpy

matplotlib

seaborn

nltk

#### If you're using Jupyter Notebook or plan to visualize, also add:

jupyter

## 💬 Acknowledgments
This project was inspired by the real-world challenges of handling high-volume incident reports in cybersecurity environments. Thanks to the MITRE ATT&CK framework and numerous cybersecurity datasets available publicly.
