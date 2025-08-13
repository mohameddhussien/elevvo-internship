# 📚 Elevvo NLP Internship Projects

<p>This repository contains all the tasks completed during my NLP internship at <strong>Elevvo</strong>,
covering multiple real-world datasets and applying diverse <strong>Natural Language Processing</strong> and <strong>Machine Learning</strong> techniques.</p>
---

## 📂 Repository Structure
```markdown
elevvo-internship/
├── amazon-reviews-sentiment-analysis/
├───├── \_resources.zip
│   └── \_resources/
│       └── models/
├── fake-news-detection/
├───├── \_resources.zip
│   └── \_resources/
│       └── models/
├── NER-news-article/
├───├── \_resources.zip
│   └── \_resources/
│       └── models/
├── news-multi-classification/
├───├── \ train.csv
│   └── \ test.csv
└─────────────────
```

- <strong>To access cached resources</strong>: unzip `_resources.zip` in the repository root.
- <strong>For full runs of certain projects</strong> (Fake News Detection & Amazon Reviews Sentiment Analysis), you must use the <strong>Kaggle API</strong> to download datasets.  
  - Obtain your API Key/Token from your Kaggle account.  
  - Use the Kaggle CLI to download datasets:  
    [Kaggle API Documentation](https://www.kaggle.com/docs/api)

---

## ⚙️ Project Details

### 1️⃣ Amazon Reviews Sentiment Analysis
- <strong>Dataset:</strong> [kritanjalijain/amazon-reviews](https://www.kaggle.com/datasets/kritanjalijain/amazon-reviews) <i>(Kaggle API required)</i>
- <strong>Stack:</strong>
  - `NLTK`, `WordNetLemmatizer`, `Tokenization`, `Spacy`
  - `TFIDF`, `Logistic Regression`, `Multinomial Naive Bayes`
- <strong>Preprocessing:</strong>
  - Punctuation removal
  - Repeated letter normalization
  - Collapsing elongated words
- <strong>Pipeline Steps:</strong>
  1. Load dataset via Kaggle API or cached resources.
  2. Clean and preprocess text.
  3. Vectorize using TFIDF.
  4. Train models (Logistic Regression, MultiNB).
  5. Evaluate performance.

---

### <strong>2️⃣ News Category Classification</strong>
- <strong>Dataset:</strong> [amananandrai/ag-news-classification-dataset](https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset)
- <strong>Stack:</strong>
  - `Data Visualization`, `WordClouds`
  - `LightGBM`, `TFIDF`
- <strong>Preprocessing:</strong>
  - Simple regex cleaning
- <strong>Pipeline Steps:</strong>
  1. Load dataset.
  2. Clean text with regex.
  3. Visualize word distributions.
  4. Vectorize with TFIDF.
  5. Train LightGBM classifier.
  6. Evaluate accuracy.

---

### <strong>3️⃣ Fake News Detection</strong>
- <strong>Dataset:</strong> [clmentbisaillon/fake-and-real-news-dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset) *(Kaggle API required)*
- <strong>Stack:</strong>
  - `TFIDF`, `LightGBMClassifier`, `XGBClassifier`, `RandomForestClassifier`, `Ridge Classifier`
- <strong>Preprocessing:</strong>
  - Simple regex cleaning
- <strong>Pipeline Steps:</strong>
  1. Load dataset via Kaggle API or cached resources.
  2. Clean text with regex.
  3. Vectorize using TFIDF.
  4. Train multiple ML models.
  5. Compare and evaluate results.

---

### <strong>4️⃣ Named Entity Recognition (NER) from News Articles</strong>
- <strong>Dataset:</strong> [alaakhaled/conll003-englishversion](https://www.kaggle.com/datasets/alaakhaled/conll003-englishversion)
- <strong>Stack:</strong>
  - `DistilBERT`, `GoogleBERT`, `GoogleElectraSmallDiscriminator`
  - `Positional Encoding`, `CrossEntropy Loss`
- <strong>Preprocessing:</strong>
  - Remove duplicate sentences by grouping via `sentence_id`
- <strong>Pipeline Steps:</strong>
  1. Load and preprocess dataset.
  2. Tokenize using Fast Tokenizer.
  3. Train transformer-based models for entity recognition.
  4. Evaluate precision, recall, and F1-score.

---

## 🚀 Getting Started

1. <strong>Clone the repository</strong>
   ```bash
   git clone https://github.com/mohameddhussien/elevvo-internship.git
   cd elevvo-internship

2. <strong>Install dependencies</strong>

   ```bash
   pip install -r requirements.txt
   ```

3. <strong>Download datasets using Kaggle API (for specific tasks)</strong>

   ```bash
   kaggle datasets download kritanjalijain/amazon-reviews
   kaggle datasets download clmentbisaillon/fake-and-real-news-dataset
   ```

5. <strong>Run the notebooks/scripts</strong> for each project.

---

## 📌 Notes
* Models are stored under `_resources/models` for easy reuse.
* For Kaggle API setup, refer to the [official documentation](https://www.kaggle.com/docs/api).
