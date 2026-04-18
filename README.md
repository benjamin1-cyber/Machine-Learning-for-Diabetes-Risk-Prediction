# Machine-Learning-for-Diabetes-Risk-Prediction
## 📌 Project Overview

This project develops and evaluates machine learning models to predict diabetes risk using **non-invasive, population-level health indicators**. The goal is to support **early detection and large-scale screening**, especially in settings where laboratory testing is limited.

The study leverages data from the **Behavioral Risk Factor Surveillance System (BRFSS)** and applies supervised machine learning techniques to classify individuals as diabetic or non-diabetic.


## 🎯 Objectives

* Predict diabetes risk using **routine health indicators**
* Compare performance of multiple machine learning models
* Prioritize **recall and ROC-AUC** for clinical relevance
* Support **clinical decision-making and public health screening**


## 📊 Dataset

* **Source:** BRFSS (CDC survey data)
* **Dataset Link:** [https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset](https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset)
* **Size:** ~253,000 observations

### Features Include:

* Demographics (age, sex, income, education)
* Behavioral factors (smoking, physical activity)
* Health indicators (BMI, blood pressure, cholesterol)

### Target Variable:

* `Diabetes_binary`

  * **1:** Diabetes (including prediabetes & gestational)
  * **0:** No diabetes

⚠️ Note: Data is self-reported → possible misclassification bias


## ⚙️ Methodology

### 🔹 Data Processing

* No major cleaning required (pre-encoded dataset)
* Stratified train-test split (80/20)
* Class imbalance handled using:

  * `class_weight='balanced'`
  * Stratified sampling

### 🔹 Models Implemented

* Logistic Regression
* Decision Tree
* Random Forest
* Gradient Boosting
* xGBoost

### 🔹 Validation

* Stratified K-Fold Cross-Validation
* Hyperparameter tuning using RandomizedSearchCV


## 📈 Results

### 🔑 Model Performance (Best Model)

* **Accuracy:** 75%
* **Precision (Diabetes):** 33%
* **Recall (Diabetes):** 73%
* **F1 Score:** 45%
* **ROC-AUC:** **0.819**

### 🔍 Confusion Matrix

* True Negatives: 32,988
* False Positives: 10,679
* False Negatives: 1,922
* True Positives: 5,147

## 🧠 Clinical Interpretation

* ✅ **High Recall (73%)**

  * Model detects most diabetes cases
  * Suitable for **early screening**

* ⚠️ **Low Precision (33%)**

  * Many false positives
  * Requires confirmatory testing

* ✅ **Low False Negatives**

  * Few missed cases → clinically important

### 🏥 Conclusion:

👉 Best suited as a **screening tool**, not a diagnostic system
👉 Should be followed by **clinical/lab confirmation**


## 💻 Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn



## 🚀 How to Run the Project

```bash
# Clone repository
git clone https://github.com
benjamin1-cyber/diabetes-risk-ml.git

# Navigate into project folder
cd diabetes-risk-ml

# Install dependencies
pip install -r requirements.txt

# Run notebook
 notebook AI_IN_HEALTHCARE_PROJECT_FINAL.ipynb
```



## 🎥 Project Presentation

👉 **(https://youtu.be/-baBxA64qQY)**

*(Replace this with your video link before submission)*



## 👥 Contributors

**Group 7**

* David Blemano

  * Project design, preprocessing, modeling, evaluation

* Benjamin Asomaning

  * Literature review, methodology support, report writing



## 📚 References

1. World Health Organization. Global Report on Diabetes, 2016
2. American Diabetes Association. Standards of Care, 2024
3. Breiman, L. Random Forests, 2001
4. Friedman, J. Gradient Boosting Machine, 2001
5. Yu et al., Diabetes Prediction using ML, 2020
6. Kavakiotis et al., ML in Diabetes Research, 2017



## ⚠️ Limitations

* Self-reported dataset → possible bias
* Class imbalance affects precision
* Not a substitute for clinical diagnosis



## 🔮 Future Work

* Improve precision via threshold tuning
* Incorporate additional clinical data
* Deploy as a web-based decision support tool



## ⭐ Acknowledgment

This project was developed as part of an **AI in Healthcare / Health Informatics course**, focusing on real-world clinical applications of machine learning.
