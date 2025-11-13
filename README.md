# 📊 S&P 500 ESG Risk Ratings Dashboard  
### *Power BI | Data Analysis | ESG Risk & Controversy Insights*

---

## 📘 Project Overview  
This project analyzes **ESG (Environmental, Social, Governance) risk ratings** for S&P 500 companies using Power BI.  
It evaluates sector-level ESG exposure, controversy distribution, and risk category clustering to identify patterns and investment implications.  

The dashboard enables users to:  
- Assess ESG risk performance by sector and pillar  
- Benchmark governance and controversy levels  
- Detect high-risk clusters across industries  
- Support data-driven ESG investment decisions  

---

## 🗂️ Dataset Summary  

The dataset contains **503 company-level records** across multiple industries and ESG pillars.  
- **73 companies** have missing sector information (NA), leaving **430 valid entries** for analysis.  
- Each record includes total ESG risk scores, pillar-specific metrics, controversy indicators, and company details.  

The dataset supports multi-dimensional analysis for:  
✅ Sector-level risk averages  
✅ ESG pillar contribution  
✅ Controversy assessment  
✅ Company benchmarking  

---

### ⚠️ Missing Sector Data Impact  
Excluding 73 NA entries ensures more **accurate and unbiased** results for sector-level comparisons and ESG benchmarking.  

---

## 🧾 Dataset Fields  

| Column | Description |
|--------|--------------|
| Symbol | Unique stock symbol |
| Name | Company name |
| Address | Headquarters address |
| Sector | Economic sector |
| Industry | Specific industry classification |
| Full Time Employees | Total number of employees |
| Description | Overview of company’s operations |
| Total ESG Risk Score | Combined ESG risk indicator |
| Environment Risk Score | Environmental risk metric |
| Governance Risk Score | Governance quality score |
| Social Risk Score | Social responsibility score |
| Controversy Level | Category of ESG controversies |
| Controversy Score | Quantified controversy level |
| ESG Risk Percentile | Percentile ranking among peers |
| ESG Risk Level | Risk category (Negligible–Severe) |

---

## 🧹 Data Cleaning & Standardization  

Steps performed using **Power Query (Power BI)**:  
- Removed blank or NA rows  
- Converted numeric columns to correct data types  
- Standardized sector/industry naming conventions  
- Labeled missing ESG scores as “Not Rated”  

---

## 📐 ESG Metrics & Calculations  

### Total ESG Risk  
```DAX
**Total ESG Risk = [Environment Risk Score] + [Governance Risk Score] + [Social Risk Score]

ESG Risk Category = 
SWITCH(
    TRUE(),
    'esgriskscore'[Total ESG Risk Score] <= 10, "Negligible",
    'esgriskscore'[Total ESG Risk Score] <= 20, "Low",
    'esgriskscore'[Total ESG Risk Score] <= 30, "Medium",
    'esgriskscore'[Total ESG Risk Score] <= 40, "High",
    'esgriskscore'[Total ESG Risk Score] > 40, "Severe",
    "Unknown"
)**

Thresholds:
| Range | ESG Risk Level |
| ----- | -------------- |
| 0–10  | Negligible     |
| 10–20 | Low            |
| 20–30 | Medium         |
| 30–40 | High           |
| 40+   | Severe         |

📊 Dashboard Overview
KPIs

- Average ESG Risk Score

- Average Environmental, Governance, and Social Scores

- Average Controversy Score

- ESG Risk Level Distribution

**Visuals**

- Treemap: Sector-wise average ESG risk

- Bar Chart: Industry-level risk comparison

- Heatmap: ESG Percentile vs. Controversy Level

- Scatter Plot: ESG Risk vs. Full-Time Employees

**Dashboard**

![ESG Risk Dashboard Screenshot](https://raw.githubusercontent.com/<your-username>/<your-repo>/main/assets/ESG_Risk_Dashboard.png)



📈 Key Conclusions

“Across the top-performing companies, Governance risk constitutes 40–60% of overall ESG exposure.
Environmental risk is minimal due to asset-light models, while Social risk varies based on workforce and supply-chain complexity.”

🧩 Tools & Technologies Used

Power BI – Dashboard design & ESG visualization

Power Query – Data transformation and cleaning

DAX – KPI and risk category calculations

Excel – Data preprocessing and validation

💡 Final Takeaway

“Transparent ESG data transforms risk into opportunity — empowering investors and companies to align profit with purpose.” 🌱



