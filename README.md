[README_Text_Mining_NLP.md](https://github.com/user-attachments/files/28397626/README_Text_Mining_NLP.md)
# Text Classification & Topic Detection — NLP & Text Mining

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![NLP](https://img.shields.io/badge/NLP-Text%20Mining-red?style=flat-square&logo=spacy)
![BERT](https://img.shields.io/badge/Model-BERT%20Fine--tuned-yellow?style=flat-square&logo=huggingface)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![Type](https://img.shields.io/badge/Type-Classification%20%7C%20Topic%20Modelling-purple?style=flat-square)

---

## Project Overview

This project applies natural language processing (NLP) techniques to classify text and detect latent topics. The pipeline covers the full text mining workflow — from raw text preprocessing through to classical bag-of-words classifiers, BERT-based deep learning fine-tuning, and unsupervised topic modelling with LDA.

> **Goal:** Compare classical NLP classification approaches with transformer-based models, and extract meaningful themes from unstructured text data.

---

## Repository Structure

```
Text-Mining-NLP/
│
├── data/                                         # Raw text dataset
├── notebooks/
│   └── IDTA_Text_Mining_Assignment.ipynb         # Full analysis notebook
├── README.md
```

---

## Dataset

- **Type:** Text corpus for classification and topic detection
- **Task:** Multi-class or binary text classification + unsupervised topic discovery

---

## Analysis Breakdown

### Step 1 — Text Preprocessing Pipeline
A systematic preprocessing pipeline was applied to clean and normalise raw text:

| Step | Description |
|------|-------------|
| 1. Punctuation Removal | Strip all punctuation marks |
| 2. Digit Removal | Remove numerical characters |
| 3. Case Normalisation | Convert all text to lowercase |
| 4. Stop Word Removal | Remove common low-information words (NLTK stopwords) |
| 5. Lemmatisation | Reduce words to their base/dictionary form |

### Task 2 — Bag-of-Words Classification (3 Algorithms)
Classical machine learning classifiers applied to TF-IDF / BoW feature representations:

| Model | Approach |
|-------|----------|
| **Naïve Bayes** | Probabilistic baseline; fast and interpretable |
| **Random Forest** | Ensemble of decision trees; handles high-dimensional feature spaces |
| **SVM** | Support Vector Machine; strong performer on text classification tasks |

- Full performance comparison across accuracy, precision, recall, and F1-score
- Detailed analysis of where each model excels and where it struggles

### Task 3 — BERT-Based Classification with Fine-Tuning
- **Model:** Pre-trained BERT (`bert-base-uncased`) fine-tuned on the task dataset
- Tokenisation and input formatting for transformer architecture
- Fine-tuning with supervised training loop
- Evaluation on held-out test set
- **Direct comparison** with Task 2 classical models — quantifying the uplift from deep learning

### Task 4 — Topic Detection with LDA
- **Algorithm:** Latent Dirichlet Allocation (LDA)
- Unsupervised discovery of latent topics within the corpus
- Optimal number of topics determined through coherence score analysis
- Additional analysis performed to validate and interpret discovered topics

---

## Tools & Libraries

| Category | Tools |
|---|---|
| Language | Python 3 |
| Text Processing | NLTK, re |
| Feature Extraction | scikit-learn (TF-IDF, CountVectorizer) |
| Classical ML | scikit-learn (Naïve Bayes, Random Forest, SVM) |
| Deep Learning / NLP | TensorFlow, Hugging Face Transformers, BERT |
| Topic Modelling | Gensim (LDA) |
| Evaluation | scikit-learn metrics, seqeval |
| Environment | Google Colab |

---

## Key Findings

- **BERT fine-tuning significantly outperformed** all Bag-of-Words classifiers, demonstrating the advantage of contextual word embeddings over static feature representations
- Among classical models, **SVM** consistently delivered the strongest performance on text classification tasks
- **LDA topic modelling** uncovered coherent thematic clusters within the corpus, with additional analysis confirming topic stability and interpretability
- Preprocessing quality (particularly lemmatisation vs stemming) had a measurable impact on downstream classifier performance

---

## How to Run

1. Clone the repository
2. Open `notebooks/IDTA_Text_Mining_Assignment.ipynb` in Google Colab
3. Ensure GPU runtime is enabled (recommended for BERT fine-tuning)
4. Upload/connect the dataset
5. Run all cells sequentially

>  **Note:** BERT fine-tuning requires a GPU runtime. In Google Colab, go to `Runtime → Change runtime type → GPU`.

---

## Author

**William C** | [@chijokow](https://github.com/chijokow)  
Data Analyst | Python · SQL · Power BI

---
