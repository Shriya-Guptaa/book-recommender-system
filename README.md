# Book Recommendation System

## Overview

This project implements an **Item-Based Collaborative Filtering** book recommendation system using **K-Nearest Neighbors (KNN)**.
Books are recommended based on similarity in user rating patterns rather than content information.

---

## Dataset

The system uses the **Book-Crossing Dataset**:

* `BX-Books.csv` – Book metadata
* `BX-Users.csv` – User information
* `BX-Book-Ratings.csv` – User ratings

---

## Approach

* **Filtering Type**: Item-Based Collaborative Filtering
* **Method**: Memory-based KNN
* **Similarity Basis**: User–book rating matrix

---

## Data Preprocessing

* Keep users who rated **more than 200 books**
* Keep books with **at least 50 ratings**
* Remove duplicate user–book ratings
* Create a pivot table of **books × users**
* Fill missing ratings with 0

---

## Model

* Algorithm: `NearestNeighbors` (brute-force)
* Input: Sparse matrix of book rating vectors
* Output: Top-N similar books for a given book

---

## Usage

```python
book_recommend("Bag of Bones")
```

Returns books most similar to the given title based on user ratings.

---

## Key Libraries

* NumPy
* Pandas
* Scikit-learn
* SciPy

---

## Summary

This recommender system suggests books by analyzing collective user behavior, making it a classic example of **item-based collaborative filtering**.

---
