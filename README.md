#  Insurance Data Analysis with Python

This project demonstrates an end-to-end **data analytics pipeline** on a U.S. health-insurance dataset.  
Starting from raw CSV files, it walks through **data wrangling**, **exploratory data analysis (EDA)**,  
and **visual storytelling** to uncover premium drivers, customer segments, and actionable business insights.

---

## 1. Project Overview
### Business Context
An insurance company wants to understand what drives policy **Premium Amounts**  
and how to **segment customers** for targeted retention and upsell campaigns.

### Goals
1. Clean and standardize raw customer data for analysis and modeling.
2. Identify **premium drivers** using descriptive statistics and correlation analysis.
3. Segment customers into risk/revenue groups using clustering.
4. Visualize findings to communicate actionable insights to business stakeholders.

### Key Deliverables
| File / Folder | Purpose |
|---------------|--------|
| `01_data_wrangling.ipynb` | Cleaning, encoding, and scaling raw data |
| `02_exploratory_data_analysis.ipynb` | Statistical exploration, correlation, clustering |
| `03_data_visualization.ipynb` | Ranked driver charts, customer segments, profitability plots |
| `data/Insurance.csv` | Original dataset |
| `data/Insurance_cleaned.csv` | Cleaned, encoded, and scaled dataset |
| `Visualization/*.png` | Saved charts for reports and presentations |

---

## 2. Data Source
- **Dataset:** [US Health Insurance Premiums and Risk Factors](https://www.kaggle.com/datasets/ethancollins9786/us-health-insurance-premiums-and-risk-factors)
- **Size:** 2,082 rows × 23 columns
- **Key Fields:**  
  `Customer ID`, `Age`, `Gender`, `Marital Status`, `Occupation`, `Income Level`,  
  `Education Level`, `Coverage Amount`, `Premium Amount`, `Deductible`,  
  `Policy Type`, `Preferred Communication Channel`, `Risk Profile`, `Credit Score`,  
  `Driving Record`, `Life Events`.

---

## 3. Business Questions
The analysis is guided by four primary questions:

1. **Premium Drivers** – Which factors most strongly influence the insurance premium amount?
2. **Customer Segments** – Can we group customers into segments with distinct risk and revenue profiles?
3. **Segment Profitability** – Which customer segment provides the highest average revenue and should be prioritized for retention or upsell?
4. **Upsell Opportunity** – Which segment offers the largest customer count but the lowest premiums (ideal for cross-selling)?

---

## 4. Workflow Summary

### 4.1 Data Wrangling:
- **Consistency Checks:** Removed unrealistic ages (<18 or >100), negative premiums, and zero coverage amounts.
- **Missing Values:**  
  - Numeric: Median + Iterative Imputer  
  - Categorical: Mode (most frequent)
- **Encoding:** One-hot encoding for high-cardinality categorical variables (gender, marital status, occupation, education, policy type).
- **Scaling:** Standardized key numeric features (`Premium Amount`, `Coverage Amount`, `Deductible`, `Income Level`, `Credit Score`) to mean 0, std 1.
- **Output:** Cleaned dataset with **38 columns** saved as `Insurance_cleaned.csv`.

### 4.2 Exploratory Data Analysis:
- **Premium Distribution:** Premiums cluster around \$3,000 with a modest right tail.
- **Correlation Analysis:**  
  - Positive: **Coverage Amount** (+0.6) and **Income Level** (+0.4)  
  - Negative: **Deductible** (−0.5)  
  - Mild Positive: **Age**
- **Clustering:**  
  - K-Means (k=3) reveals:
    - **Segment 2:** High coverage & low deductible → highest premiums (~\$3,300)
    - **Segment 0:** Balanced mid-range (~\$2,930)
    - **Segment 1:** Low premium, high deductible (~\$2,100)
- **Retention Signals:** Premiums increase steadily with age, peaking in the 50–70 group.

### 4.3 Visualization & Segmentation:
- **Ranked Premium Drivers:** Bar chart confirms Coverage Amount as the dominant driver, followed by Deductible and Income.
- **Customer Segments:** Cluster size and average premium visualized to highlight high-value groups.
- **Segment Profitability:** Segment 2 generates the greatest revenue; Segment 1, despite its size, is least profitable—prime target for upsell.

---

## 5. Key Insights
* Coverage amount is the **primary driver** of premium pricing; deductible shows a strong negative effect.
* **Segment 2** (high coverage, low deductible) is the **most profitable** and should be prioritized for retention campaigns.
* **Segment 1** has the **largest customer count but lowest premiums**, presenting an opportunity for cross-selling or premium upgrades.
* Premiums rise with **age**, with the 50–70 group offering strong lifetime value potential.

---

## 6. Requirements
Install dependencies before running the notebooks:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
7. Reproduction Steps

   **Clone the repository:**
git clone https://github.com/<your-username>/insurance_python_analysis.git
cd insurance_python_analysis

   **Lauch Jupyter:**
jupyter lab

   **Run notebooks in order:**
   
         01_data_wrangling.ipynb

         02_exploratory_data_analysis.ipynb

         03_data_visualization.ipynb

   Each notebook saves intermediate outputs (Insurance_cleaned.csv, charts) for reuse.


8. Next Steps

- Integrate claims or external risk data for more robust segmentation.

- Train predictive models (e.g., logistic regression, gradient boosting) for churn or premium prediction.

- Deploy interactive dashboards (Tableau, Power BI, or Plotly Dash) for real-time business use.

9. License

MIT License – you are free to use, share, and adapt this project with attribution.
