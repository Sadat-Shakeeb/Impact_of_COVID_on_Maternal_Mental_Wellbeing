# 🧠 Impact of COVID-19 on Mental Health in Pregnant Individuals

## 📘 Project Description
This project explores the **impact of COVID-19-related stresses on pregnant individuals and their infants** using survey-based data collected across Canada as part of the *Pregnancy during the COVID-19 Pandemic (PdP)* project.  

The analysis aims to understand the relationship between factors such as **socioeconomic status, maternal age, and delivery outcomes** with key **mental health indicators** including:
- **Edinburgh Postnatal Depression Scale (EPDS)**  
- **PROMIS Anxiety Scores**

---

## 📊 Dataset Information
The dataset contains survey responses from pregnant individuals during the COVID-19 pandemic in Canada.  

### **Key Columns**
| Column | Description |
|--------|-------------|
| **Maternal_Age** | Maternal age (years) at intake |
| **Household_Income** | Total household income before taxes and deductions (2019) |
| **Maternal_Education** | Maternal education level (categorical) |
| **EPDS** | Edinburgh Postnatal Depression Scale score (higher = greater severity) |
| **PROMIS_Anxiety** | Anxiety score (7–35; higher = greater severity) |
| **GAbirth** | Gestational age at birth (weeks) |
| **Delivery_Date** | Delivery month and year |
| **Birth_Length** | Infant birth length (cm) |
| **Birth_Weight** | Infant birth weight (grams) |
| **Delivery_Mode** | Mode of delivery (Vaginal or C-section) |
| **NICU_stay** | Was the infant admitted to NICU? (Yes/No) |
| **Threaten_Life** | Perceived danger to own life during COVID-19 (0–100) |
| **Threaten_Baby_Danger** | Perceived danger to unborn baby’s life (0–100) |
| **Threaten_Baby_Harm** | Worry about COVID-19 harming unborn baby (0–100) |

> Columns like `OSF_ID` and `Language` were removed during preprocessing.

---

## 🧹 Data Cleaning and Preprocessing
The following steps were performed to prepare the dataset for analysis:

- Removed irrelevant columns: **`OSF_ID`** and **`Language`**
- Dropped rows with high missing values in key outcome variables
- Removed duplicate rows
- Handled missing values appropriately (e.g., replaced with `-1` for visualization)
- Created new categorical features:
  - **Weight Category** — Healthy / Unhealthy based on `Birth_Weight`
  - **Height Category** — Healthy / Unhealthy based on `Birth_Length`
- Converted `Gestational_Age_At_Birth` from weeks to months
- Verified consistency in data types and formats

---

## 🔍 Exploratory Data Analysis (EDA)

### **Univariate Analysis**
- Descriptive statistics for all numerical columns (`count`, `min`, `max`, `std`, `quartiles`)
- Distribution plots using **`seaborn.kdeplot`**
- Frequency and missing value checks for categorical columns

### **Bivariate Analysis**
- Explored relationships between key factors and mental health outcomes:
  - **Maternal Age vs EPDS / PROMIS Anxiety**
  - **Household Income vs Anxiety / Depression**
  - **Threat Perception vs Income Level**
- Used:
  - **`seaborn.lineplot`** for continuous relationships  
  - **`plotly.express` histograms** for categorical comparisons  
- Performed **Logistic Regression (statsmodels)** to test associations between:
  - Maternal age and **NICU stay**
  - Maternal age and **unhealthy weight/height**

---

## 🧩 Key Findings and Conclusions

- Women aged **25–38 years** exhibit **lower anxiety and depression levels**, suggesting better maternal and infant care.
- **Conceiving beyond 42 years** increases the risk of **premature birth**.
- **Younger (<25)** and **older (>45)** mothers showed higher anxiety and depression, with increased worry about COVID-19’s effects.
- There is a **13% increase** in C-section probability **after age 38**.
- **Maternal age** is significantly associated with **NICU stay** and **unhealthy birth weight**, but not with height.
- **Low income** and **low education** levels are strongly linked to **higher EPDS and anxiety scores**.
- **High income** is correlated with **lower depression and anxiety risk**.
- **High EPDS scores** are associated with **premature births** and **higher NICU admission** likelihood.
- **Education and income** both significantly affect perceived worries about maternal and infant health.
- Advanced maternal age (40+) remains a risk factor for depression even among higher-income, well-educated women.

---

## 🧠 Insights Summary

| Factor | Observation |
|--------|--------------|
| **Age (25–38 yrs)** | Lower anxiety and depression |
| **Age > 42 yrs** | Higher risk of premature birth |
| **Income Level** | Higher income → Lower anxiety & depression |
| **C-section Likelihood** | Increases by 13% after 38 yrs |
| **Low Income + Low Education** | Highest vulnerability group |
| **High EPDS Scores** | Correlate with high anxiety and premature births |
| **NICU Stay** | Strongly associated with anxiety, depression, and low birth weight |

---

## 🧰 Tools and Libraries

The analysis was performed in **Python** using the following libraries:

| Library | Purpose |
|----------|----------|
| **pandas** | Data manipulation and preprocessing |
| **numpy** | Numerical operations |
| **matplotlib** | Data visualization |
| **seaborn** | Statistical plotting and distribution visualization |
| **statsmodels** | Hypothesis testing and logistic regression |
| **plotly** | Interactive visualizations |

---

## 📈 Future Work
- Incorporate **machine learning models** to predict high-risk pregnancies.
- Expand dataset with **postpartum follow-up data**.
- Perform **correlation network analysis** to identify co-dependent risk factors.

---

## 🧾 Author
**Sadat**  
📊 *Data Analyst | Python | SQL | Power BI | Machine Learning Enthusiast*  

If you found this project insightful, feel free to ⭐ **star** the repository and contribute improvements!
