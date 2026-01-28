# 🎓 Graduate Admission Probability Analysis (Jamboree Case Study)

## 📌 Project Overview

This project analyzes the key factors influencing graduate school admissions from an Indian applicant’s perspective and builds a statistically sound model to estimate the **probability of admission**.

The objective is not merely prediction, but **understanding**:
- Which factors truly matter
- How these factors interact
- How reliable and interpretable such a model can be

The project follows a **business-first, statistics-driven approach**, closely aligned with real-world analytics and decision-making.

---

## 🎯 Vision & Motivation

Jamboree helps thousands of students prepare for international graduate programs. While most platforms emphasize scores and cutoffs, this project aims to answer deeper questions:

- What actually drives admission decisions?
- Are standardized tests as important as long-term academic performance?
- How much independent value does research experience add?
- Can we build a model that is both **accurate** and **explainable**?

**Vision:**  
To create an interpretable, statistically valid model that helps students and platforms like Jamboree make **data-informed, realistic decisions**, rather than relying on opaque heuristics or score obsession.

---

## 🧠 Problem Statement

Identify the most important factors influencing graduate admission chances and build a linear regression model that can estimate admission probability while satisfying all key statistical assumptions.

---

## 📊 Dataset Description

The dataset contains profiles of 500 graduate applicants with the following attributes:

- GRE Score  
- TOEFL Score  
- Undergraduate CGPA  
- University Rating  
- Statement of Purpose (SOP) strength  
- Letter of Recommendation (LOR) strength  
- Research Experience (0/1)  
- Chance of Admit (target variable)

---

## 🧭 Analytical Approach

This project prioritizes **interpretability over black-box accuracy** and follows a structured analytics workflow:

1. Understand the data before modeling  
2. Validate assumptions before trusting results  
3. Resolve multicollinearity instead of ignoring it  
4. Explain decisions, not just report metrics  

---

## 🔍 Step-by-Step Process

### 1️⃣ Exploratory Data Analysis (EDA)

- Verified data quality (no missing values, no duplicates)
- Classified variables into continuous, ordinal, and binary
- Analyzed distributions to ensure representation across applicant profiles
- Studied relationships between predictors and admission probability

**Outcome:**  
Confirmed that the dataset reflects a realistic, merit-diverse applicant pool suitable for regression analysis.

---

### 2️⃣ Correlation & Bivariate Analysis

- Examined feature–target relationships visually
- Built a correlation matrix to identify overlapping predictors
- Observed strong correlations among CGPA, GRE, and TOEFL

**Key Insight:**  
Multiple variables were measuring the same underlying concept — **academic strength** — leading to multicollinearity.

---

### 3️⃣ Baseline Linear Regression (OLS)

- Built an initial OLS model using statsmodels
- Interpreted coefficients, p-values, and overall fit
- Identified variables losing significance due to overlap

**Learning:**  
Statistical significance reflects **unique contribution**, not surface-level correlation.

---

### 4️⃣ Multicollinearity Resolution (VIF)

- Computed Variance Inflation Factor (VIF)
- Iteratively removed redundant variables
- Used domain logic to guide elimination

Final retained predictors:
- **CGPA** – long-term academic performance  
- **Research Experience** – independent academic readiness signal  

**Outcome:**  
A clean, stable feature set with acceptable multicollinearity levels.

---

### 5️⃣ Final Regression Model

Final model structure:

Chance of Admit = f(CGPA, Research)

- R² ≈ 0.79
- Both predictors statistically significant
- High interpretability and coefficient stability

**Insight:**  
A simpler model retained most explanatory power while being far more reliable.

---

### 6️⃣ Regression Assumption Testing

All key assumptions were tested:

- Mean of residuals ≈ 0  
- Linearity (Residuals vs Fitted plot)  
- Homoscedasticity (visual inspection + Breusch–Pagan test)  
- Normality of residuals (Histogram and QQ plot)

**Conclusion:**  
Minor deviations were expected due to the bounded nature of the target variable, but overall assumptions were reasonably satisfied.

---

### 7️⃣ Model Performance Evaluation

- Train–test split (80/20)
- Metrics: MAE, RMSE, R²

**Results:**
- MAE ≈ 4–5 percentage points
- Stable RMSE
- Test R² slightly higher than train R²
- No evidence of overfitting

---

## 📈 Key Findings

- **CGPA is the strongest predictor** of admission probability
- **Research experience adds independent value**
- Standardized tests add limited incremental information once CGPA is known
- Qualitative factors often reinforce academic signals rather than act independently

---

## 💡 Business & Product Implications

- Encourage students to focus on long-term academic consistency
- Promote research exposure for competitive applicants
- Use admission probability as a **decision-support tool**, not a guarantee
- Collect richer profile data to enhance future models

---

## 🧾 Final Outcome

This project delivers a:
- Statistically sound  
- Interpretable  
- Business-aligned  

graduate admission probability model, while demonstrating a complete end-to-end analytical thought process.

---

## 🛠️ Tools & Concepts Used

- Python (Pandas, NumPy, Seaborn, Matplotlib)
- Statsmodels (OLS Regression)
- Scikit-learn (Train/Test Split, Metrics)
- Exploratory Data Analysis
- Linear Regression Assumptions
- Variance Inflation Factor (VIF)

---

## 📌 Closing Note

This project emphasizes **how to think like an analyst**, not just how to build models.  
Every modeling decision is statistically justified and grounded in real-world reasoning.
