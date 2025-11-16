# 🏦 Bank Customer Churn Prediction Model

## Project Overview
This project focuses on building a machine learning classification model to identify bank customers at high risk of attrition (churn). By analysing key demographic, financial, and product usage data, the goal is to provide the bank's strategy team with actionable insights to inform targeted retention campaigns and improve customer lifetime value.

## 🎯 Key Business Questions Addressed
* What is the baseline customer churn rate?
* Which customer segments (Geography, Gender, Age) present the highest flight risk?
* Which features (e.g., balance, activity status, credit score) are the most significant drivers of churn?
* Can we build a reliable model to predict future churn with a sufficient ROC AUC score?

---

## 🛠️ Technical Stack
The entire project was developed in a Python environment, utilising the core Data Science stack:

| Tool | Purpose |
| :--- | :--- |
| **Python 3** | Core programming language |
| **Pandas** | Data ingestion and numerical operations |
| **Matplotlib, Seaborn** | Exploratory Data Analysis (EDA) and data visualisation |
| **Scikit-learn** (`sklearn`) | Model building, data splitting, scaling, and evaluation |
| **VS Code** | Integrated Development Environment (IDE) |

---

## ⚙️ Methodology & Project Stages

### 1. Data Preprocessing & Feature Engineering
* **Data Cleaning:** Confirmed zero missing values, allowing immediate progression to feature engineering.
* **Categorical Encoding:** Applied **One-Hot Encoding** to nominal features (`Country`, `Gender`) to prepare data for the machine learning algorithm.
* **Data Splitting:** Divided the data into 80% Training and 20% Testing sets, using **Stratification** to ensure balanced churn distribution across both sets.
* **Feature Scaling:** Applied **StandardScaler** to numerical features (`Age`, `Balance`, `Estimated_Salary`) to normalise data magnitude, which is crucial for the Logistic Regression model.

### 2. Exploratory Data Analysis (EDA)
* The baseline churn rate was calculated at **~20.37%**.
* **Key Findings:**
    * **Geographic Risk:** Customers in **Germany** showed the highest churn rate ($\mathbf{\approx 32.44\%}$).
    * **Demographic Risk:** **Female customers** and customers in the **40-60 age bracket** were identified as having significantly higher flight risk.

### 3. Model Training & Evaluation
* **Model:** A **Logistic Regression** classifier was trained as the initial benchmark model.
* **Performance:**
    * **ROC AUC Score:** **0.7748** (A good indicator of the model's ability to distinguish between churners and non-churners).
    * **Recall (Churn Class):** The model achieved a Recall of **~18.67%**, indicating that while predictive, the model needs further tuning (e.g., using different classification thresholds or advanced models like XGBoost/Random Forest) to increase its effectiveness in identifying high-risk customers for intervention.

---

## 💡 Key Model Insights (Feature Importance)
Coefficients extracted from the trained Logistic Regression model reveal the strongest risk factors driving churn:

1.  **Inactive Member Status:** The single greatest predictor of churn.
2.  **Geography (Germany):** Confirmed as a massive regional risk factor.
3.  **Customer Age:** Older customers show a strong positive correlation with the likelihood of churn.

---

## 🚀 How to Run the Project
1.  **Clone the Repository:**
    ```bash
    git clone [YOUR_REPOSITORY_LINK]
    ```
2.  **Install Dependencies:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```
3.  **Run the Script:**
    ```bash
    python analyzer.py
    ```
    *Note: Ensure the `Bank Customer Churn.csv` file is in the root directory.*

---

**Author:** [Oluremi Akindeko/[LinkedIn Profile Link](https://www.linkedin.com/in/oluremi-akindeko-aca-898189127/)]
