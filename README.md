# Predictive Maintenance for Industrial Tightening Tools 🛠️📊

This project demonstrates the application of **Machine Learning** to predict unplanned failures in industrial tightening tools. By transitioning from reactive to proactive maintenance, industries can reduce operational costs and increase assembly line reliability.

## 📌 Problem Overview
Unplanned failures in industrial tools lead to:
* **Critical production downtime**.
* **High corrective maintenance costs**.
* **Compromised final product quality**.

The goal of this research was to determine if sensor data (Torque, Tool Wear, Temperature) could be used to predict these failures before they occur.

## 🧪 Methodology
The project followed an **experimental and quantitative research approach**:

* **Exploratory Data Analysis (EDA):** Investigation of variables and correlations using the "AI4I 2020 Predictive Maintenance Dataset".
* **Feature Engineering:** Creation of new predictive variables: `Power` (Torque × Rotational Speed) and `Temp_Diff` (Process vs. Air Temperature).
* **Data Splitting:** Segmentation into Training (80%) and Test (20%) sets using `train_test_split`.
* **Imbalance Handling (SMOTE):** Application of Synthetic Minority Over-sampling Technique to correct the low occurrence of failure records in the training set.
* **Model Benchmarking:** Comparative analysis of multiple algorithms to find the most efficient solution for an industrial environment.

## 📈 Benchmarking Results
After testing several classification models, **XGBoost** proved to be the most balanced solution for real-world deployment, effectively reducing false alarms while maintaining high failure detection.

| Model | Precision (Fail) | Recall (Fail) | F1-Score (Fail) | Accuracy |
| :--- | :---: | :---: | :---: | :---: |
| **XGBoost** | **0.863** | **0.926** | **0.894** | **0.993** |
| Random Forest | 0.717 | 0.971 | 0.825 | 0.986 |
| Gradient Boosting | 0.541 | 0.971 | 0.695 | 0.971 |
| Logistic Regression | 0.421 | 0.941 | 0.582 | 0.954

### Key Insight: The Industry Perspective
While Random Forest achieved a slightly higher Recall (0.971), **XGBoost was selected as the final model**. In an industrial setting, a 0.863 Precision means significantly fewer false alarms. Reducing false alarms prevents unnecessary line stoppages and optimizes maintenance resources, offering a better Return on Investment (ROI).

## 💻 Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, XGBoost, Imbalanced-Learn (SMOTE), Seaborn, Matplotlib.
* **Environment:** Anaconda / Jupyter Notebook.

## 📂 Dataset Source
The data used in this project is the **AI4I 2020 Predictive Maintenance Dataset**.

* **Description:** A synthetic dataset that mirrors real-world industrial predictive maintenance data.
* **Size:** 10,000 data points with attributes like 'Torque', 'Tool_wear', and 'Machine_failure'.
* **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset) / [Kaggle](https://www.kaggle.com/datasets/stephanmatthews/ai4i-2020-predictive-maintenance-dataset).

## 👤 About the Author
**Luis Eduardo Gonçalves da Silva**

* **Software Engineer** specializing in Industrial Data & Automation.
* **17+ years of experience** on the industrial shop floor.
* Focused on bridging the gap between industrial experience and advanced Data Science to solve manufacturing challenges.
* https://www.linkedin.com/in/luisedugdasilva/

