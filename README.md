# 🫀 Sentiment Analysis on Cardiac Complications After COVID-19 & Vaccination (SAOC)

> An NLP-driven study analyzing public sentiment around cardiac complications linked to COVID-19 and vaccination, using rule-based and transformer-based models.

---

## 📌 Overview

The COVID-19 pandemic and subsequent vaccination rollout sparked widespread public discourse around cardiac side effects. This project mines and classifies sentiment from social media text using two distinct NLP approaches — **VADER** (rule-based) and **BERT** (deep learning transformer) — to understand how people perceive and discuss cardiac risks associated with COVID-19 and vaccines.

---

## 🎯 Objectives

- Collect and preprocess health-related social media text on cardiac complications post-COVID-19 and vaccination
- Apply and compare rule-based (VADER) vs. transformer-based (BERT) sentiment classification
- Visualize sentiment trends and public perception patterns
- Evaluate model performance and identify the most effective approach for medical NLP tasks

---

## 🗂️ Project Structure

```
SAOC/
│
├── SAOC.ipynb               # Main Jupyter Notebook (full pipeline)
├── README.md                # Project documentation
└── data/                    # Dataset (tweets/reddit posts)
```

---

## 🔬 Methodology

### 1. Data Collection & Preprocessing
- Collected text data from social media platforms (Twitter/Reddit) related to COVID-19 cardiac complications and vaccine side effects
- Cleaned raw text: removed URLs, special characters, mentions, and hashtags
- Applied tokenization, lowercasing, and stopword removal
- Prepared data for both VADER (raw text) and BERT (tokenized sequences)

### 2. Sentiment Analysis Models

#### 🔹 VADER (Valence Aware Dictionary and sEntiment Reasoner)
- Rule-based lexicon model; no training required
- Fast and lightweight, suitable as a baseline
- Outputs compound sentiment scores → classified as Positive / Negative / Neutral

#### 🔹 BERT (Bidirectional Encoder Representations from Transformers)
- Fine-tuned pre-trained `bert-base-uncased` on labeled sentiment data
- Captures contextual, bidirectional language understanding
- Significantly outperforms rule-based approaches for nuanced medical text

### 3. Model Comparison

| Model | Type          | Context Awareness | Accuracy | Strength              |
|-------|---------------|-------------------|----------|-----------------------|
| VADER | Rule-based    | No                | Baseline | Fast, simple          |
| BERT  | Deep Learning | Yes               | **97%**  | Accurate, contextual  |

---

## 📊 Results

- **BERT achieved 97% accuracy**, demonstrating strong performance in classifying sentiment in health-related social media text
- BERT significantly outperformed VADER in handling negations, sarcasm, and domain-specific medical language
- Sentiment distribution analysis revealed predominantly negative/concerned public discourse around cardiac side effects
- Word clouds and sentiment trend visualizations provided interpretable insights into key topics driving public concern

---

## 🛠️ Tech Stack

| Category         | Tools / Libraries                          |
|------------------|--------------------------------------------|
| Language         | Python 3                                   |
| NLP / ML         | Transformers (BERT), VADER, NLTK, Scikit-learn |
| Data Processing  | Pandas, NumPy                              |
| Visualization    | Matplotlib, Seaborn                        |
| Environment      | Google Colab (GPU: T4)                     |

---

## ⚙️ Setup & Usage

### Prerequisites
```bash
pip install transformers torch nltk vaderSentiment scikit-learn pandas numpy matplotlib seaborn
```

### Run the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/nehachinnam956/SAOC.git
   cd SAOC
   ```
2. Open `SAOC.ipynb` in Jupyter or Google Colab
3. Run all cells sequentially

---

## 📈 Key Findings

- BERT's contextual understanding makes it far more effective than VADER for medical/health discourse sentiment classification
- Public sentiment around cardiac complications skewed negative, reflecting concern and hesitancy
- Vaccination-related posts showed more polarized sentiment compared to general COVID-19 cardiac discussion

---

## 🙋‍♀️ Author

**Neha Chinnam**
- GitHub: [@nehachinnam956](https://github.com/nehachinnam956)

---

## 📄 License

This project is for academic and research purposes only.
