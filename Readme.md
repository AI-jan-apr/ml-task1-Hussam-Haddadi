# Breast Cancer — Binary Classification

## Project Overview

This project focuses on building and comparing multiple binary classification models to predict whether a breast tumor is:

* 0 — Malignant (Cancerous)
* 1 — Benign (Non-cancerous)

The goal of this task is to train machine learning models, evaluate their performance using different classification metrics, and compare the results to determine the best model.

Feature scaling was not used in this project, as required in the assignment instructions.

---

## Dataset

The dataset used is the Breast Cancer Wisconsin Dataset, available directly from scikit-learn.

Dataset characteristics:

* 569 samples
* 30 numerical features
* Binary target variable
* No missing values

Each feature represents measurements extracted from a digitized image of a breast mass, such as radius, texture, area, smoothness, concavity, and symmetry.

---

## Models Used

The following classification models were trained using default parameters:

1. Logistic Regression
2. Support Vector Machine (SVM)
3. K-Nearest Neighbors (KNN)

All models were trained on 80% of the data and tested on the remaining 20%, using:

* test_size = 0.2
* random_state = 42
* stratify = y

Stratification ensures that the class distribution remains consistent in both training and testing sets.

---

## Evaluation Metrics

Each model was evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

These metrics provide a complete view of model performance, especially in medical classification problems where different types of errors have different consequences.

---

## Results and Comparison

After training and evaluation, the performance metrics of all models were summarized in a comparison table.

The best model is determined based on overall performance, particularly the F1-score, which balances Precision and Recall.

---

## Medical Context Consideration

In medical diagnosis tasks, Recall is the most important metric.

Recall measures how many actual cancer cases were correctly identified. A low recall means the model misses malignant cases (False Negatives), which can be very dangerous in real-world medical scenarios.

Therefore, minimizing False Negatives is more critical than slightly improving overall accuracy.

---

## Project Structure

```
ML-TASK1-HUSSAM-HADDADI/
├── modeling.ipynb
└── README.md
```

* modeling.ipynb contains all model training, evaluation, and comparison.
* README.md provides a summary of the project and results.
