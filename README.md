# 🏦 Modern Banking Data Pipeline  
**Azure Data Lake Storage Gen2 | Databricks | Power BI**

---

## 📚 Project Overview

This project showcases an end-to-end **modern data pipeline** built using **Azure Data Lake Storage Gen2 (ADLS Gen2)**, **Azure Databricks**, and **Power BI**. 

The pipeline extracts raw banking data, cleans and transforms it using **PySpark**, applies **Slowly Changing Dimensions (SCD) Type 1**, and visualizes insights through **Power BI** reports published to **Microsoft Fabric**.

---

## 🏗️ Architecture Overview

**Multi-layered architecture:**

- 🥉 **Bronze Layer**: Raw data ingestion (CSV files)
- 🥈 **Silver Layer**: Cleaned and transformed data
- 🥇 **Gold Layer**: Final curated data applying SCD Type 1 logic (Delta Lake format)

🔒 **Security** is managed using **Azure Key Vault** and **Databricks Scopes**.

⚙️ **Automation** is achieved via **Databricks Workflows**.

📊 **Reporting** is performed using **Power BI**.

---

## 🗂️ Data Source

The project processes the following banking-related CSV files:

- `accounts.csv`
- `customers.csv`
- `loan_payments.csv`
- `loans.csv`
- `transactions.csv`

All files are initially ingested into the **Bronze folder** in **ADLS Gen2**.

---

## 🛠️ Technologies Used

| Service                  | Purpose                                       |
|---------------------------|-----------------------------------------------|
| Azure Data Lake Storage Gen2 | Data storage (Bronze, Silver, Gold layers)   |
| Azure Databricks          | Data processing with PySpark                  |
| Azure Key Vault           | Secure secrets and credentials               |
| Power BI                  | Data visualization and reporting             |
| Microsoft Fabric          | Publishing enterprise reports                |

---

## ⚙️ Workflow Summary

1. **Authentication**:
   - Service Principal authentication to Azure services.
   - Secrets managed via **Azure Key Vault** and accessed through **Databricks scopes**.

2. **Ingestion**:
   - Raw CSVs mounted and loaded into the **Bronze layer**.

3. **Transformation (Silver Layer)**:
   - Clean/transform raw data in the **Silver Notebook**.
   - Create joined Delta tables (IDs and Amounts).

4. **Curation (Gold Layer)**:
   - Implement **SCD Type 1** logic in the **Gold Notebook**.
   - Save final Delta tables to the **Gold layer**.

5. **Orchestration**:
   - **Databricks Workflow** automates Silver and Gold notebook execution.

6. **Visualization**:
   - Power BI connects to Gold layer data.
   - Reports modeled and published to **Microsoft Fabric**.

---

## 📦 Deliverables

- 📒 PySpark notebooks for Silver and Gold layer transformations.
- 🧩 Databricks Workflows for job automation.
- 📊 Power BI report based on Gold layer data.
- 🖼️ Architecture diagram.
- 📝 Documentation for setup and execution.


