# Physical Medicine & Rehabilitation Dataset EDA and Preprocessing

**Name:** Yağmur Yilmaz  
**Email:** yagmurylmzz02@email.com  

---

## Project Overview

This project focuses on exploring and preprocessing a physical medicine & rehabilitation dataset containing 2235 patient observations with 13 features. The main goal is to perform an in-depth Exploratory Data Analysis (EDA) and prepare the dataset for potential predictive modeling. The target variable for this project is **TedaviSuresi (Treatment Duration)**.  

No model building is required; the focus is on making the data clean, consistent, and analyzable.

---

## Dataset Columns

- **HastaNo:** Anonymized patient ID  
- **Yas:** Age  
- **Cinsiyet:** Gender  
- **KanGrubu:** Blood type  
- **Uyruk:** Nationality  
- **KronikHastalik:** Chronic conditions (comma-separated)  
- **Bolum:** Department/Clinic  
- **Alerji:** Allergies (single or multi-label)  
- **Tanilar:** Diagnoses  
- **TedaviAdi:** Treatment name  
- **TedaviSuresi:** Treatment duration (sessions)  
- **UygulamaYerleri:** Application sites  
- **UygulamaSuresi:** Application duration  

---

## Preprocessing Steps

1. **Cleaning Categorical Columns:**  
   - Stripped leading/trailing spaces, converted all text to lowercase.  
   - Replaced `'nan', 'NAN', '<NA>', ''` values with proper missing values.

2. **Handling Missing Values:**  
   - Used `SimpleImputer(strategy="most_frequent")` to fill missing values in categorical columns.  

3. **Converting Columns to Numeric:**  
   - Extracted numeric values from `TedaviSuresi` and `UygulamaSuresi` columns.  

4. **Dropped Columns:**  
   - Removed `HastaNo` as it is not useful for analysis.  

---

## Exploratory Data Analysis (EDA)

- **Target Distribution:**  
  Histogram of `TedaviSuresi` with KDE.

- **Categorical Analysis:**  
  - Value counts and bar plots for `Uyruk`, `Cinsiyet`, `Bolum`.  
  - Boxplots to see treatment duration by `Uyruk`.

- **Numerical Relationships:**  
  - Scatter plot of `Yas` vs `TedaviSuresi`.  
  - Histogram comparison of `TedaviSuresi` and `UygulamaSuresi`.  
  - Correlation heatmap between `Yas`, `TedaviSuresi`, `UygulamaSuresi`.

- **Treatment Frequency Analysis:**  
  - Bar plot of the top 20 most frequent treatments.  
  - Line plot of average treatment duration by department.

---

## Instructions to Run the Code

1. Clone this repository:
```bash
git clone https://github.com/YourUsername/Pusula_Yagmur_Yilmaz.git
