# 📊 Telecom Customer Churn & Retention Analytics

An end-to-end exploratory data analysis and cohort intelligence project investigating the behavioral, contractual, and service patterns driving customer attrition across 7,043 telecom accounts.

---

## 📌 Executive Summary

Customer churn is one of the most critical metrics in subscription businesses. In this dataset, the baseline churn rate is **26.54%** (1,869 churned customers out of 7,043), contributing to substantial Monthly Recurring Revenue (MRR) loss.

This project moves beyond surface-level visualizations to combine:
1. **Automated Pipeline Cleaning & Database Ingestion** via MySQL (XAMPP).
2. **Statistical Hypothesis Testing** (Chi-Square & Two-Sample T-Tests).
3. **Cohort Risk Segmentation** using Advanced SQL (CTEs, Window Functions).
4. **Actionable Business Recommendations** for subscription retention.

---

## 🛠️ Tech Stack & Tools

- **Programming:** Python 3.x
- **Data Manipulation:** Pandas, NumPy
- **Database & Querying:** MySQL, SQLAlchemy, PyMySQL
- **Visualization:** Seaborn, Matplotlib
- **Statistical Analysis:** SciPy (Hypothesis Testing)
- **Environment:** Jupyter Notebook / JupyterLab

---

## 🔍 Key Data Insights & Findings

### 1. The Critical Churn Window (Tenure)
- **Early Stage Risk:** Over **50% of total churn occurs within the first 6–12 months** of customer onboarding.
- Customers who stay past the 24-month threshold exhibit significantly higher brand loyalty and lower attrition.

### 2. Contract Vulnerability
- **Month-to-Month Contracts:** Churn rate spikes at **~42.7%**.
- **1-Year Contracts:** Churn drops to **~11.3%**.
- **2-Year Contracts:** Churn drops dramatically to **~2.8%**.
- *Takeaway:* Contract flexibility without retention incentives creates high customer volatility.

### 3. Payment Method & Billing Friction
- Customers paying via **Electronic Check** churn at an alarming rate of **~45.3%**, compared to <18% for credit card or bank auto-transfer methods.
- *Reason:* Electronic checks lack recurring automation, triggering regular manual payment evaluations by users.

### 4. Service-Level Vulnerability
- **Fiber Optic Internet:** Exhibits higher attrition rates (~41.9%) compared to standard DSL (~18.9%), despite fiber users having higher average monthly spend ($80+).
- *Takeaway:* Service reliability, onboarding support, or pricing satisfaction issues exist specifically within high-bandwidth plans.

---

## 🧪 Statistical Hypothesis Testing

To ensure observations were not due to random variation, inferential statistical tests were performed:

1. **Chi-Square Test of Independence (Payment Method vs. Churn):**
   - **Result:** $p < 0.001$ ($\chi^2 \approx 648.4$).
   - **Conclusion:** Strong, statistically significant dependency between payment method and customer churn probability.
2. **Independent Two-Sample T-Test (Monthly Charges):**
   - **Result:** Churned customers paid significantly higher average monthly charges ($74.44) compared to retained customers ($61.26) with $p < 0.001$.

---

## 💡 Business Recommendations & Strategy

1. **Auto-Pay Migration Incentive:**
   - Offer a one-time bill credit ($5–$10) or bundled data perks to convert Electronic Check payers to automated credit card/bank debit.
2. **First-Quarter Onboarding Campaign:**
   - Implement structured customer success check-ins at Day 30, 60, and 90 to mitigate early-tenure drop-offs.
3. **Annual Contract Transition Offerings:**
   - Incentivize month-to-month customers to switch to 1-year plans with discounted upfront billing tiers.
4. **Fiber Optic Service Quality Audit:**
   - Investigate customer service ticket volume for fiber lines to resolve setup friction and high attrition among premium users.

---

## 📂 Project Structure

```text
├── Data_refine.ipynb             # Main cleaning, SQL pipeline & EDA notebook
├── churn_risk_heatmap.png        # Generated risk correlation heatmap
├── customer_churn.csv            # Raw dataset
├── sql/
│   └── churn_analysis.sql        # Advanced SQL queries (CTEs, Window Functions)
└── README.md                     # Project documentation'""
-
🚀 How to Run the Project Locally
1. Prerequisites
Python 3.8+

XAMPP / MySQL Server running locally

2. Installation
Clone the repository:

Bash
git clone https://github.com/AbhiDevp151/telco-customer-churn-analytics.git
cd telco-customer-churn-analytics
Install necessary packages:

Bash
pip install pandas numpy matplotlib seaborn scipy sqlalchemy pymysql
3. Database Setup (Optional)
If running the MySQL ingestion:

Start MySQL in XAMPP (Port 3306 or 3307).

Create database telco_churn_db.

Execute the notebook cells to automatically stream data to MySQL.

👨‍💻 Author
GitHub: @AbhiDevp151
