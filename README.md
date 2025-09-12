# Insurance SQL–Python Dashboard

End-to-end insurance analysis using SQL, Python, and dashboards.

---

## Key Business Questions
1. **Premium Drivers** – Which factors most influence the premium amount?  
2. **Risk vs. Revenue Segments** – Can we cluster customers into risk groups and compare profitability?  
3. **Retention & Upsell** – Which profiles are more likely to upgrade or renew?  

---

## Repository Structure
- **01_load_to_sqlite.ipynb** – Load and create SQLite database  
- **02_data_wrangling.ipynb** – Cleaning, handling missing values, feature engineering  
- **03_exploratory_data_analysis.ipynb** – Statistical summaries, correlations, outlier detection  
- **04_data_visualization.ipynb** – Charts and plots to answer business questions  
- **Data/** – Raw and processed datasets (ignored in `.gitignore`)  
- **Visualization/** – Saved charts and plots for reporting  

---

## How to Run
1. Clone the repo  
   ```bash
   git clone <your_repo_url>
