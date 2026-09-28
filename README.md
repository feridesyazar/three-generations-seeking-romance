# 💜 Three Generations Seeking Romance

## Overview

This project explores whether structured information from online dating profiles can be used to predict a user's **age** and **generation**.

Using anonymized profile data from **OKCupid**, the project addresses two supervised learning tasks:

1. **Regression** — Can profile information predict a user's age?
2. **Classification** — Can profile information predict whether a user belongs to the Millennial, Gen X, or Boomer generation?

Both tasks are implemented using simple feed-forward neural networks.

---

## Dataset

The dataset contains anonymized OKCupid profile information.

The `last_online` feature indicates that the profiles are from approximately **2011–2012**.

The generation groups are defined as:

- **Millennial:** 18–32
- **Gen X:** 33–47
- **Boomer:** 48–70

Selected profile features include:

- Height
- Income
- Sex
- Orientation
- Body type
- Diet
- Drinking habits
- Drug use
- Education
- Job
- Smoking habits
- Relationship status

The essay text fields are not used in this version of the project.

---

## Project Workflow

1. Load and explore the dataset
2. Inspect missing values and data types
3. Filter users between ages 18 and 70
4. Create generation labels
5. Analyze age and generation distributions
6. Prepare numerical and categorical features
7. Encode categorical variables
8. Standardize model inputs
9. Train a neural network for age regression
10. Evaluate regression performance
11. Train a neural network for generation classification
12. Evaluate classification performance
13. Visualize predictions and training results

---

## Part 1 — Age Prediction

A neural network regression model is used to predict a user's age from structured profile characteristics.

### Regression Results

| Metric | Result |
| --- | ---: |
| MAE | **5.9479** |
| RMSE | **7.9998** |
| R² Score | **0.1926** |

The model predicts age with an average absolute error of approximately **6 years**.

The R² score indicates that the selected structured profile features explain only a limited part of the variation in user age.

---

## Part 2 — Generation Classification

The second model predicts whether a user belongs to one of three generations:

- Millennial
- Gen X
- Boomer

### Classification Result

| Metric | Result |
| --- | ---: |
| Accuracy | **64.95%** |

The model performs best for the Millennial group, while prediction performance is lower for Gen X and especially Boomers.

The unequal distribution of generation groups in the dataset influences classification performance.

---

## Model Architecture

Both models use simple feed-forward neural networks with:

- Input layer
- Dense hidden layers
- ReLU activation
- Early Stopping

The regression model uses a single numerical output.

The classification model uses a **Softmax** output layer for the three generation classes.

---

## Visualizations

The notebook includes:

- Generation distribution
- Age distribution
- Correlation heatmap
- Actual vs Predicted Age
- Regression training and validation loss
- Generation confusion matrix
- Classification training and validation accuracy

---

## Technologies

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Scikit-learn` `TensorFlow` `Keras` `Jupyter Notebook`

---

## Conclusion

This project applies supervised deep learning to two prediction tasks using structured OKCupid profile information.

The regression results show that profile characteristics provide limited information for predicting a user's exact age.

The classification model achieved an overall accuracy of **64.95%**, with stronger performance for the more represented Millennial group.

Overall, the project presents a complete workflow for data preparation, feature engineering, deep learning regression, multi-class classification, evaluation, and visualization.
