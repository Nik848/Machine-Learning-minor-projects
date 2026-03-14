# 🎬 Netflix Movie & TV Show Recommendation System (KNN)

A **content-based recommendation system** built using **Python, TF-IDF vectorization, and K-Nearest Neighbors (KNN)** that suggests similar Netflix titles based on metadata such as genres, description, cast, and director.

This project demonstrates how machine learning techniques can be used to build a **movie recommendation engine similar to those used by streaming platforms.**

---

# 📌 Project Overview

Streaming platforms like Netflix recommend content based on similarities between titles.  
This project builds a **content-based recommender** that analyzes textual features of movies and TV shows to suggest similar content.

The system processes Netflix metadata, converts it into numerical vectors using **TF-IDF**, and finds similar titles using the **KNN algorithm with cosine similarity**.

---

# 🧠 Machine Learning Approach

This project uses **Content-Based Filtering**.

The recommendation process follows these steps:

Dataset  
↓  
Data Cleaning  
↓  
Exploratory Data Analysis (EDA)  
↓  
Text Preprocessing  
↓  
Feature Engineering  
↓  
TF-IDF Vectorization  
↓  
KNN Similarity Model  
↓  
Recommendation System  

---

# 📊 Dataset

Dataset used:

**Netflix Shows Dataset**  
Source: Kaggle  

Contains information about:

- Movies and TV shows available on Netflix
- Directors
- Cast members
- Genres
- Descriptions
- Country
- Release year

Dataset size:
~8800 titles
12 features


Key columns:

| Column | Description |
|------|-------------|
| title | Name of the show or movie |
| type | Movie or TV Show |
| director | Director name |
| cast | Actors |
| country | Country of production |
| listed_in | Genre |
| description | Summary of the content |

---

# 🔧 Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- NLTK  
- Matplotlib  
- Seaborn  
- KaggleHub  

---

# 📈 Exploratory Data Analysis

The following analyses were performed:

### Movies vs TV Shows Distribution
Understanding the proportion of movies and TV shows.

### Content Growth Over Time
Shows how Netflix content increased over the years.

### Top Producing Countries
Identifies countries producing the most content.

### Top Genres
Analyzes the most common genres on Netflix.

---

# ⚙️ Feature Engineering

To build the recommender, multiple textual features were combined:
genre
description
cast
director
country


Important improvements:

- Limited description length to reduce noise
- Removed generic Netflix labels
- Weighted genre and description for stronger relevance
- Applied text cleaning and stopword removal

---

# 🔢 Text Vectorization

Text features were converted into numerical vectors using:

**TF-IDF (Term Frequency – Inverse Document Frequency)**

Configuration:
max_features = 7000
ngram_range = (1,2)
stop_words = english


This allows the model to capture meaningful words and phrases.

---

# 🤖 KNN Recommendation Model

The recommendation system uses **K-Nearest Neighbors** with cosine similarity.

Metric: Cosine similarity
Algorithm: Brute force
Neighbors: 10


The model finds titles that are closest in the TF-IDF vector space.

---

# 🎯 Example Recommendation

Input:
recommend("Kota Factory")


Example output:

| Title | Genre | Country | Year | Similarity |
|------|------|------|------|------|
| Castle of Stars | Romantic TV Shows | Unknown | 2015 | 0.43 |
| Hot Date | TV Comedy | USA | 2018 | 0.42 |
| Refresh Man | Romantic Drama | Taiwan | 2016 | 0.41 |

---

# 🚀 How to Run the Project

### 1 Install Dependencies

Example output:

| Title | Genre | Country | Year | Similarity |
|------|------|------|------|------|
| Castle of Stars | Romantic TV Shows | Unknown | 2015 | 0.43 |
| Hot Date | TV Comedy | USA | 2018 | 0.42 |
| Refresh Man | Romantic Drama | Taiwan | 2016 | 0.41 |

---

# 🚀 How to Run the Project

### 1 Install Dependencies
pip install pandas numpy scikit-learn nltk matplotlib seaborn kagglehub


---

### 2 Run the Notebook or Script

Load dataset and train the recommender.

---

### 3 Get Recommendations

Example:

```python
recommend("Kota Factory")
