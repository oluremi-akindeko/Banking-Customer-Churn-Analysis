# 🏦 Bank Customer Churn Prediction Model

## Project Overview
This project focuses on building a predictive machine learning classification model to identify bank customers at high risk of attrition (churn). By analysing key demographic, financial, and product usage data, the goal is to provide the bank's strategy team with actionable insights to inform targeted retention campaigns and improve customer lifetime value.

The entire analysis, from data ingestion to model evaluation and feature importance, is contained within a single **Jupyter Notebook**.

## 🎯 Key Business Questions Addressed
* What is the baseline customer churn rate?
* Which customer segments (Geography, Gender, Age) present the highest flight risk?
* Which features (e.g., balance, activity status, credit score) are the most significant drivers of churn?
* Can we build a reliable model to predict future churn with a sufficient ROC AUC score?

---

## 📁 Repository Files

| File Name | Description | Purpose |
| :--- | :--- | :--- |
| **`README.md`** | This file. | Provides the project overview and instructions. |
| **`Bank Customer Churn Analysis.ipynb`** | **The main analysis document.** | Contains all code, outputs, visualisations, and markdown commentary. |
| **`Bank Customer Churn.csv`** | The raw dataset used for the project. | Allows immediate replication of the analysis. |
| **`.gitignore`** | Git configuration file. | Ensures temporary files (`venv/`, `.ipynb_checkpoints`) are not committed. |

---

## 🛠️ Technical Stack
The project utilised the core Python Data Science stack:

| Tool | Purpose |
| :--- | :--- |
| **Python 3** | Core programming language |
| **Pandas** | Data ingestion, manipulation, and numerical operations (built upon **NumPy** |
| **Matplotlib, Seaborn** | Exploratory Data Analysis (EDA) and visualisation (outputs visible in the notebook) |
| **Scikit-learn** (`sklearn`) | Model building, data splitting, scaling, and evaluation |
| **Jupyter Notebook** | Interactive environment for full workflow documentation |

---

## 💡 Key Model Insights & Results

### Model Performance (Logistic Regression)
* **ROC AUC Score:** **0.7748**
* **Recall (Churn Class):** **~18.67%** (Identified as the key area for future improvement using advanced models like XGBoost/Random Forest).

### Top 3 Churn Drivers (Feature Importance)
1.  **Inactive Member Status:** The single greatest predictor, making inactive customers the highest priority for re-engagement.
2.  **Geography (Germany):** A major regional risk factor, requiring localised attention.
3.  **Customer Age:** Older customers show a strong positive correlation with the likelihood of churn.

---

## 🚀 How to Run the Project
To fully reproduce the analysis, you need to run the `Bank Customer Churn Analysis.ipynb` notebook cell-by-cell.

1.  **Clone the Repository:**
    ```bash
    git clone (https://github.com/oluremi-akindeko/Banking-Customer-Churn-Analysis)
    ```
2.  **Install Dependencies:**
    ```bash
    pip install pandas scikit-learn matplotlib seaborn
    ```
3.  **Launch the Notebook:** Open the `Bank Customer Churn Analysis.ipynb` file in VS Code or Jupyter Lab/Notebook environment and run the cells sequentially.

---

**Author:** [Oluremi Akindeko/[LinkedIn Profile Link](https://www.linkedin.com/in/oluremi-akindeko-aca-898189127/)]
