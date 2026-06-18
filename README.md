# 🎬 IMDb Sentiment Analysis using NLP

## 📌 Project Overview

This project focuses on **Sentiment Analysis** of IMDb movie reviews using various Natural Language Processing (NLP) techniques and Machine Learning algorithms.

The objective is to classify movie reviews as **Positive** or **Negative** and compare the effectiveness of different text representation methods.

---

## 📊 Dataset

* Dataset: IMDb Movie Reviews Dataset
* Total Reviews: 50,000
* Classes:

  * Positive
  * Negative

The dataset is balanced, making it suitable for binary classification tasks.

---

## 🧹 Text Preprocessing

The following preprocessing techniques were applied to clean and normalize the text data:

### ✅ Lowercasing

Converted all reviews to lowercase to ensure consistency.

### ✅ HTML Tag Removal

Removed HTML tags present in reviews.

### ✅ URL Removal

Removed URLs and unwanted links.

### ✅ Punctuation & Special Character Removal

Removed punctuation marks and special symbols.

### ✅ Contraction Handling

Expanded contractions to preserve sentiment information.

**Example**

| Before   | After     |
| -------- | --------- |
| don't    | do not    |
| wouldn't | would not |
| can't    | cannot    |

### ✅ Stopword Removal

Removed common English stopwords while preserving important negation words:

* not
* no
* nor

This helps retain sentiment information.

### ✅ Tokenization

Split reviews into individual words (tokens).

### ✅ Text Normalization

Applied stemming/lemmatization experiments to reduce vocabulary size and normalize word forms.

---

## 🔤 Text Representation Techniques

Three different vectorization techniques were explored and compared.

### 1️⃣ Bag of Words (BoW)

Represents text using word occurrence frequencies.

### 2️⃣ TF-IDF

Assigns importance scores to words based on their frequency within a document and across the corpus.

### 3️⃣ Word2Vec

Generated dense word embeddings using Word2Vec and represented reviews using averaged word vectors.

---

## 🤖 Machine Learning Models

The following classification algorithms were trained and evaluated:

### Logistic Regression

A widely used linear classification algorithm for NLP tasks.

### Linear Support Vector Classifier (LinearSVC)

A linear SVM-based classifier optimized for high-dimensional text data.

---

## 📈 Model Performance

| Text Representation | Model               | Accuracy   |
| ------------------- | ------------------- | ---------- |
| TF-IDF              | Logistic Regression | 88.88%     |
| TF-IDF              | LinearSVC           | **89.36%** |
| Bag of Words        | Logistic Regression | 88.28%     |
| Bag of Words        | LinearSVC           | 86.75%     |
| Word2Vec            | Logistic Regression | 86.07%     |
| Word2Vec            | LinearSVC           | 86.03%     |

---

## 🏆 Best Performing Model

**TF-IDF + LinearSVC**

**Accuracy:** 89.36%

This combination achieved the highest performance among all evaluated approaches.

---

## 🔍 Key Observations

* TF-IDF outperformed both Bag of Words and Word2Vec representations.
* LinearSVC performed best when combined with TF-IDF features.
* Preserving negation words improved sentiment understanding.
* Average Word2Vec embeddings were less effective for this task compared to sparse TF-IDF features.
* Feature representation significantly impacts model performance in sentiment classification tasks.

---

## 🛠️ Libraries Used

* Pandas
* NumPy
* NLTK
* Scikit-learn
* Gensim
* Matplotlib
* Seaborn

---

## 🚀 Future Improvements

* TF-IDF with N-Grams
* Hyperparameter Tuning
* Deep Learning Models (LSTM/BiLSTM)
* Transformer Models (BERT)
* Model Deployment using Streamlit or FastAPI
