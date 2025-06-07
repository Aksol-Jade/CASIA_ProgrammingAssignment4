---

# Support Vector Machine for Binary Tumor Classification

---

## Project Overview

This notebook demonstrates the application of Support Vector Machines (SVM) to a binary classification problem involving tumor status prediction. The workflow involves feature preprocessing, hyperparameter tuning, and model evaluation using a breast tumor dataset with 30 numerical features.

---

## Objectives

* Preprocess and scale high-dimensional data
* Train a Support Vector Machine classifier with default settings
* Perform hyperparameter tuning to optimize model performance
* Evaluate classification metrics and analyze feature importance

---

## Methodology

### 1. Preprocessing

* The feature set was standardized using `StandardScaler` to improve SVM efficiency.
* Class distributions were maintained during the train-test split using `stratify=y`.
* No missing values were present, so no imputation was required.

### 2. Model Training

* Trained initial model using `sklearn.svm.SVC` with default parameters.
* Performed hyperparameter tuning with `GridSearchCV` to explore:

  * Regularization parameter (`C`)
  * Kernel type (`linear`, `rbf`, `poly`)
  * Kernel coefficient (`gamma`)

### 3. Evaluation Metrics

* Computed training and testing accuracy
* Generated a confusion matrix
* Calculated:

  * Precision
  * Recall
  * F1-score
  * False Alarm Rate

### 4. Feature Selection

* Used `SelectFromModel` to identify the most informative features.

---

## Key Learnings

* Standardization is essential for distance-based models like SVM to ensure fair feature contributions.
* The best performance was achieved using the RBF kernel with `C=10`.
* SVM showed strong classification performance on both training and test sets.
* Proper hyperparameter tuning significantly improved model generalization.

---

## Tools and Libraries

* **Python**
* **Scikit-learn** (SVC, GridSearchCV, StandardScaler, SelectFromModel)
* **Pandas**, **NumPy** for data handling
* **Matplotlib**, **Seaborn** for visual analysis

---

## Conclusion

Support Vector Machines provide a robust approach to binary classification tasks when paired with proper preprocessing and tuning. The resulting model was both accurate and interpretable, making it suitable for high-dimensional diagnostic problems.

---
