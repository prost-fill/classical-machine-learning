# Classical Machine Learning: From Fundamentals to Ensembles

A collection of practical machine learning experiments covering the core stages of a classical ML workflow: data preprocessing, classification, regression, clustering, model validation, hyperparameter tuning, regularization, model evaluation, ensemble learning, and pipelines.

The repository combines introductory and advanced machine learning exercises into a single structured project and demonstrates how different algorithms and validation strategies can be applied and compared on practical datasets.

## Project Overview

The project progresses from fundamental supervised and unsupervised learning methods to more advanced model-selection and ensemble techniques.

The main topics include:

- Binary and multiclass classification
- Regression
- Clustering
- Feature preprocessing and scaling
- One-hot encoding
- Train/test splitting
- Cross-validation
- Regularization
- Hyperparameter optimization
- Model evaluation with multiple metrics
- Ensemble learning
- Reusable Scikit-learn pipelines

## Machine Learning Workflow

```text
Raw data
   ↓
Preprocessing & Feature Engineering
   ↓
Encoding / Scaling
   ↓
Train / Test Split
   ↓
Model Training
   ↓
Cross-Validation
   ↓
Hyperparameter Tuning
   ↓
Model Evaluation
   ↓
Ensemble Methods / Pipelines
```

## What This Project Demonstrates

### Classification

The notebooks explore several classification algorithms:

- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest
- One-vs-Rest multiclass classification

The experiments cover binary and multiclass problems and compare different models under a common evaluation workflow.

### Regression

Regression experiments include:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- K-Fold validation
- Mean Squared Error
- R² score

### Clustering

The unsupervised learning section explores:

- K-Means
- DBSCAN
- Agglomerative Clustering
- Hierarchical clustering
- Dendrogram visualization
- Silhouette Score

### Model Validation

The project demonstrates:

- Train/test split
- Cross-validation
- Stratified validation
- K-Fold validation
- Comparison of training and validation performance

These techniques are used to estimate model generalization and identify potential overfitting.

### Hyperparameter Tuning

`GridSearchCV` is used to search for better model configurations.

Examples of tuned parameters include:

- SVM: `C`, `gamma`, `kernel`, `class_weight`
- Decision Tree: `max_depth`, `criterion`, `class_weight`
- Random Forest: `n_estimators`, `max_depth`, `criterion`, `class_weight`

### Model Evaluation

Models are evaluated using several metrics depending on the task:

- Accuracy
- Precision
- Recall
- ROC AUC
- Mean Squared Error
- R²
- Silhouette Score

Using multiple metrics provides a more complete view of model performance than relying on accuracy alone.

### Ensemble Learning

Advanced notebooks explore several ensemble approaches:

- Voting
- Bagging
- Stacking

The experiments investigate how combining multiple estimators can affect predictive performance.

### ML Pipelines

The final part of the project uses Scikit-learn `Pipeline` and custom transformers based on:

- `BaseEstimator`
- `TransformerMixin`

This allows preprocessing and model training steps to be combined into a reusable ML workflow and integrated with hyperparameter search.

## Repository Structure

```text
classical-machine-learning/
├── datasets/
│   ├── checker_regression.csv
│   ├── checker_submits.csv
│   ├── checker_timestamp.csv
│   ├── day-of-week-not-scaled.csv
│   ├── dayofweek.csv
│   └── regression.csv
│
├── notebooks/
│   ├── fundamentals/
│   │   ├── 00_binary_classifier_logreg.ipynb
│   │   ├── 01_binary_classifier_svm_tree.ipynb
│   │   ├── 02_multiclass_one-hot.ipynb
│   │   ├── 03_split_crossval.ipynb
│   │   ├── 04_regression.ipynb
│   │   └── 05_clustering_RU.ipynb
│   │
│   └── advanced/
│       ├── 00_regularization.ipynb
│       ├── 01_gridsearch.ipynb
│       ├── 02_metrics.ipynb
│       ├── 03_ensembles.ipynb
│       └── 04_pipelines(1).ipynb
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Notebook Guide

### Fundamentals

**00 — Binary Classification with Logistic Regression**  
Introduction to binary classification using Logistic Regression.

**01 — Model Comparison**  
Comparison of Logistic Regression, SVM, and Decision Tree classifiers.

**02 — Multiclass Classification & One-Hot Encoding**  
Categorical feature preprocessing and multiclass classification.

**03 — Train/Test Split & Cross-Validation**  
Model validation and comparison using holdout and cross-validation strategies.

**04 — Regression**  
Regression models and evaluation with regression metrics.

**05 — Clustering**  
Unsupervised learning with K-Means, DBSCAN, Agglomerative Clustering, and cluster-quality evaluation.

### Advanced

**00 — Regularization**  
Investigation of model complexity, regularization, and generalization.

**01 — Grid Search**  
Hyperparameter optimization using `GridSearchCV`.

**02 — Metrics**  
Model comparison using Accuracy, Precision, Recall, and ROC AUC.

**03 — Ensembles**  
Experiments with Voting, Bagging, and Stacking.

**04 — Pipelines**  
Reusable Scikit-learn pipelines and custom transformers.

## Installation

Clone the repository and create a virtual environment:

```bash
git clone <repository-url>
cd classical-machine-learning

python3 -m venv .venv
source .venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project

Start Jupyter:

```bash
jupyter notebook
```

Open the notebooks from either:

```text
notebooks/fundamentals/
```

or:

```text
notebooks/advanced/
```

The notebooks use relative paths to the CSV files stored in `datasets/`, so the repository structure should be preserved when running them.

## Tech Stack

`Python` · `Pandas` · `NumPy` · `Scikit-learn` · `SciPy` · `Matplotlib` · `Jupyter Notebook`

## Skills Demonstrated

`Classification` · `Regression` · `Clustering` · `Feature Preprocessing` · `Feature Scaling` · `One-Hot Encoding` · `Cross-Validation` · `Regularization` · `Hyperparameter Tuning` · `Model Evaluation` · `Ensemble Learning` · `ML Pipelines`

## Possible Improvements

- Add a unified experiment-tracking table comparing models and metrics.
- Move repeated preprocessing logic into reusable Python modules.
- Add automated tests for custom transformers.
- Add model explainability techniques such as feature importance analysis.
- Introduce a reproducible experiment configuration for random seeds and model parameters.
