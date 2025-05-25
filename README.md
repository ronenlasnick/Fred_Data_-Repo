# Fred_Data_-_Repo 📊

A data engineering and analytics pipeline built using **Databricks**, **Delta Lake**, and **Power BI**, powered by daily, monthly, and quarterly macroeconomic data sourced from the FRED API.

## 🏗️ Project Structure

This repo contains modular ETL notebooks designed to orchestrate and transform economic indicators into structured delta tables.

### 📁 Notebooks

| Notebook | Description |
|----------|-------------|
| `00_dim_date_builder` | Builds a unified date dimension from daily, monthly, and quarterly sources. |
| `01_fred_daily_pipeline` | Ingests and processes daily indicators like interest rates and oil prices. |
| `02_fred_monthly_pipeline` | Ingests and transforms monthly data such as CPI and income statistics. |
| `03_fred_quarterly_pipeline` | Processes GDP and corporate profits from quarterly FRED datasets. |
| `04_fred_orchestrator` | Orchestrates the full pipeline from staging to data warehouse registration. |

---

## 🗃️ Data Lake Locations (Delta)

The following delta tables are registered:

- `default.fact_macro_daily`
- `default.fact_macro_monthly`
- `default.fact_macro_quarterly`
- `default.dim_date`
- `default.job_metadata`

## 🛠️ Technologies

- **Databricks**
- **PySpark**
- **Delta Lake**
- **Power BI**
- **Azure Storage**
- **GitHub Integration**

---

## 🚀 Deployment

1. Clone the repository inside Databricks Repos.
2. Ensure cluster is running (DBR 13.3+ with Photon preferred).
3. Run `04_fred_orchestrator` to trigger full data pipeline.
4. Connect output tables to Power BI for visualization.

---

## 🔒 Git Integration Setup (Databricks)

If you're seeing auth errors:
- Make sure you have a valid GitHub PAT (token) with `repo` access.
- In Databricks → **User Settings** → **Git Integration**, paste the token.

---

## 📈 Sample Dashboards

Coming soon – Power BI dashboards visualizing GDP trends, CPI, interest rates, and more.

---

## License

This project is licensed under the [Apache 2.0 License](LICENSE).

---

Created with ❤️ by Ronen Lasnick