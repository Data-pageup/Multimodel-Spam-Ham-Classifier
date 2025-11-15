# 📱 SMS Spam Classifier

A simple **Ham/Spam SMS Classification** project using **Text Preprocessing, TF-IDF Vectorization, Naive Bayes, Logistic Regression, and Random Forest**.  
The goal is to automatically detect whether an SMS message is **spam (1)** or **ham (0)**.

---

## 🔹 Project Overview

- Dataset: **UCI SMS Spam Collection** ([link](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection))  
- **Unbalanced dataset:** majority of messages are `ham`.  
- Goal: Detect spam messages automatically.  
- Pipeline:
  1. **Text Cleaning** → lowercase, remove punctuation, remove stopwords, lemmatization.  
  2. **TF-IDF Vectorization** → uni-grams and bi-grams to convert text into numerical features.  
  3. **Model Training** → Multiple ML models.  
  4. **Evaluation** → Accuracy, Precision, Recall, F1-Score.  
  5. **Comparison** → Identify best model for spam detection.

---


---

## ⚙️ Preprocessing

- Lowercasing  
- Removing punctuation and numbers  
- Removing extra spaces  
- Tokenization  
- Stopword removal  
- Lemmatization  
- TF-IDF Vectorization (uni-grams & bi-grams)  

> **Purpose:** Prepare clean numerical features for machine learning models.

---

## 🧠 Models Used

1. **Naive Bayes (MultinomialNB)** → baseline  
2. **Logistic Regression** → standard linear model  
3. **Logistic Regression (Class Balanced)** → handles dataset imbalance  
4. **Random Forest (Class Balanced)** → ensemble method for robustness  

---

## 📊 Model Comparison

| Model            | Accuracy  | Precision | Recall   | F1-Score |
|------------------|-----------|-----------|----------|----------|
| Naive Bayes      | 0.970986  | 1.000000  | 0.770992 | 0.870690 |
| Logistic Reg.    | 0.947776  | 0.963855  | 0.610687 | 0.747664 |
| LogReg Balanced  | 0.970019  | 0.878788  | 0.885496 | 0.882129 |
| Random Forest    | 0.974855  | 0.990654  | 0.809160 | 0.890756 |

**Interpretation:**  
- **Naive Bayes:** Perfect precision but lower recall (misses some spam).  
- **Logistic Regression:** Fast but lower recall on spam.  
- **LogReg Balanced:** Better recall for spam messages.  
- **Random Forest:** Best overall tradeoff between precision, recall, and F1-score.

---

by - Amirtha ganesh R



