# Heart Disease Prediction System

---

## 1. Project Objective

The primary goal of this project is to design and implement a **machine learning–based classification system** capable of accurately predicting the risk of heart disease in patients. By systematically analyzing structured clinical and demographic health data, the system aims to function as a **decision-support tool** for healthcare professionals.

The model is intended to reduce dependency on manual diagnosis, minimize potential human error, and significantly accelerate **early-stage medical intervention**, which is critical for improving patient outcomes in cardiovascular diseases.

---

## 2. Dataset Used

The system is built using the **Heart Disease Dataset**, sourced from Kaggle. This dataset is a well-established benchmark widely used in medical machine learning research.

### Dataset Characteristics

- **Features:**  
  The dataset includes essential clinical parameters such as:
  - Age  
  - Gender  
  - Chest Pain Type (`cp`)  
  - Resting Blood Pressure (`trestbps`)  
  - Serum Cholesterol (`chol`)  
  - Fasting Blood Sugar  
  - Resting Electrocardiographic Results  
  - Maximum Heart Rate Achieved  

  These features are medically relevant and commonly used in real-world cardiovascular risk assessment.

- **Data Cleaning:**  
  A comprehensive audit of the dataset was conducted to identify missing or inconsistent values. The inspection confirmed a **high degree of data integrity**, with zero null or missing entries across all features.

- **Preprocessing:**  
  Numerical features were standardized using **StandardScaler** to normalize feature ranges. This preprocessing step ensures unit-independent learning, improves optimization stability, and enhances convergence behavior for distance-based and gradient-based models.

- **Class Balancing:**  
  To mitigate class imbalance and prevent biased predictions, the dataset was **upsampled**, resulting in a perfectly balanced distribution of **420 samples per target class**. This significantly improved model fairness and recall performance.

---

## 3. Models Tested

To identify the most robust and generalizable solution, six different classification algorithms were implemented, trained, and evaluated:

- **Logistic Regression**  
  Used as a baseline linear classifier for performance comparison.

- **Random Forest Classifier**  
  An ensemble-based bagging approach capable of modeling complex non-linear relationships.

- **Support Vector Classifier (SVC)**  
  Particularly effective for high-dimensional decision boundaries.

- **K-Nearest Neighbors (KNN)**  
  A distance-based classifier relying on neighborhood proximity.

- **Decision Tree Classifier**  
  A hierarchical and highly interpretable rule-based model.

- **Gaussian Naive Bayes**  
  A probabilistic classifier grounded in Bayes’ Theorem with feature independence assumptions.

---

## 4. Model Comparison & Evaluation Metrics

All models were evaluated using four primary performance metrics:

- Accuracy  
- F1-Score  
- Precision  
- Recall  

The comparative analysis highlighted clear differences in predictive strength and generalization ability.

| Model | Accuracy | F1-Score | Precision | Recall |
|------|---------|----------|-----------|--------|
| Random Forest | 98.81% | 0.988 | 0.988 | 0.988 |
| SVC | 96.43% | 0.964 | 0.965 | 0.964 |
| Logistic Regression | 95.24% | 0.952 | 0.952 | 0.952 |
| Decision Tree | 95.24% | 0.952 | 0.953 | 0.952 |
| Gaussian Naive Bayes | 92.86% | 0.929 | 0.929 | 0.929 |
| KNN | 92.26% | 0.923 | 0.926 | 0.923 |

---

## 5. Model Selected

The **Random Forest Classifier** was selected as the final production-ready model.

### Selection Justification

- **Performance:**  
  The model achieved the highest scores across all evaluation metrics.

- **AUC Score:**  
  An **Area Under the Curve (AUC) value of 1.00** indicates perfect class separability between diseased and healthy patients in the test dataset.

- **Robustness:**  
  As an ensemble learning method, Random Forest significantly reduces overfitting compared to a single Decision Tree while preserving the ability to capture **complex, non-linear patterns** inherent in medical data.

---

## 6. Key Findings and Results

### Feature Importance

Exploratory Data Analysis (EDA) and correlation heatmaps revealed that the most influential predictors of heart disease are:

- Chest Pain Type (`cp`)
- Number of Major Vessels (`ca`)
- Thalassemia (`thal`)

### Medical Safety Perspective

The model achieved a **Recall score of 98.8%**, which is critically important in healthcare applications. This high recall confirms that the system is highly sensitive and produces **very few false negatives**, minimizing the risk of failing to identify patients with heart disease.

### Inference Capability

Individual prediction tests on unseen data confirmed that the trained model can reliably classify new patient records with **high confidence and consistency**, demonstrating strong real-world applicability.

---

## 7. Conclusion

The Heart Disease Prediction System is a **clean, well-structured, and highly reliable machine learning solution** for medical classification tasks. Exploratory analysis confirms strong feature relevance, the trained model demonstrates excellent generalization, and the system is fully prepared for deployment in downstream clinical decision-support applications.
