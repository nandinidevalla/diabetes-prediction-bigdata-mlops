# 📐 Project Design Outline: Diabetes Prediction MLOps Pipeline

This document outlines my structured approach to solving the diabetes prediction problem using big data and MLOps principles. Instead of simply following a course assignment, I treated this as a real-world data product — driven by reproducibility, scalability, and impact.

---

## 🔍 Problem Framing

**Goal:** Predict whether an individual is diabetic, prediabetic, or non-diabetic based on survey responses (CDC BRFSS 2015).  
**Type:** Multi-class classification  
**Motivation:** Enable early detection and support preventive health policy using data.

---

## 📁 Dataset Selection

- Dataset: CDC Diabetes Health Indicators (via [UCI ML Repo](https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators))
- Rows: 253,680  
- Target Variable: `Diabetes_012` (values: 0, 1, 2)  
- Format: Tabular  
- Domain: Public health, lifestyle, chronic disease

---

## 🧩 Project Breakdown

### 1. **Data Engineering & Cleaning**
- Removed duplicate records (~23.9K rows)
- Handled extreme values in BMI, PhysHlth, and MentHlth
- Used Spark DataFrames for all operations

### 2. **Feature Engineering**
- Selected key features based on correlation and domain knowledge:
  - HighBP, BMI, GenHlth, PhysHlth, DiffWalk, Age
- Scaled features using `StandardScaler`
- Combined into a single feature vector using `VectorAssembler`

### 3. **Exploratory Data Analysis**
- Checked class imbalance
- Mapped key health indicators across diabetes labels
- Identified strongest predictors and risk profiles

### 4. **Model Development**
- Trained and compared 4 ML models (LogReg, DT, RF, GBT)
- Addressed class imbalance with oversampling
- Evaluated models using accuracy, precision, recall, F1-score

### 5. **Automation & MLOps**
- Used **Spark ML Pipelines** to chain preprocessing + training
- Tracked model performance using **MLflow**
- Tuned hyperparameters using Spark’s `CrossValidator`

---

## 🔁 Reproducibility Practices

- Used **Parquet format** to store cleaned data
- Logged all metrics, parameters, and models with **MLflow**
- Structured notebook on **Databricks** for versioned collaboration

---

## 📌 Outcomes

- Best Model: **Gradient Boosted Trees (GBT)**  
- Accuracy: **84.7%**  
- Key Insight: Lifestyle and health access are critical risk levers for diabetes prediction  
- Strategy: Build targeted early-screening systems for at-risk populations

---

## 🙋‍♀️ Designed & Led by

Nandini Priya Devalla  
Graduate Student – Business Analytics, Purdue  
[LinkedIn](https://www.linkedin.com/in/nandini-devalla)
