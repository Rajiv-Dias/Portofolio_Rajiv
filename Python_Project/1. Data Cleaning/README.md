# 🐍 Data Cleaning Master | Python Project

## 📊 Project Overview

**Project Title**: Data Cleaning Master  
**Level**: Beginner – Intermediate  
**Language**: Python  

This project is designed to automate the data cleaning and preprocessing process using Python. It transforms raw datasets into clean, structured, and analysis-ready data by handling common data quality issues such as missing values, duplicates, and inconsistent formats.

---

## 🎯 Objectives

- Automate data cleaning workflow  
- Validate dataset file and format  
- Handle missing values and duplicates  
- Standardize dataset structure  
- Generate clean datasets for further analysis  

---

## 🔄 Data Cleaning Workflow (Visual)

```mermaid
flowchart TD

A[Start Program] --> B[Input Dataset Path & Name]

B --> C{Check File Exists?}
C -- No --> D[Show Error & Stop]
C -- Yes --> E[Detect File Type]

E --> F{File Format}
F -- CSV --> G[Load CSV File]
F -- Excel --> H[Load Excel File]
F -- Unknown --> D

G --> I[Standardize Columns]
H --> I

I --> J[Check Dataset Dimension]

J --> K[Check Duplicates]
K --> L{Duplicates Found?}
L -- Yes --> M[Save Duplicate File]
M --> N[Remove Duplicates]
L -- No --> O[Skip]

N --> P[Check Missing Values]
O --> P

P --> Q[Handle Missing Values]
Q --> R{Column Type}

R -- Numeric --> S[Fill with Mean]
R -- Categorical --> T[Drop Rows]

S --> U[Reset Index]
T --> U

U --> V[Save Clean Data CSV]
V --> W[Save Clean Data Excel]

W --> X[End Process ✅]
```

---

## 🛠 Project Structure

### 1. File Validation & Loading

- Detect dataset format (CSV / Excel)  
- Validate file path  
- Handle parsing errors  

```python
if not os.path.exists(data_path):
    print('File not found.')
```

---

### 2. Data Standardization

- Convert all column names to lowercase for consistency  

```python
data.columns = [col.lower() for col in data.columns]
```

---

### 3. Data Exploration

- Check dataset dimensions  
- Identify duplicate records  
- Analyze missing values  

---

### 4. Data Cleaning

#### 🔁 Duplicate Handling

- Detect duplicate rows  
- Save duplicate records  
- Remove duplicates  

```python
data = data.drop_duplicates()
```

---

#### ❗ Missing Value Handling

- Numeric columns → filled with mean  
- Categorical columns → rows removed  

```python
if data[col].dtype in (float, int):
    data[col] = data[col].fillna(data[col].mean())
else:
    data.dropna(subset=[col], inplace=True)
```

---

### 5. Data Finalization

- Reset index after cleaning  

```python
data = data.reset_index(drop=True)
```

---

### 6. Output Generation

- Save cleaned dataset into:
  - CSV file  
  - Excel file  

```python
data.to_csv(f"{data_name}_Clean_data.csv", index=None)
data.to_excel(f"{data_name}_Clean_data.xlsx", index=None)
```

---

## 🔍 Key Features

- Automated data cleaning process  
- Supports CSV and Excel files  
- Detects and removes duplicates  
- Handles missing values intelligently  
- Generates clean datasets automatically  
- User-friendly execution  

---

## 💡 Key Insights

- Raw datasets often contain duplicates and missing values that reduce data quality  
- Automated cleaning improves efficiency and reduces manual effort  
- Clean data is essential for accurate analysis in tools like SQL and Power BI  

---

## 🛠 Skills Demonstrated

- Python Programming  
- Data Cleaning & Preprocessing  
- Pandas & NumPy  
- File Handling  
- Error Handling  
- Automation  

---

## 🚀 Tools & Libraries

- Python  
- Pandas  
- NumPy  
- OpenPyXL / xlrd  
- OS & File Handling  

---

## ▶️ How to Run

1. Run the script:

```bash
python your_script_name.py
```

2. Input:
- Dataset path  
- Dataset name  

3. Output:
- Cleaned dataset (CSV & Excel)  
- Duplicate dataset file (if exists)  

---

## 📂 Dataset

- Supports:
  - CSV files  
  - Excel (.xlsx) files  
- Works with structured datasets  

---

## 📊 Conclusion

This project demonstrates how Python can be used to automate data cleaning processes efficiently. It highlights the importance of preprocessing in data analytics and shows how raw data can be transformed into reliable and analysis-ready datasets.

---

## 👤 Author

**Rajiv Noor Said**  
Industrial Engineering Graduate | Aspiring Data Analyst  

🔗 LinkedIn:  
www.linkedin.com/in/rajiv-noor-said  

---

⭐ *This project showcases my ability to automate data cleaning and prepare high-quality datasets for analysis.*
