# Insurance Premium Analysis 🏥

## Overview
Analyzed insurance premium data using MySQL & Excel to identify 
pricing patterns based on BMI, smoking status, and risk levels.

## Key Results
- Smokers and BMI ≥30 customers paid 60–80% higher premiums
- Removed 50+ data inconsistencies for clean analysis
- Built BMI classifier covering 4 categories & 3 risk levels
- Insights directly support pricing optimization strategy

## Tech Stack
MySQL | MS Excel | Dashboard Design

## Files
| File | Description |
|------|-------------|
| `insurance_analysis.sql` | SQL queries & BMI classifier logic |
| `insurance_dashboard.xlsx` | Excel dashboard with KPIs |
| `dataset.csv` | Insurance dataset |
| `dashboard_screenshot.png` | Dashboard preview |

## Analysis Steps
1. Data Cleaning — removed 50+ inconsistencies, validated BMI values
2. SQL BMI Classifier — categorized into 4 BMI groups
3. Risk Level Mapping — tagged 3 risk levels per customer
4. Excel Dashboard — KPIs tracking premiums by BMI & smoking status
5. Insights & Pricing Recommendations

## Dashboard Preview
<img width="1089" height="452" alt="image" src="https://github.com/user-attachments/assets/c0785730-6218-498c-9cd9-478614e63869" />


## Key SQL Logic
```sql
-- BMI Classifier
SELECT *,
  CASE 
    WHEN bmi < 18.5 THEN 'Underweight'
    WHEN bmi BETWEEN 18.5 AND 24.9 THEN 'Normal'
    WHEN bmi BETWEEN 25 AND 29.9 THEN 'Overweight'
    ELSE 'Obese'
  END AS bmi_category
FROM insurance_data;
```
