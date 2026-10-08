# Imbalanced Classification Evaluation

## Overview

This project demonstrates how to build and properly evaluate a binary classifier on imbalanced data.

The main focus is model evaluation rather than model complexity.

The notebook evaluates the classifier using:

- Confusion Matrix
- Precision
- Recall
- Accuracy
- Probability threshold analysis

## Objective

The objective is to demonstrate why accuracy can be misleading when working with imbalanced datasets and how selecting a classification threshold can change the precision-recall trade-off.

## Model

The project uses Logistic Regression with balanced class weights.

## Dataset

The Breast Cancer Wisconsin dataset provided by scikit-learn is used as the starting dataset. A controlled class imbalance is created by downsampling one class. No external dataset download is required.

## Evaluation Approach

The model produces probability scores for the positive class.

A default threshold of 0.50 is evaluated first.

The threshold is then selected deliberately using this requirement:

> Recall must be at least 90%, while maximizing precision among thresholds that satisfy this requirement.

This makes the threshold decision based on an explicit evaluation objective rather than choosing an arbitrary value.

## Why Accuracy Is Not Enough

Accuracy can be misleading on imbalanced datasets because a model can obtain high accuracy by mostly predicting the majority class.

For this reason, precision, recall, and the confusion matrix are given greater importance in this project.

## Repository Structure

```text
imbalanced-classifier/
├── notebook/
│   └── imbalanced_classification.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Requirements

- Python 3.10+
- NumPy
- pandas
- matplotlib
- scikit-learn
- Jupyter

## Installation

Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
cd imbalanced-classifier
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
notebook/imbalanced_classification.ipynb
```

Run all cells from top to bottom.

## Expected Outcome

The notebook demonstrates:

1. Imbalanced class distribution
2. Logistic Regression classification
3. Confusion matrix
4. Precision and recall
5. Why accuracy can be misleading
6. Probability-based threshold selection
7. Comparison between the default and selected thresholds

## Submission

Make the GitHub repository public and submit the repository URL.

Example:

```text
https://github.com/YOUR_USERNAME/imbalanced-classifier
```

## Conclusion

The project demonstrates that evaluating an imbalanced classifier requires more than looking at accuracy. Precision, recall, the confusion matrix, and a deliberately selected operating threshold provide a more meaningful assessment of model performance.
