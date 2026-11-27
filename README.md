
# Mushroom Classification Using Machine Learning

## 1. Problem Statement

The aim of this project is to classify mushrooms as edible or poisonous
using their physical characteristics. Five machine learning classification
models are trained and evaluated to compare their performance.

## 2. Dataset Description

The Mushroom dataset is obtained from the UCI Machine Learning Repository.

Dataset source:
https://archive.ics.uci.edu/ml/machine-learning-databases/mushroom/agaricus-lepiota.data

The dataset contains 8124 instances and 22 input features.
The target variable is class.

Target classes:
- e: Edible
- p: Poisonous

All input features are categorical. Missing values represented by ?
were handled during preprocessing.

Class distribution:
- Edible: 4208 samples (51.77%)
- Poisonous: 3916 samples (48.23%)

The classes are fairly balanced.

## 3. GitHub Repository

Repository link: To be added after creating the GitHub repository.

## 4. Data Preprocessing

- Missing values represented by ? were converted to missing values.
- Missing categorical values were replaced using the most frequent value.
- Categorical features were converted using One-Hot Encoding.
- The dataset was split into 80% training and 20% testing data.
- Stratified splitting maintained the class distribution.
- Random state 42 was used for reproducibility.
- Preprocessing was fitted only on training data to avoid data leakage.

## 5. Machine Learning Models

1. Logistic Regression
2. Decision Tree
3. K-Nearest Neighbors (KNN)
4. Multinomial Naive Bayes
5. Random Forest

## 6. Model Evaluation

The models were evaluated using Accuracy, AUC, Precision, Recall,
F1-score and Matthews Correlation Coefficient (MCC).

The poisonous class (p) was considered the positive class for
Precision, Recall and F1-score.

### Model Comparison Results

| Model | Accuracy | AUC | Precision | Recall | F1-score | MCC |
|---|---:|---:|---:|---:|---:|---:|
| Logistic Regression | 0.9988 | 1.0000 | 1.0000 | 0.9974 | 0.9987 | 0.9975 |
| Decision Tree | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| KNN | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| Multinomial Naive Bayes | 0.9471 | 0.9974 | 0.9888 | 0.9004 | 0.9425 | 0.8970 |
| Random Forest | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |

## 7. Performance Visualization

A grouped bar chart was created to compare all five models across
the six evaluation metrics.

## 8. Observations

Decision Tree, KNN and Random Forest achieved perfect scores across
all six metrics on the test dataset.

Logistic Regression also performed very well, with an accuracy of 99.88%.

Multinomial Naive Bayes had comparatively lower performance, especially
in recall. Its recall of 0.9004 indicates that some actual poisonous
mushrooms were missed by the model.

The results are based on one train-test split. Perfect test scores do
not guarantee the same performance on all unseen data.

## 9. Project Files

- test_data.csv: Test dataset used for evaluation.
- model_results.csv: Evaluation results of all five models.
- requirements.txt: Required Python libraries.
- model/: Saved trained model pipelines.
- README.md: Project description and results.

## 10. How to Run

Install the required libraries using:

pip install -r requirements.txt

Open the Jupyter Notebook and run the cells in order.
The saved model pipelines can be loaded using the joblib library.
