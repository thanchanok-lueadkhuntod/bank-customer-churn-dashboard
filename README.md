<img width="6000" height="3407" alt="Bank-Customer-Churn-1" src="https://github.com/user-attachments/assets/36e5002e-6bcd-4587-b0bf-bb97e75a6434" /><img width="6000" height="3407" alt="Bank-Customer-Churn-1" src="https://github.com/user-attachments/assets/a481c1a0-16c5-4eba-83fb-55a1891c4b66" /># Bank Customer Churn Analysis & Retention Strategy

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
*(Insert Screenshot Here: <img width="6000" height="3407" alt="Bank-Customer-Churn-1" src="https://github.com/user-attachments/assets/a094f776-fe57-4ece-889b-fb49f4435f5f" />
)*

### 2. Churn Insights (Deep Dive)
Utilizes AI-driven analytics to uncover hidden patterns.
- **AI Key Influencers:** Automatically identified that customers holding >3 products have a significantly higher risk of churning.
- **Behavioral Analysis:** Heatmap detailing churn risk by credit card status and engagement levels.
*(Insert Screenshot Here: <img width="6000" height="3407" alt="Bank-Customer-Churn-2" src="https://github.com/user-attachments/assets/33021243-114d-46f9-95a6-90430a84ec34" />
)*

### 3. Action Plan & Target List
Translates raw data into a proactive business strategy for the CRM team.
- **Target List:** A prioritized table sorting at-risk customers by their account balance.
- **Business Impact:** Enables the call center to directly reach out to high-value accounts, minimizing potential financial loss.
*(Insert Screenshot Here: <img width="6000" height="3407" alt="Bank-Customer-Churn-3" src="https://github.com/user-attachments/assets/3bfff1bf-86b0-4088-820b-208c54c2df66" />
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
