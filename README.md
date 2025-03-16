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

| Model                      | Accuracy | AUC   | Precision Class 0  | Recall Class 0 | Precision Class 1 | Recall Class 1  |
|----------------------------|----------|-------|--------------------|----------------|--------------------|----------------|
| Logistic Regression        | 0.8142   | 0.9025| 0.93               | 0.78           | 0.63               | 0.89           |
| Deep Learning              | 0.8019   | 0.8857| 0.85               | 0.84           | 0.71               | 0.74           |
| Random Forest              | 0.9412   | 0.9509| 0.95               | 0.96           | 0.93               | 0.90           |
| Ensemble Learning (Stacking)| 0.9443  | 0.9315| 0.97               | 0.95           | 0.91               | 0.94           |


## Conclusions

1. _“Which machine learning method has the highest accuracy in the context of medical predictions?”_

The ensemble learning model showed the highest accuracy with an accuracy of 94.43%, but the random forest model with an accuracy of 98.78% on the current set is not far behind. The main reason for the small increase in accuracy in the ensemble learning model is the “weak” logistic regression and deep learning models.

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
