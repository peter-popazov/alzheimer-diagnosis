# Machine Learning Model for Alzheimer's Disease Diagnosis

## Overview

This project implements and evaluates machine learning models to aid in the preliminary diagnosis of Alzheimer's disease
using patient medical data. The objective is to develop accurate and interpretable models to identify patterns
associated with Alzheimer's diagnosis.

## Dataset

The dataset used for training and evaluation is sourced
from [Kaggle](https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset). It contains 2150 records of
patients across various
demographics and includes medical, cognitive, and lifestyle features

## Machine Learning Models

### Logistic Regression

**Purpose:** Binary classification (Alzheimer's diagnosis)

**Hyperparameters:** L2 regularization, balanced class weights, 1000 iterations

**Evaluation:** ~82% on training set and ~81% on validation set; f-1 score: 0-class - 0.84, 1-class - 0.77

### Deep Learning

**Purpose:** Improve accuracy by capturing complex patterns in data

**Architecture:** Three hidden layers (64, 32, 16 neurons) with ReLU activation, batch normalization, dropout for
regularization

**Evaluation:** ~94% on training set and ~85% on validation set; f-1 score: 0-class - 0.87, 1-class - 0.75 (more
training led to problems with overfitting)

### Random Forest Classifier

**Purpose:** Ensemble learning model to enhance prediction of just one decision tree

**Hyperparameters:** 100 decision trees, max depth = 10, class balancing

**Evaluation:** ~99% on training set and ~94% on validation set; f-1 score: 0-class - 0.95, 1-class - 0.91

## Conclusions

1. _“Which machine learning method has the highest accuracy in the context of medical predictions?”_

The most accurate was the random forest model with an accuracy of 98.78% on the training set and 93.72% on the test set,
indicating good generalization. The small gap indicates that the model works well and generalizes effectively due to the
effective use of several, namely 100 decision trees.

2. _“What was the impact of feature engineering on the prediction of neurological diseases?”_

Feature engineering had almost no impact on the prediction accuracy of neurological diseases, as the increase was only
about 1%. This can be explained by the fact that the initial medical indicators were already sufficiently informative.
In addition, neurological diseases have a complex nature that is difficult to express in simple features available in
the dataset. Another possible factor is the limitedness or noise (which is present in any medical record) in the data,
which makes the construction of additional features inefficient.

4. _“What is the correlation between model complexity and performance?”_

The correlation between model complexity and performance is not linear. In the early stages, increasing the complexity
of a model (for example, using more neurons or layers in neural networks) improved its performance because the model
better “understands” complex patterns in the data. However, a model that is too complex led to overfitting.

5. _“What are the most effective methods for dealing with class imbalance?”_

According to research, the most effective method for dealing with class imbalance was using an ensemble model – a
random forest.
