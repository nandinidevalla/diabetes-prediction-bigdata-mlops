# 🧠 Diabetes Risk Prediction using Big Data & MLOps

A scalable, production-style ML pipeline to predict diabetes risk based on health and lifestyle factors. Built using Apache Spark, MLflow, and Databricks to simulate real-world big data and MLOps practices.

---

## 📌 Overview

This project applies distributed computing and MLOps principles to a real-world public health problem: predicting diabetes status from behavioral and demographic data. Using a 250K+ record dataset from the CDC, the pipeline is designed for scale, automation, and explainability.

---

## 🚀 What This Project Demonstrates

- ✅ End-to-end ML pipeline built with **Apache Spark MLlib**
- ✅ Experiment tracking and automation using **MLflow** on **Databricks**
- ✅ Scalable preprocessing with **Spark DataFrames**
- ✅ Health insights powered by **EDA, feature selection, and correlation analysis**
- ✅ Real-world MLOps mindset with reproducibility and class imbalance handling

---

## 📊 Dataset

- 📦 Source: [UCI ML Repository – CDC Diabetes Health Indicators](https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators)
- 📈 Records: 253,680 | Features: 22
- 🎯 Target: `Diabetes_012`  
  - `0` = No Diabetes  
  - `1` = Pre-diabetes  
  - `2` = Diabetes

---

## 🔧 Tech Stack

| Tool / Tech        | Role                                   |
|--------------------|----------------------------------------|
| **Databricks**     | Cloud-based platform for development   |
| **Apache Spark**   | Distributed data processing & modeling |
| **Spark MLlib**    | Machine learning at scale              |
| **MLflow**         | Model experiment tracking              |
| **Python**         | Core language for all processing       |
| **Pandas / Seaborn**| Local EDA and visualization           |
| **Parquet**        | Efficient data storage format          |

---

## 🧠 Project Workflow

1. **Data Preparation**
   - Removed 23.9K duplicate rows
   - Handled outliers and cleaned variables
   - Encoded + scaled features using `VectorAssembler` and `StandardScaler`
   - Stored as **Parquet** for efficiency

2. **Exploratory Data Analysis (EDA)**
   - Identified top predictors (e.g., HighBP, BMI, General Health)
   - Found links between diabetes and socioeconomic/lifestyle factors
   - Visualized correlations and data distributions

3. **Modeling**
   - Trained: Logistic Regression, Decision Tree, Random Forest, GBT
   - Used **One-vs-Rest** strategy for multi-class classification
   - Addressed class imbalance using **oversampling techniques**

4. **MLOps & Automation**
   - Used **MLflow** to log experiments, metrics, parameters
   - Performed hyperparameter tuning via Spark CV
   - Automated pipeline execution using **Databricks notebooks**

---

## 📈 Results

| Model                  | Accuracy  |
|------------------------|-----------|
| Logistic Regression    | ~81%      |
| Decision Tree          | ~82%      |
| Random Forest (Tuned)  | 84.52%    |
| **GBT (Tuned)** ✅     | **84.70%** |

---

## 📂 Repository Structure

```markdown
notebook/
└── diabetes_prediction_pipeline.ipynb # Full Spark-based ML pipeline

report/
├── final_report.pdf # Final write-up
└── project_design_outline.md # My structured plan for building the pipeline

presentation/
└── diabetes_prediction_presentation.pptx # Visual presentation deck
```
---

## 👩‍💻 Author

**Nandini Priya Devalla**  
M.S. Business Analytics & Information Management  
Purdue University  
[LinkedIn](https://www.linkedin.com/in/nandini-devalla)

---

## 💬 Why This Matters

This project simulates a real-world MLOps use case:  
- Reproducibility through experiment tracking  
- Scalable ML pipelines with Spark  
- Actionable healthcare insights via ML  


