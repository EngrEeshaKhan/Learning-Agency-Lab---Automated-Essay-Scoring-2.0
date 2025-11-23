# Learning-Agency-Lab---Automated-Essay-Scoring-2.0
Improve upon essay scoring algorithms to improve student learning outcomes
<h1 align="center">📘 Automated Essay Scoring (AES)</h1>

<div style="border: 2px solid #4CAF50; padding: 15px; border-radius: 10px; margin-bottom: 20px;">
  <h3>📌 Project Overview</h3>
  <p>
  This repository contains an Automated Essay Scoring (AES) system designed to evaluate student essays
  using Natural Language Processing (NLP) and supervised Machine Learning models. The system follows
  the official CEP (Comprehensive English Program) essay marking criteria, focusing on coherence,
  grammar, organization, vocabulary richness, and content quality.
  </p>
</div>

---

## 📂 Project Structure


---

<div style="border: 1px solid #2196F3; padding: 15px; border-radius: 10px; margin-bottom: 20px;">
  <h3>📊 Dataset Description</h3>
  <p>
  The dataset used in this project contains essays written by students and scored by certified evaluators
  following the CEP marking rubric. Each essay includes scores for:
  </p>
  <ul>
    <li><b>Content quality</b></li>
    <li><b>Organization & structure</b></li>
    <li><b>Grammar & mechanics</b></li>
    <li><b>Vocabulary richness</b></li>
    <li><b>Coherence & cohesion</b></li>
    <li><b>Final overall score</b> — the prediction target</li>
  </ul>
</div>

---

## 🧹 Preprocessing Workflow

<div style="border: 1px solid #FF9800; padding: 15px; border-radius: 10px;">
  
- Lowercasing text  
- Removing stopwords  
- Lemmatization  
- Removing special characters  
- Sentence segmentation  
- Tokenization  
- Spell correction  
- Dropping extremely short essays  
- Handling missing values  
- Standardizing scoring fields  

</div>

---

## 🧠 Feature Engineering

### Extracted Feature Categories

| Category | Features |
|---------|----------|
| **Lexical** | Word count, unique words, type-token ratio |
| **Syntactic** | POS tag proportions, sentence length distribution |
| **Semantic** | TF-IDF vectors, embedding-based similarity |
| **Error-based** | Grammar errors, spelling mistakes |
| **Structural** | Paragraph count, transition indicators |

---

## 🔥 Machine Learning Models Evaluated

<div style="border: 1px solid #9C27B0; padding: 15px; border-radius: 10px;">

### **Model Comparison Table**

| Model | R² Score | Notes |
|-------|----------|-------|
| **Linear Regression** | 0.41 | Simple baseline |
| **Random Forest Regressor** | 0.68 | Stronger baseline |
| **Gradient Boosting** | 0.72 | Handles non-linear patterns |
| **XGBoost** | 0.76 | High performance on engineered features |
| **BERT-based Regression Model** | 0.82 | Best performance; understands context deeply |

</div>

---

## 🧪 Training Pipeline Included in Notebook

The notebook performs the following:

- Load CEP essay dataset  
- Clean & preprocess essays  
- Generate linguistic, semantic, & structural features  
- Vectorize text (TF-IDF or transformer embeddings)  
- Train multiple machine learning models  
- Evaluate their accuracy and R² performance  
- Export model predictions & graphs  

---

## ▶️ How to Run This Project

### **1️⃣ Install Dependencies**
```bash
pip install -r requirements.txt

