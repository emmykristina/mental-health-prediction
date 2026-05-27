# Mental Health Prediction – Deep Learning ANN Project

## Overview

Mental Health Prediction is a deep learning project focused on predicting depression risk among students using an Artificial Neural Network (ANN).

The project is based on student lifestyle, academic and mental health related factors such as academic pressure, sleep duration, financial stress, study satisfaction and suicidal thoughts.

The goal of the project is to investigate whether deep learning can identify meaningful patterns connected to depression risk and classify whether a student is likely to experience depression.

This project was created as part of our Deep Learning course, with focus on:

* Exploratory Data Analysis (EDA)
* Deep Learning
* Artificial Neural Networks (ANN)
* Binary Classification
* Data Preprocessing
* Feature Engineering
* Model Evaluation
* Overfitting Analysis
* Regularization Techniques
* Grid Search Optimization
* Data Storytelling and Business Value

---

## Team

This project was developed by:

* Emmy
* Mahtab
* Spirit

---

## Project Story

Mental health issues among students are increasing globally, and many students experience high levels of stress, academic pressure and sleep-related problems.

Universities and student wellbeing teams often struggle to identify students at risk early enough.

In this project, we use deep learning and Artificial Neural Networks (ANN) to analyze patterns connected to depression risk among students.

The model acts as a support tool that analyzes multiple student-related factors and predicts whether a student may belong to the depression risk group.

The model is not intended to diagnose depression, but rather to support early insight and risk detection.

---

## Dataset

The project uses the:

```text
Student Depression Dataset
```

The dataset contains:

* 27,901 rows
* 18 original columns
* Binary target variable: Depression

### Target Variable

| Value | Meaning       |
| ----- | ------------- |
| 0     | No Depression |
| 1     | Depression    |

### Class Distribution

| Class         | Percentage |
| ------------- | ---------- |
| No Depression | ~41.5%     |
| Depression    | ~58.5%     |

The dataset was not extremely imbalanced, but multiple evaluation metrics were still used to achieve a more complete understanding of model performance.

---

## Features

Examples of variables included in the dataset:

* Age
* Gender
* Academic Pressure
* Work Pressure
* CGPA
* Study Satisfaction
* Job Satisfaction
* Work/Study Hours
* Financial Stress
* Sleep Duration
* Dietary Habits
* Degree
* Suicidal Thoughts
* Family History of Mental Illness

After preprocessing and one-hot encoding, the final dataset contained:

```text
111 input features
```

---

## Deep Learning Workflow

The project follows a complete deep learning workflow:

1. Load and inspect the dataset
2. Perform Exploratory Data Analysis (EDA)
3. Analyze class distribution
4. Investigate relationships between variables
5. Handle missing values
6. Perform preprocessing and one-hot encoding
7. Scale numerical features
8. Split data into training and test sets
9. Build baseline ANN model
10. Evaluate model performance
11. Analyze overfitting
12. Improve model using:

    * Dropout
    * L2 Regularization
    * EarlyStopping
13. Perform Grid Search optimization
14. Compare model performance
15. Summarize findings as a data story

---

## ANN Architecture

The final ANN architecture included:

* Input layer: 111 features
* Dense layer (64 neurons + ReLU)
* Dropout
* Dense layer (32 neurons + ReLU)
* Dropout
* Output layer (1 sigmoid neuron)

The model was trained for binary classification:

```text
Depression / No Depression
```

---

## EDA Insights

The Exploratory Data Analysis revealed several meaningful patterns:

* Less sleep was associated with higher depression rates
* Higher academic pressure showed increased depression risk
* Higher financial stress showed increased depression risk

### Correlation Analysis

Strongest positive correlations:

* Academic Pressure
* Financial Stress
* Work/Study Hours

Negative correlation:

* Age

Correlation analysis showed relationships between variables, but not causation.

---

## Baseline ANN Results

| Metric   | Result |
| -------- | ------ |
| Accuracy | 0.832  |
| Recall   | 0.864  |
| ROC-AUC  | 0.907  |

The baseline ANN model showed signs of overfitting:

* Training loss decreased
* Validation loss increased
* Training accuracy increased
* Validation accuracy decreased

---

## Improved ANN Results

To improve model stability and reduce overfitting, the following regularization techniques were applied:

* Dropout
* L2 Regularization
* EarlyStopping

### Improved Model Performance

| Metric   | Result |
| -------- | ------ |
| Accuracy | 0.844  |
| Recall   | 0.875  |
| F1-score | 0.868  |
| ROC-AUC  | 0.917  |

The improved model showed:

* More stable learning
* Reduced overfitting
* Better generalization on unseen data
* Fewer false negatives

---

## Grid Search Optimization

Several ANN configurations were tested using Grid Search.

### Best Model: Grid Search Model 6

| Metric    | Result |
| --------- | ------ |
| Accuracy  | 0.845  |
| Precision | 0.856  |
| Recall    | 0.883  |
| F1-score  | 0.870  |
| ROC-AUC   | 0.918  |

All tested models performed similarly, but Model 6 achieved the highest F1-score and was selected as the final balanced model.

---

## Business Value

This type of deep learning model could potentially support universities and student wellbeing services by:

* Identifying mental health risk patterns
* Supporting preventive mental health work
* Prioritizing student support resources
* Understanding stress and sleep-related factors
* Supporting early intervention strategies

The model should always be used ethically and as a support tool — not as a replacement for healthcare professionals.

---

## Key Conclusions

* EDA revealed meaningful mental health risk patterns
* ANN performed well for binary classification
* Proper preprocessing and handling of missing values were critical
* Regularization techniques reduced overfitting
* Grid Search slightly improved final performance
* The final ANN model achieved strong and balanced results

This project demonstrates how deep learning can support mental health analytics and early risk detection in educational environments.

---

## Project Structure

```text
mental-health-prediction/
│
├── data/
│   └── Student Depression Dataset.csv
│
├── notebooks/
│   ├── emmy/
│   ├── mahtab/
│   └── spirit/
│
├── requirements.txt
├── README.md
└── .gitignore
```
