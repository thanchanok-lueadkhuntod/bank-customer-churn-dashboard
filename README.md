# Bank Customer Churn Analysis & Retention Strategy

## Project Overview
This project features an interactive Power BI dashboard designed to analyze customer attrition in the banking sector. The objective is to identify key churn drivers and provide the CRM team with an actionable target list for proactive retention campaigns.

## Tools & Technologies
- **Business Intelligence:** Power BI
- **Data Analysis:** DAX, Data Modeling
- **Advanced Visuals:** AI Key Influencers
- **UI/UX:** State-based navigation, Dynamic filtering

## Dashboard Pages & Features
### 1. Executive Summary
Provides a high-level overview of critical business metrics.
- **Key Metrics:** Total Balance Lost, Overall Churn Rate, High-Value Churns.
- **Visuals:** Churn rate by geographic region and customer distribution by product holding.
*(Insert Screenshot Here: ![Bank Customer Churn-1](https://github.com/user-attachments/assets/43bef256-bad6-4bbb-98d1-f075a70bf823)
)*

### 2. Churn Insights (Deep Dive)
Utilizes AI-driven analytics to uncover hidden patterns.
- **AI Key Influencers:** Automatically identified that customers holding >3 products have a significantly higher risk of churning.
- **Behavioral Analysis:** Heatmap detailing churn risk by credit card status and engagement levels.
*(Insert Screenshot Here: ![Bank Customer Churn-2](https://github.com/user-attachments/assets/abaf5a8a-68fe-46fd-8934-6a1b6d37a7f4)
)*

### 3. Action Plan & Target List
Translates raw data into a proactive business strategy for the CRM team.
- **Target List:** A prioritized table sorting at-risk customers by their account balance.
- **Business Impact:** Enables the call center to directly reach out to high-value accounts, minimizing potential financial loss.
*(Insert Screenshot Here: ![Bank Customer Churn-3](https://github.com/user-attachments/assets/54ab0749-0c38-47f2-af1d-867f2d657383)
)*

## Key DAX Measures Used
Here are some of the core DAX formulas engineered for this dashboard:
```dax
Total Balance Lost = 
CALCULATE(
    SUM(bank_data[balance]),
    bank_data[churn] = 1
)

Active Member Churn Rate = 
CALCULATE(
    [Churn Rate],
    bank_data[is_active_member] = 1
)
