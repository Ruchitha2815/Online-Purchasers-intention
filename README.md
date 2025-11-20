# 🛒 Online Shoppers Purchasing Intention – Machine Learning Project

## 📖 Overview

This project analyzes the Online Shoppers Purchasing Intention Dataset to build machine learning models capable of predicting whether a user will complete a purchase during their session on an e-commerce website.

The dataset contains rich behavioral features captured during online browsing sessions — such as page visits, bounce and exit rates, user type, traffic type, and special day scores — which can be used to understand decision-making patterns.

---

## 📂 Dataset Description

The dataset used in this project is the popular Online Shoppers Purchasing Intention Dataset from UCI ML Repository.

- **Number of Rows:** ~12,330
- **Number of Features:** 18 attributes + 1 target (Revenue)

### 🔍 Feature Groups

| Feature Group | Description |
|---|---|
| **Page Visit Metrics** | Administrative, Informational, ProductRelated and their durations |
| **Rate Metrics** | BounceRates, ExitRates, PageValues |
| **Time-based Metrics** | SpecialDay, Month |
| **User & Session Attributes** | OperatingSystems, Browser, Region, TrafficType, VisitorType, Weekend |
| **Target Variable** | Revenue → 1 = Purchase, 0 = No Purchase |

---

## 🎯 Objective

Predict whether a user session will lead to Revenue = 1 based on browsing patterns.

---

## 📊 Project Workflow

### 1️⃣ Importing Libraries

The project uses:

- **Pandas, NumPy** → Data handling
- **Matplotlib, Seaborn** → Visualizations
- **Scikit-Learn** → Modeling, preprocessing, metrics
- **XGBoost** → Gradient boosting

### 2️⃣ Data Preprocessing

**Handling Missing Values**
- Checking null values
- Validating numerical ranges
- Converting data types

**Categorical Encoding**
- VisitorType, Month, Weekend encoded using One-Hot Encoding
- Ensures models can process non-numeric data

**Train-Test Split**
- Train: 80%
- Test: 20%

### 3️⃣ Exploratory Data Analysis (EDA)

**Key EDA Steps:**
- Distribution of numerical features
- Correlation heatmap
- Comparison of features for Revenue=0 vs Revenue=1
- Detecting class imbalance
- Monthly purchasing trend
- Impact of user type (Returning vs New)
- Checking whether weekend activity connects to purchases

**🌟 Key Insights (General Trends):**
- Higher PageValues usually → higher probability of purchase
- Returning visitors convert more than new visitors
- High ExitRates and BounceRates → low purchase intention
- Months near major holidays show spikes (e.g., Nov)

### 4️⃣ Modeling & Machine Learning Pipeline

**Models Implemented:**

| Model | Description |
|---|---|
| **Logistic Regression** | Baseline linear classifier |
| **Decision Tree** | Rule-based non-linear classifier |
| **Random Forest** | Ensemble of trees (good for tabular data) |
| **XGBoost** | Gradient boosting (often top performer) |
| **KNN** | Distance-based classifier |
| **SVM** | Margin-based classifier |

**Standard ML Pipeline:**
1. Import model
2. Fit on training data
3. Predict on test data
4. Evaluate using metrics

### 5️⃣ Evaluation Metrics

**Metrics Used:**
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- ROC-AUC Score

**📌 Why These Metrics Matter?**

| Metric | Meaning |
|---|---|
| **Accuracy** | Overall correctness |
| **Precision** | How many predicted "buyers" were actual buyers |
| **Recall** | How many actual buyers were detected |
| **F1 Score** | Balance between precision & recall |
| **ROC-AUC** | Measures separation between classes |

### 6️⃣ Example Results Table

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---|---|---|---|---|
| **Logistic Regression** | 0.85 | 0.70 | 0.55 | 0.61 | 0.89 |
| **Random Forest** | 0.90 | 0.78 | 0.74 | 0.76 | 0.94 |
| **XGBoost** | 0.92 | 0.81 | 0.77 | 0.79 | 0.95 |

### 7️⃣ Business Interpretation of Results

**💡 Insights useful for e-commerce platforms:**

- Returning visitors should be targeted with personalized suggestions
- Improving UX on product pages reduces exit rates → higher conversions
- Increasing PageValues (recommendations, relevance, discounts) boosts purchases
- Marketing efforts around high SpecialDay scores (near holidays) are profitable

**This analysis can be used for:**
- ✔ Conversion optimization
- ✔ Targeted advertising
- ✔ Dynamic pricing
- ✔ Session-level user segmentation

---

## 🧪 How to Run the Project

### ✔ Requirements

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost
```

### ✔ On Kaggle

1. Open the project notebook in Kaggle
2. Run the cells sequentially
3. View results and visualizations inline

---

## 📁 Project Resources

- **Dataset:** Online Shoppers Purchasing Intention Dataset (UCI ML Repository)
- **Notebook:** Available on Kaggle
- **Platform:** Kaggle Notebooks

---

## 📌 Notes

This project is developed and run entirely on Kaggle, leveraging the platform's computational resources and integrated libraries.
