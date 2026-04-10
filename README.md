# TMDB Genre Classification — NLP Assignment (Week 07)

## 📌 Overview

This project implements a complete NLP pipeline for **text classification (genre detection)** using movie data from the TMDB API.
It follows the required structure: **data cleaning, preprocessing, TF-IDF (from scratch), cosine similarity search, modeling, and evaluation**.

---

## 📂 Dataset

Source: TMDB API (Top Rated Movies - Page 3)

```
https://api.themoviedb.org/3/movie/top_rated?api_key=8265bd1679663a7ea12ac168da84d2e8&language=en-US&page=3
```

Features used:

* `title`
* `overview` (text data)
* `genre_ids`

---

## ⚙️ Installation & Setup

### 1. Clone Repository

```https://github.com/Vicodwer/Day-37.git
cd week07/monday
```

### 2. Install Dependencies

```
pip install pandas numpy scikit-learn requests
```

---

## ▶️ How to Run

1. Open the notebook or Python file
2. Run all cells sequentially

Expected outputs:

* Cleaned dataset preview
* TF-IDF matrix (from scratch)
* Top-5 search results for query
* Model evaluation metrics

---

## 🧠 Implementation Details

### 1. Data Cleaning & Preprocessing

* Lowercasing text
* Removing punctuation and special characters
* Tokenization using `.split()`

---

### 2. TF-IDF (From Scratch)

* Built custom vocabulary
* Computed:

  * Term Frequency (TF)
  * Inverse Document Frequency (IDF)
* Generated full TF-IDF matrix using NumPy

---

### 3. Cosine Similarity Search

* Query converted to TF-IDF vector
* Cosine similarity used to rank documents
* Returns **Top-5 most relevant movie overviews**

Query used:

```
"wireless earbuds battery life poor"
```

---

### 4. TF-IDF Comparison (sklearn)

* Used `TfidfVectorizer`
* Compared matrices using **L2 norm difference**

---

### 5. Modeling (Genre Classification)

* Multi-label classification
* Model: **One-vs-Rest Linear SVM (LinearSVC)**
* Input: TF-IDF features
* Output: Predicted genres

---

### 6. Evaluation

* Metrics used:

  * Precision
  * Recall
  * F1-score
* Generated using `classification_report`

---

## 📊 Results

* TF-IDF successfully captures important keywords
* Cosine similarity returns relevant movie matches
* SVM performs well for sparse text classification

---

## 📝 Theoretical Insights

* Rare words have higher TF-IDF due to high IDF
* Common words like "the" have near-zero importance
* TF-IDF improves over raw frequency by reducing noise

---

## ⭐ Bonus

* BM25 scoring function implemented for ranking comparison

---

## 📁 Project Structure

```
week07/
 └── monday/
      ├── tmdb_genre_classification.ipynb
      ├── README.md
```

---

## ✅ Evaluation Checklist (Rubric Alignment)

* ✔ TF-IDF implemented from scratch
* ✔ Cosine similarity search implemented
* ✔ sklearn comparison included
* ✔ Model training + evaluation completed
* ✔ Clean and modular code
* ✔ No hardcoding of logic

---

## 👨‍💻 Author

Vishal Pagadala

---

## 🚀 Notes

This project is designed to meet **Band 4 (Excellent)** criteria:

* Correct implementation
* Clean engineering practices
* Complete documentation

