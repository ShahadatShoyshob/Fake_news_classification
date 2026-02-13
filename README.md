# Fake News Classification (NLP) — Traditional ML vs LSTM

This repository contains my university **Natural Language Processing (NLP)** coursework on **fake news detection**.  
The project compares **traditional machine-learning text classifiers** (using Bag-of-Words / TF‑IDF features) against a **deep learning LSTM** model (using word embeddings).

The main deliverables included in this repo are the exported report files:
- `fake_news_classification.pdf`
- `fake_news_classification.html`

---

## Project Goal

Build and compare multiple text-classification approaches for detecting **FAKE** vs **REAL** news articles, then evaluate them using:
- Accuracy
- Precision / Recall
- F1-score
- Confusion Matrix
- ROC-AUC (where applicable)

---

## Dataset

The project uses the **“Fake and Real News”** dataset from **Kaggle** (Clément Bisaillon).  
It contains news articles labeled as **FAKE** or **REAL**.

---

## Methods Implemented

### 1) Data Preprocessing
Typical NLP pipeline steps were applied, including:
- Cleaning and normalization (lowercasing, punctuation removal, etc.)
- Tokenization
- Stopword handling (NLTK)
- Train/test split for evaluation

### 2) Baseline & Traditional ML Models
Text features:
- **CountVectorizer** (Bag-of-Words)
- **TF‑IDF Vectorizer**

Classifiers compared:
- **Naive Bayes**
- **Logistic Regression**
- **Support Vector Machine (SVM)**
- **Random Forest**

### 3) Deep Learning Model
- **Embedding layer** (vocabulary-limited, sequence padding)
- **LSTM** network trained for fake/real classification

---

## Key Results (Summary)

From the final evaluation table in the report:

- **Random Forest (TF‑IDF)**: **98.90% accuracy**, **F1 ≈ 0.989**, ~10 seconds training  
- **LSTM (Embeddings)**: **97.89% accuracy**, **F1 ≈ 0.978**, ~2.5 minutes training

General takeaway:
- Traditional ML + TF‑IDF performed extremely strongly and is fast + interpretable.
- LSTM captures language nuance better in some cases, but is slower and less interpretable.

---

## Repository Contents

```
NLP/
├─ fake_news_classification.pdf     # exported coursework report
└─ fake_news_classification.html    # HTML version of the report
```

---

## How to View the Report

### Option A: PDF
Open:
- `NLP/fake_news_classification.pdf`

### Option B: HTML
Open:
- `NLP/fake_news_classification.html`

> Tip: If your browser blocks local file scripts/styles, serve it with a simple local server:
```bash
python -m http.server 8000
```
Then open:
- `http://localhost:8000/`

---

## Tools / Libraries Used (in the notebook that generated the report)

- Python (Jupyter Notebook)
- pandas, NumPy
- scikit-learn
- NLTK
- TensorFlow / Keras

---
