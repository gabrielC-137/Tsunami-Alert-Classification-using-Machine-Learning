# Tsunami Alert Classification using Machine Learning

## 1. Introduction  
Understanding and responding effectively to seismic events is critical for minimizing the impact of natural disasters. While official tsunami warning systems rely on complex geophysical models, there is growing interest in exploring how data-driven approaches can complement these systems.

This project develops a machine learning classification framework to support tsunami alert decision-making using historical seismic event data. The objective is not to predict earthquakes or tsunamis themselves, but to classify whether a recorded seismic event is likely to trigger a tsunami warning based on post-event characteristics.

---

## 2. Problem Statement  
The goal of this project is to build a classification model that predicts whether a seismic event will generate a tsunami alert based on observed event characteristics such as magnitude, depth, and intensity-related variables.

This problem is framed as a supervised binary classification task and can be used as a decision-support tool for emergency response systems.

---

## 3. Dataset  
The dataset used in this project was obtained from the EveryEarthquake API (via Kaggle) and contains global seismic event records.

### Key variables:
- Magnitude  
- Depth  
- Geographic coordinates  
- Community Determined Intensity (CDI)  
- Modified Mercalli Intensity (MMI)  
- Seismic Significance (SIG)  
- Tsunami indicator (target variable)  

### Preprocessing steps:
- Data cleaning and handling missing values  
- Feature selection based on relevance  
- Removal of inconsistent records  

---

## 4. Methodology  

### 4.1 Data Preparation  
- Cleaning and preprocessing of raw seismic data  
- Feature selection based on domain relevance and correlation  
- Train-test split for model validation  

### 4.2 Model Development  
The following classification algorithms were implemented and compared:

- Logistic Regression  
- Decision Tree Classifier  
- K-Nearest Neighbors (KNN)  
- Linear Discriminant Analysis (LDA)  
- Quadratic Discriminant Analysis (QDA)

<img width="701" height="556" alt="image" src="https://github.com/user-attachments/assets/7a9a82b2-20a4-40be-b052-0d5ea7306c81" />  

### 4.3 Model Evaluation  
Models were evaluated using a hold-out test set with the following metrics:

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- ROC-AUC

---

## 5. Results  
The Decision Tree Classifier achieved the best overall performance among all tested models.

### Model Performance - Accuracy

| Model                          | Train | Test | Gap |
|-------------------------------|-------|------|-----|
| Logistic Regression           | 0.96  | 0.96 | 0.00 |
| Decision Tree                 | 0.99  | 0.99 | 0.00 |
| K-Nearest Neighbors          | 1.00  | 0.97 | 0.03 |
| Linear Discriminant Analysis | 0.92  | 0.92 | 0.00 |
| Quadratic Discriminant Analysis | 0.77 | 0.71 | 0.05 |

### Model Performance - F1 Score

| Model                          | Train | Test | Gap |
|-------------------------------|-------|------|-----|
| Logistic Regression           | 0.97  | 0.96 | 0.00 |
| Decision Tree                 | 0.99  | 0.99 | 0.00 |
| K-Nearest Neighbors          | 1.00  | 0.98 | 0.02 |
| Linear Discriminant Analysis | 0.94  | 0.94 | 0.01 |
| Quadratic Discriminant Analysis | 0.85 | 0.80 | 0.05 |

### Key findings:
- Tree-based models captured nonlinear relationships effectively  
- Intensity-related variables were the most predictive features  
- Performance was consistent across multiple evaluation metrics  

### Most important features:
- Magnitude  
- Community Determined Intensity (CDI)  
- Modified Mercalli Intensity (MMI)  
- Seismic Significance (SIG)  

---

## 6. Discussion  
The results demonstrate that interpretable machine learning models can provide meaningful insights for seismic risk classification tasks.

Although this model is not intended to replace official tsunami warning systems, it highlights the potential of data-driven approaches to enhance situational awareness and support emergency decision-making processes.

### Limitations:
- Reliance on historical data only  
- Lack of real-time geophysical sensor integration  
- Simplified binary classification of a complex phenomenon  

## 7. Conclusion
This project demonstrates how machine learning techniques can be applied to seismic data to support tsunami alert classification. By leveraging interpretable models and key intensity-based features, it is possible to build systems that assist in improving decision-making in disaster risk scenarios.
