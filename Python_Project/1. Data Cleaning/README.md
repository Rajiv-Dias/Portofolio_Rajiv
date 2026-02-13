🧺 Smart Data Laundry: Automated Cleaning Pipeline

Tired of dealing with messy datasets, annoying duplicates, and cluttered numerical columns? Smart Data Laundry is a streamlined Python-based tool designed to automate the data cleaning process for both .csv and .xlsx files, ensuring your data is "analysis-ready" in seconds.
✨ Why This Project?

Data cleaning often consumes up to 80% of a data professional's workflow. This project aims to accelerate that process with the following features:

    Auto-Detection: Automatically identifies file formats and handles common delimiter issues.

    Smart Imputation: Automatically fills missing values (nulls) in numerical columns using the Mean (μ).

    Integrity Guard: Instead of just deleting duplicates, the system isolates and saves them into a separate file for auditing purposes.

    Consistency: Ensures all column names are standardized to lowercase and the index is reset for a clean, sequential structure.

🚀 Workflow

    Ingesting: Loads CSV or Excel files from your local path with built-in error handling.

    Deduplicate: Identifies and isolates "twin" records, preserving a copy before removal.

    Sanitizing:

        Numerical Columns: Implements Mean Imputation (μ) for any missing values.

        Categorical/Text Columns: Removes rows with missing values to maintain data quality.

        Smart Formatting: Attempts to convert "string-trapped" currency or numeric data into proper formats.

    Exporting: Saves the refined results into both .csv and .xlsx formats for maximum compatibility.
