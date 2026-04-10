# Classifier Performance Across Dataset Difficulty

This project compares the performance of three supervised learning classifiers — Support Vector Machine (SVM), Random Forest, and K-Nearest Neighbors (KNN) — across binary classification datasets with different levels of difficulty.

## Overview

The goal of this project was to study how model performance changes as dataset complexity increases and as the amount of training data changes. I evaluated all three classifiers on three datasets representing easy, medium, and hard classification settings, using multiple train/test splits and cross-validation for hyperparameter tuning.

## Methods

- Models evaluated:
  - Support Vector Machine (RBF kernel)
  - Random Forest
  - K-Nearest Neighbors
- Datasets:
  - Banknote Authentication
  - Breast Cancer Wisconsin (Diagnostic)
  - MAGIC Gamma Telescope
- Train/test splits:
  - 20/80
  - 50/50
  - 80/20
- Hyperparameter selection:
  - 5-fold cross-validation
- Framework:
  - scikit-learn

## Key Findings

- All three models performed very well on the easiest dataset, where class separation was strong.
- SVM produced the best results on the medium-difficulty Breast Cancer dataset across all train/test splits.
- Random Forest was the most robust model on the hardest dataset, MAGIC, outperforming the other classifiers in every split.
- Increasing the amount of training data had the greatest effect on performance for the most difficult dataset.

## Results Snapshot

### 20/80 split
- SVM: 0.999 / 0.945 / 0.863
- Random Forest: 0.981 / 0.933 / 0.870
- KNN: 0.996 / 0.928 / 0.826

### 50/50 split
- SVM: 0.999 / 0.968 / 0.871
- Random Forest: 0.990 / 0.956 / 0.876
- KNN: 0.998 / 0.953 / 0.837

### 80/20 split
- SVM: 1.000 / 0.974 / 0.873
- Random Forest: 0.995 / 0.950 / 0.880
- KNN: 1.000 / 0.933 / 0.843

Values are listed in the order:
Banknote / Breast Cancer / MAGIC.

## Tools Used

- Python
- scikit-learn
- NumPy
- Pandas

## Files

- `classifier-performance-across-dataset-difficulty.pdf` — final report for the project

## Notes

This was an academic machine learning project completed at UC San Diego. I am sharing it here as part of my technical portfolio.
