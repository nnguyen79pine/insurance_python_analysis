# Insurance SQL–Python Dashboard

This is my end-to-end project for analyzing an **insurance customer dataset** using **SQL, Python, and rich visualizations**.  
It walks through everything—from raw data cleaning to insight-driven dashboards—just like a real analytics workflow.

---

## Key Business Questions

During the analysis I focused on a few big questions:

1. **Premium Drivers** – Which factors most influence the insurance premium amount?  
2. **Risk vs. Revenue Segments** – Can we cluster customers into risk groups and compare profitability?  
3. **Retention & Upsell** – Which profiles are more likely to renew or upgrade their policies?

These questions shaped every step of the pipeline and the charts you’ll see in the notebooks.

---

##  Repository Structure

| Item                                      | Purpose                                                                               |
| ----------------------------------------- | ------------------------------------------------------------------------------------- |
| **01_load_to_sqlite.ipynb**              | Load the raw CSV into a SQLite database so we can query it with SQL.                  |
| **02_data_wrangling.ipynb**              | Clean, impute, and engineer features to prepare for analysis.                         |
| **03_exploratory_data_analysis.ipynb**   | Explore the cleaned dataset: distributions, outliers, correlations, and key patterns. |
| **04_data_visualization.ipynb**          | Final storytelling visuals that bring insights together for presentation.             |
| **Data/**                                | Original and cleaned CSV files (raw data is in `.gitignore`).                         |
| **Visualization/**                       | Final exported charts and plots for presentations and reports.                        |

Each notebook represents a stage of the workflow so you can follow along or reuse individual steps.  
Run them in order to see the full pipeline from start to finish.

---

##  How to Run

1. **Clone the repository**

   ```bash
   git clone https://github.com/nnguyen79pine/insurance-sql-python-dashboard.git
   cd insurance-sql-python-dashboard
