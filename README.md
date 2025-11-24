# 🧠 Impact of COVID-19 on Mental Health in Pregnant Individuals

## 📘 Project Description
This project explores the **impact of COVID-19-related stresses on pregnant individuals and their infants** using survey-based data collected across Canada as part of the *Pregnancy during the COVID-19 Pandemic (PdP)* project.

The analysis examines how factors such as **socioeconomic status, maternal age, and delivery outcomes** relate to key **mental health indicators**, including:
- **Edinburgh Postnatal Depression Scale (EPDS)**
- **PROMIS Anxiety Scores**

---

## 📊 Dataset Information
The dataset contains detailed survey responses from pregnant individuals across Canada during the COVID-19 pandemic.

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
| **Delivery_Mode** | Delivery method (Vaginal or C-section) |
| **NICU_stay** | Was the infant admitted to NICU? (Yes/No) |
| **Threaten_Life** | Perceived danger to own life during COVID-19 (0–100) |
| **Threaten_Baby_Danger** | Perceived danger to unborn baby’s life (0–100) |
| **Threaten_Baby_Harm** | Worry about COVID-19 harming unborn baby (0–100) |

> Columns such as `OSF_ID` and `Language` were removed during preprocessing.

---

## 🧹 Data Cleaning and Preprocessing
The dataset was thoroughly cleaned and prepared using the following steps:

- Removed irrelevant columns (**`OSF_ID`**, **`Language`**)
- Dropped rows with excessive missing values in key outcome variables
- Removed duplicate entries
- Handled missing values (e.g., replaced with `-1` for visualization purposes)
- Created new features:
  - **Weight Category** (Healthy / Unhealthy based on `Birth_Weight`)
  - **Height Category** (Healthy / Unhealthy based on `Birth_Length`)
- Converted **Gestational Age at Birth** from weeks to months
- Ensured consistent data types and formats across columns

---

## 🔍 Exploratory Data Analysis (EDA)

### **Univariate Analysis**
- Descriptive statistics for all numerical features  
- KDE distribution plots using **seaborn**
- Frequency counts and missing-value summaries for categorical variables  

### **Bivariate Analysis**
Explored relationships between maternal characteristics and mental health outcomes:

- **Maternal Age vs EPDS / PROMIS Anxiety**
- **Household Income vs Anxiety / Depression**
- **Income Level vs Threat Perception**

Analysis methods included:
- **seaborn.lineplot** for numerical trends  
- **plotly.express histograms** for categorical comparisons  
- **Logistic Regression (statsmodels)** to analyze associations between:
  - Maternal age and **NICU stay**
  - Maternal age and **unhealthy infant weight/height**

---

## 🧩 Key Findings and Conclusions

- Women aged **25–38** show **lower anxiety and depression levels**, indicating better maternal and infant outcomes.  
- Pregnancies beyond **42 years** have a higher risk of **premature birth**.  
- **Younger (<25)** and **older (>45)** mothers experience elevated anxiety and depression levels.  
- There is a **13% increase in C-section likelihood** after age **38**.  
- **Maternal age** is significantly associated with NICU admission and low birth weight.  
- **Lower income** and **lower education** correlate strongly with higher EPDS and anxiety scores.  
- **Higher income** individuals tend to have lower depression and anxiety risk.  
- High EPDS values correlate with **premature births** and **increased NICU stays**.  
- Education and income meaningfully affect perceived threats to maternal and infant health.  
- Advanced maternal age (40+) remains a risk factor for depression even among high-income, well-educated women.

---

## 🧠 Insights Summary

| Factor | Observation |
|--------|-------------|
| **Age (25–38 yrs)** | Lower anxiety and depression |
| **Age > 42 yrs** | Higher premature birth risk |
| **Income Level** | Higher income → Lower anxiety/depression |
| **C-section Probability** | +13% after 38 yrs |
| **Low Income + Low Education** | Most vulnerable group |
| **High EPDS Scores** | Linked to anxiety and premature births |
| **NICU Stay** | Strongly associated with mental health and low birth weight |

---

## 🧰 Tools and Libraries
Analysis was conducted in **Python** using the following libraries:

| Library | Purpose |
|---------|---------|
| **pandas** | Data manipulation & preprocessing |
| **numpy** | Numerical computations |
| **matplotlib** | Basic visualization |
| **seaborn** | Statistical visualizations |
| **statsmodels** | Regression & hypothesis testing |
| **plotly** | Interactive charts |

---

## 📈 Future Work
- Develop **machine learning models** for predicting high-risk pregnancies  
- Include **postpartum follow-up data** for long-term analysis  
- Perform advanced **correlation network analysis**  
- Build **interactive dashboards** for real-time insights  

---

## 🧾 Author
**Sadat**  
📊 *Data Analyst | Python | SQL | Power BI | Machine Learning Enthusiast*

If you found this project useful, feel free to ⭐ **star the repository** and contribute enhancements.
