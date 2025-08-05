# 📊 US Macro Economic Insights

A modern **data engineering and analytics pipeline** built with **Databricks**, **Delta Lake**, and **Power BI**, ingesting macroeconomic data directly from the [FRED API](https://fred.stlouisfed.org/). The system transforms **daily**, **monthly**, and **quarterly** indicators into clean, queryable Delta tables stored in **Azure Blob Storage Gen2**.

---

## 🏗️ Project Overview

This repo contains modular, production-grade ETL notebooks that process and unify macroeconomic time-series data into a curated data lakehouse.

### 🔁 Pipeline Highlights

- Automated ingestion and transformation of FRED datasets
- Full support for **daily**, **monthly**, and **quarterly** economic indicators
- Lakehouse architecture with **Delta Lake** and **Azure Storage**
- Seamless integration with **Power BI** for visualization
- Metadata logging and schema evolution

---

## 📁 Notebooks

| Notebook | Description |
|----------|-------------|
| `00_dim_date_builder` | Builds a unified date dimension table supporting daily, monthly, and quarterly granularities. |
| `01_fred_daily_pipeline` | Ingests and processes daily indicators like Federal Funds Rate, WTI Oil Prices, and Treasury Yields. |
| `02_fred_monthly_pipeline` | Ingests and transforms monthly macroeconomic data such as CPI, income statistics, and retail growth. |
| `03_fred_quarterly_pipeline` | Loads GDP and corporate profits from quarterly datasets. |
| `04_fred_orchestrator` | Orchestrates all pipeline stages end-to-end, from raw ingestion to warehouse registration. |

---

## 🗃️ Data Architecture (Delta Lake on Azure)

All tables are materialized as Delta tables and saved to **Azure Blob Storage Gen2**. The following tables are available in the `default` catalog:

- `fact_macro_daily`
- `fact_macro_monthly`
- `fact_macro_quarterly`
- `dim_date`
- `job_metadata` (pipeline logs)

---

## ⚙️ Technologies Used

- **Databricks (Notebooks + Jobs)**
- **Apache Spark (PySpark)**
- **Delta Lake**
- **Azure Blob Storage Gen2**
- **Power BI**
- **FRED API**
- **GitHub** (for CI/CD and version control)

---

## 📈 Dashboards


- 📉 GDP & Corporate Profits (Quarterly)
- 📊 CPI, Retail Sales, and Income Growth (Monthly)
- 💰 Interest Rates, Oil Prices, Treasury Yields (Daily)
- [View Full Project](https://ronenlasnick.github.io/github-fred/?utm_source=readme&utm_medium=github&utm_campaign=fred_macro)
---


## 📄 License

This project is licensed under the [Apache 2.0 License](LICENSE).

---

## 👨‍💻 Author

Built with ❤️ by **Ronen**  
Feel free to fork, contribute, or reach out for collaborations.
