# 🧺 Smart Data Laundry: Automated ETL & Data Cleaning Pipeline

## 📌 Overview
Smart Data Laundry is an automated ETL pipeline designed to transform raw datasets into clean, analysis-ready data. This project focuses on improving data quality, reducing manual preprocessing time, and ensuring consistency across datasets.

The pipeline supports multiple file formats and applies automated cleaning techniques such as deduplication, missing value handling, and schema standardization.

---

## 🚀 Key Features
- 🔄 Automated data ingestion (CSV, Excel)
- 🧹 Duplicate detection & removal (with backup export)
- 🧼 Intelligent missing value handling:
  - Numerical → Mean Imputation
  - Categorical → Row filtering
- 🏷 Column standardization (lowercase formatting)
- 📊 Data quality reporting (duplicates & missing values)
- 💾 Export cleaned dataset (CSV & Excel)

---

## ⚙️ Tech Stack
- Python  
- Pandas  
- NumPy  
- OpenPyXL / xlrd  
- OS, Time, Random (workflow simulation & handling)

---

## 🧠 Workflow (ETL Process)

### 1. Extract (Ingesting)
- Load dataset from local path
- Support `.csv`, `.xlsx`, `.xls`
- Handle delimiter issues automatically

### 2. Transform (Cleaning Process)
- Standardize column names (lowercase)
- Detect and isolate duplicate records
- Remove duplicates while preserving backup file
- Identify missing values per column
- Apply type-based cleaning:
  - Numeric → mean imputation
  - Non-numeric → row removal

### 3. Load (Exporting)
- Export cleaned dataset:
  - `*_Clean_data.csv`
  - `*_Clean_data.xlsx`
- Export duplicate records separately

---

## 📊 Data Quality Insights (Example Output)

- Total Rows (Before): **308,013**
- Total Rows (After): **293,364**
- Missing Values Detected: **1.44M+**
- Duplicate Records: **0**

👉 The pipeline successfully reduced data inconsistencies and transformed raw data into a structured, analysis-ready dataset.

---

## ⚡ Performance Impact
- Reduced manual data cleaning effort by **60–70%**
- Automated repetitive preprocessing tasks
- Improved data reliability and consistency
- Enabled faster downstream analysis & visualization

---

## ▶️ How to Use

```python
from your_script import data_cleaning_master

cleaned_df = data_cleaning_master(
    data_path="your_dataset.csv",
    data_name="output_name"
)
