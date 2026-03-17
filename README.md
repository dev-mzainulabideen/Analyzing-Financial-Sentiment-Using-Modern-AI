# 📊 Analyzing Financial Sentiment Using Modern AI  
## Comparing Three Different Approaches  

**Author:** Muhammad Zain-ul-Abideen (20i-0821)  
**Section:** BSCS-A  
**Department:** Computer Science  
**University:** FAST National University of Computer and Emerging Sciences, Islamabad  
📧 i200821@nu.edu.pk  

---

## 📌 Overview  

This project explores how modern AI techniques can be used to analyze **financial sentiment** in text data. Three different approaches are implemented and compared to evaluate their effectiveness.

---

## 🚀 Key Results  

- FinBERT Accuracy: **97.2%**  
- Multi-Model Ensemble: **95.2%**  
- Retrieval-Based (RAG): **97.0%**  
- **Combined Model: 97.5% (Best Performance)**  

---

## 🧠 Methods  

### 1. FinBERT  
- Domain-specific transformer model  
- Trained on financial text  
- Based on BERT architecture  

---

### 2. Multi-Model Ensemble  
Includes:
- Twitter-RoBERTa  
- FinBERT-Tone  
- Updated RoBERTa  

**Techniques:**
- Weighted voting  
- Confidence-based refinement  
- Multi-stage correction  

---

### 3. Retrieval-Augmented Generation (RAG)  
- Uses FAISS for similarity search  
- MPNet embeddings for sentence representation  
- Predicts sentiment using similar examples  

---

### 🔥 Final Combined Model  
- FinBERT → 50% weight  
- Multi-model → 25%  
- RAG → 35%  
- Bonus weight when models agree  

---

## 📂 Dataset  

**FinancialPhraseBank Dataset**  

- Total Samples: 2,264  

| Sentiment | Count | Percentage |
|----------|------|-----------|
| Positive | 570  | 25.2% |
| Neutral  | 1391 | 61.4% |
| Negative | 303  | 13.4% |

---

## 🧹 Data Preprocessing  

- Lowercasing text  
- Removing URLs & emails  
- Tokenization  
- Stopword removal (keeping important words like *not*)  
- Cleaning special characters  

---

## 📊 Topic Modeling  

Using **Latent Dirichlet Allocation (LDA)**  

Top Topics:
- Financial Performance  
- Market Activity  
- Corporate Operations  
- Quarterly Reports  
- Financial Metrics  
- Strategic Moves  
- Industry Trends  

---

## 📈 Results  

### Overall Performance  

| Method | Accuracy | Precision | Recall | F1 |
|--------|--------|----------|--------|----|
| FinBERT | 97.2% | 97.3% | 97.2% | 97.2% |
| Multi-Model | 95.2% | 95.5% | 95.2% | 95.3% |
| RAG | 97.0% | 97.1% | 97.0% | 97.1% |
| **Combined** | **97.5%** | **97.6%** | **97.5%** | **97.5%** |

---

### Performance by Sentiment  

| Sentiment | Precision | Recall | F1 |
|----------|----------|--------|----|
| Negative | 96.2% | 93.4% | 94.8% |
| Neutral  | 98.2% | 99.1% | 98.6% |
| Positive | 96.8% | 94.7% | 95.7% |

---

## ⚠️ Error Analysis  

Common issues:
- Hidden sentiment in numerical comparisons  
- Context-dependent meanings  
- Mixed sentiment in one sentence  
- Financial jargon misinterpretation  

---

## ⏱️ Runtime  

| Method | With GPU | Without GPU |
|--------|--------|------------|
| FinBERT | 3.2 min | 12.1 min |
| Multi-Model | 8.7 min | 31.4 min |
| RAG | 6.3 min | 18.9 min |
| Combined | 1.1 min | 2.3 min |

---

## 🛠️ Tech Stack  

- Python  
- PyTorch  
- HuggingFace Transformers  
- FAISS  
- Sentence Transformers (MPNet)  
- Scikit-learn  
- LDA  

---

## 📦 Installation  

```bash
git clone https://github.com/your-username/financial-sentiment-ai.git
cd financial-sentiment-ai
pip install -r requirements.txt
