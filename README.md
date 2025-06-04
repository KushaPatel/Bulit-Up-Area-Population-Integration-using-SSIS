# UK Built-up Areas ETL SSIS Project
This project demonstrates an end-to-end ETL (Extract, Transform, Load) solution using **SQL Server Integration Services (SSIS)** for data from UK built-up areas. It covers data import, validation, transformation, error handling, and data export.

---

## 🎯 Project Objectives
✅ Import data from a CSV file into a SQL Server table.  
✅ Validate data to ensure no duplicate entries.  
✅ Transform and categorize population data.  
✅ Export transformed data into a new CSV file.  
✅ Aggregate total population and store it in a separate table.  
✅ Implement robust error handling and logging.

---

## 📂 Source Data

- **CSV File:** `UK built-up areas.csv`  
- Fields include: `AreaName`, `Population`, and other demographic details.

---

## 🗂️ Destination Tables

| Table Name                | Purpose                                                                 |
|----------------------------|-------------------------------------------------------------------------|
| UKBuiltUpAreas            | Stores the raw imported data.                                            |
| UKBuiltUpAreasCategorized | Stores data with population category (High, Medium, Low).                |
| ImportErrors              | Logs errors during import, including row data and error descriptions.    |
| TotalPopulation           | Stores the aggregated total population for all built-up areas.           |


## ⚠️ Error Handling
- **Error Redirection:** Errors during data import (e.g., duplicate keys, data conversion issues) are redirected to the `ImportErrors` table.  
- **Logging:** Captures detailed error messages and the raw data that caused the issue.

---

## 🏗️ Key SSIS Components
- **Flat File Source:** For CSV file input.
- **OLE DB Destination:** For loading data into SQL Server tables.
- **Lookup Transformation:** For duplicate checks and referential integrity.
- **Conditional Split:** For error redirection.
- **Derived Column:** For data cleaning and transformations.
- **Aggregate Transformation:** For calculating total population.
- **Script/Derived Columns:** For detailed error descriptions.

---

## 🚀 Outcome
The final result is a set of **SQL Server tables** with cleaned, validated, and categorized data, along with a CSV export of transformed data and aggregated population totals. All errors are logged for auditing and troubleshooting.


