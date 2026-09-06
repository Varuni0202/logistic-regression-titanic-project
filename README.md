#  Titanic Survival Prediction Using Machine Learning

##  Project Overview

This project predicts whether a passenger survived the Titanic disaster using machine learning classification algorithms.

The project uses passenger information such as **passenger class, gender, age, family information, fare, embarkation point, and cabin availability** to predict the target variable `Survived`.

Four different machine learning models are implemented and compared:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Gaussian Naive Bayes
* Decision Tree

The models are evaluated using accuracy, precision, recall, F1-score, and confusion matrices.

##  Objective

The main objective of this project is to:

* Analyze the Titanic passenger dataset.
* Clean and preprocess the data.
* Perform feature engineering.
* Convert categorical variables into numerical features.
* Train multiple classification algorithms.
* Compare their performance.
* Identify the best-performing model.

##  Dataset

The project uses the **Titanic Dataset** containing **891 passenger records and 12 original features**.

Important features include:

* `Survived` — Target variable
* `Pclass` — Passenger class
* `Gender` — Passenger gender
* `Age` — Passenger age
* `SibSp` — Number of siblings/spouses aboard
* `Parch` — Number of parents/children aboard
* `Fare` — Ticket fare
* `Embarked` — Port of embarkation
* `Cabin` — Cabin information

##  Exploratory Data Analysis

The project performs exploratory analysis to understand survival patterns.

For example, the dataset shows an overall survival rate of approximately **38.38%**, while approximately **61.62%** of passengers did not survive.

The analysis also examines survival based on gender, passenger class, and cabin availability.

##  Data Preprocessing

### Missing Values

The dataset contains missing values in:

* `Age`
* `Cabin`
* `Embarked`

The project fills missing age values using the mean and processes the `Embarked` feature.

### Feature Engineering

A new feature called `has_cabin` is created to indicate whether a passenger had cabin information available.

### Removing Irrelevant Features

The following columns are removed:

* `PassengerId`
* `Name`
* `Ticket`
* `Cabin`

The processed dataset therefore focuses on features considered useful for prediction.

##  Train-Test Split

The dataset is divided into:

* **80% Training Data**
* **20% Testing Data**

A `random_state` of 42 is used to make the split reproducible.

##  Machine Learning Models

### 1. Logistic Regression

Logistic Regression is used as the baseline classification model.

**Test Accuracy: 80.45%**

The model achieved approximately 0.80 precision, recall, and F1-score overall.

**Conclusion:** Logistic Regression performed well and provides a simple and interpretable baseline, but it was slightly outperformed by KNN and Decision Tree.

### 2. K-Nearest Neighbors

KNN was tested with different values of `k`, and the final model used **7 neighbors**.

**Test Accuracy: 82.12%**

**Overall F1-score: 0.82**

**Conclusion:** KNN achieved the highest test accuracy and overall F1-score, making it the best-performing model in this project.

### 3. Gaussian Naive Bayes

Gaussian Naive Bayes was implemented as another probabilistic classification approach.

**Test Accuracy: 75.42%**

**Overall F1-score: 0.75**

**Conclusion:** Gaussian Naive Bayes produced the lowest performance among the four tested models.

### 4. Decision Tree

A Decision Tree Classifier was trained on the processed dataset.

**Test Accuracy: 81.01%**

**Overall F1-score: 0.81**

**Conclusion:** Decision Tree performed strongly and was the second-best model based on test accuracy.

##  Model Comparison

| Rank | Model                |   Accuracy | F1-Score |
| ---: | -------------------- | ---------: | -------: |
|  1 | **KNN (K=7)**        | **82.12%** | **0.82** |
|  2 | Decision Tree        |     81.01% |     0.81 |
|  3 | Logistic Regression  |     80.45% |     0.80 |
|  4 | Gaussian Naive Bayes |     75.42% |     0.75 |

##  Best Model

### K-Nearest Neighbors (KNN)

KNN is the best-performing model in this project because it achieved the highest test accuracy of **82.12%** and an overall F1-score of **0.82**.

Its confusion matrix was:

```text
[[86 19]
 [13 61]]
```

This means the model correctly classified 86 passengers who did not survive and 61 passengers who survived.

##  Key Findings

* Gender has a strong relationship with survival in the dataset.
* Passenger class is an important factor in survival prediction.
* Feature engineering can provide useful information for classification.
* Different algorithms produce different prediction performances.
* KNN performed best among the four models tested.

##  Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook / Google Colab

##  Machine Learning Concepts Used

* Exploratory Data Analysis
* Data Cleaning
* Missing Value Handling
* Feature Engineering
* Categorical Encoding
* Feature Scaling
* Train-Test Split
* Classification
* Logistic Regression
* KNN
* Naive Bayes
* Decision Trees
* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

##  Future Improvements

* Apply cross-validation to obtain more reliable model comparisons.
* Perform hyperparameter tuning for all models.
* Try Random Forest and Gradient Boosting models.
* Optimize feature selection.
* Build a prediction interface using Streamlit.
* Analyze ROC-AUC scores for additional model comparison.

##  Final Conclusion

This project demonstrates a complete machine learning classification workflow for predicting Titanic passenger survival. Four classification algorithms were trained and evaluated using the same test data. **KNN achieved the highest test accuracy of 82.12%, followed by Decision Tree at 81.01%, Logistic Regression at 80.45%, and Gaussian Naive Bayes at 75.42%. Therefore, KNN is the best-performing model in the current experiment.**

##  Author

**Attrija Sharma**
