# Predictive Maintenance for Industrial Tightening Tools 🛠️📊

This project demonstrates the application of **Machine Learning** to predict unplanned failures in industrial tightening tools. By transitioning from reactive to proactive maintenance, industries can reduce operational costs and increase assembly line reliability.

## 📌 Problem Overview
Unplanned failures in industrial tools lead to:
**Critical production downtime**.
* **High corrective maintenance costs**.
* **Compromised final product quality**.

The goal of this research was to determine if sensor data (Torque, Tool Wear, Temperature) could be used to predict these failures before they occur.

## 🧪 Methodology
The project followed an **experimental and quantitative research approach**:

* **Exploratory Data Analysis (EDA):** Investigation of variables and correlations using the "AI4I 2020 Predictive Maintenance Dataset".
* **Feature Engineering:** Creation of new predictive variables: `Power` (Torque × Rotational Speed) and `Temp_Diff` (Process vs. Air Temperature).
* **Data Splitting:** Segmentation into Training (80%) and Test (20%) sets using `train_test_split`.
* **Imbalance Handling (SMOTE):** Application of Synthetic Minority Over-sampling Technique to correct the low occurrence of failure records in the training set.
* **Model Training:** Implementation of a **Random Forest Classifier**.
* **Evaluation:** Validation using unseen data from the test set.

## 📈 Key Results
The model achieved high effectiveness in identifying failures, answering the research question affirmatively:

* **Recall (Failure Class): 96%** — The model successfully identified 96% of all actual failures.
* **F1-Score (Failure Class): 0.84** — A robust balance between precision and recall for the minority class.
* **Conclusion:** It is highly viable to create robust predictive systems using machine learning for industrial environments.

## 💻 Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Imbalanced-Learn (SMOTE), Seaborn, Matplotlib.
* **Algorithm:** Random Forest.

## 👤 About the Author
**Luis Eduardo Gonçalves da Silva**

* **Software Engineer** with over 17 years of experience in different areas of the industrial sector.
* Focused on bridging the gap between industrial shop-floor expertise and advanced data analytics.
* https://www.linkedin.com/in/luisedugdasilva/

## 📂 Dataset Source
The data used in this project is the **AI4I 2020 Predictive Maintenance Dataset**.

* **Description:** A synthetic dataset that mirrors real-world industrial predictive maintenance data.
* **Size:** 10,000 data points with attributes like 'Torque', 'Tool_wear', and 'Machine_failure'.
* **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset) / [Kaggle](https://www.kaggle.com/datasets/stephanmatthews/ai4i-2020-predictive-maintenance-dataset).
