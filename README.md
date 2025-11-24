<h1 align="center">📘 Automated Essay Scoring (AES)</h1>

<div style="border: 2px solid #4CAF50; padding: 15px; border-radius: 10px; margin-bottom: 20px;">
  <h3>📌 Project Overview</h3>
  <p>
    This project implements an Automated Essay Scoring (AES) system trained on the 
    <b>Learning Agency Lab – AES 2 Kaggle dataset</b>. The system evaluates essays 
    based on linguistic richness, coherence, structure, and semantic quality to predict 
    their final human-assigned score.
  </p>
</div>

---

📂 Project Structure

```text
AES-Project/
│
├── Dataset/
│   ├── train.zip
│   └── test.csv
│
├── Notebook/
│   └── Model_Usage.ipynb
│
├── References/
│   └── CEP.pdf
│
├── requirements.txt
├── .gitignore
├── LICENSE
└── README.md
```
---
<div style="border: 1px solid #2196F3; padding: 15px; border-radius: 10px; margin-bottom: 20px;"> <h3>📊 Dataset Description</h3> <p> The dataset comes from the <b>Learning Agency Lab Automated Essay Scoring 2</b> challenge (Kaggle). It contains thousands of student essays, each scored by human graders. </p> <p><b>Included in the dataset:</b></p> <ul> <li>Essay text</li> <li>Human-assigned scores</li> <li>Essay set information</li> <li>Training & testing partitions</li> </ul> </div>
<Figure size 600x400 with 1 Axes><img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/77de8ff2-b655-48e1-9cf0-ed440b8d0b9c" />

🧹 Preprocessing Pipeline
<div style="border: 1px solid #FF9800; padding: 15px; border-radius: 10px;"> <ul> <li>Lowercasing & normalization</li> <li>Removing special characters</li> <li>Tokenization (NLTK + spaCy)</li> <li>Lemmatization</li> <li>Stopword removal</li> <li>Sentence segmentation</li> <li>Grammar/spelling cleanup</li> <li>Removal of extremely short essays</li> </ul> </div>
🧠 Feature Engineering
<div style="border: 1px solid #673AB7; padding: 15px; border-radius: 10px;"> <h4>Extracted Feature Groups</h4> <ul> <li><b>Lexical Features:</b> word count, unique words, vocabulary richness</li> <li><b>Syntactic Features:</b> POS ratios, sentence lengths</li> <li><b>Semantic Features:</b> TF-IDF, transformer embeddings</li> <li><b>Error-Based Features:</b> grammar & spelling errors</li> <li><b>Structural Features:</b> paragraph count, transitions</li> </ul> </div>

---
🔥 **Model Comparison**
<div style="border: 1px solid #9C27B0; padding: 15px; border-radius: 10px;"> <table> <thead> <tr> <th>Model</th> <th>R² Score</th> <th>Notes</th> </tr> </thead> <tbody> <tr> <td><b>Linear Regression</b></td> <td>0.40–0.45</td> <td>Simple baseline</td> </tr> <tr> <td><b>Random Forest</b></td> <td>~0.68</td> <td>Strong classical model</td> </tr> <tr> <td><b>Gradient Boosting</b></td> <td>~0.70</td> <td>Handles non-linear patterns</td> </tr> <tr> <td><b>XGBoost</b></td> <td>~0.75</td> <td>High performance</td> </tr> <tr> <td><b>BERT / RoBERTa Regression Model</b></td> <td>0.80–0.82</td> <td>Best overall results</td> </tr> </tbody> </table> </div>
<Figure size 600x400 with 1 Axes><img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/1c8458b7-58fe-4703-8703-0b534f1f21d6" />

---
📘**Notebook: Model_Usage.ipynb**

**The notebook performs:**

Dataset loading
Full preprocessing pipeline
Feature engineering
ML + Transformer model training
Model evaluation
Generating predictions
<h2 style="font-weight:700; margin-bottom:10px;">🚀 How to Run the Project</h2> <div style=" border: 1px solid #ddd; padding: 18px; border-radius: 10px; background: #fafafa; ">
<h3 style="margin-top:0; color:#333;">1. Install Dependencies</h3>
<p>Make sure Python 3.8+ is installed, then run:</p>
<pre style="
    background:#272822; 
    color:#f8f8f2; 
    padding:12px; 
    border-radius:6px;
    overflow:auto;
"><code>pip install -r Requirements.txt</code></pre>

<h3 style="color:#333;">2. Download spaCy Language Model</h3>
<p>This project uses spaCy for text preprocessing. Install the required model:</p>
<pre style="
    background:#272822; 
    color:#f8f8f2; 
    padding:12px; 
    border-radius:6px;
    overflow:auto;
"><code>python -m spacy download en_core_web_sm</code></pre>

<h3 style="color:#333;">3. Open the Notebook</h3>
<p>Run the main project notebook from your preferred environment:</p>

<ul>
    <li>Google Colab</li>
    <li>Jupyter Notebook</li>
    <li>VS Code (Jupyter Extension)</li>
</ul>

<pre style="
    background:#272822; 
    color:#f8f8f2; 
    padding:12px; 
    border-radius:6px;
    overflow:auto;
"><code>Notebook/Model_Usage.ipynb</code></pre>

<p style="margin-top:20px; font-weight:600; color:#444;">
    ✔️ After completing these steps, the system is ready for use.
</p>

---
📄 **License**

This project is licensed under the MIT License.

📎 **References**

Kaggle AES 2 Dataset

CEP PDF (in /References/)

Standard NLP & AES literature
