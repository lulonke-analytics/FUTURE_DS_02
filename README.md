# Customer Retention & Churn Analysis (Task 2)
## Executive Summary
This project presents an Executive Customer Retention & Churn Dashboard created in Power BI for a subscription-based service provider. By analysing subscriber demographics, contract structures, and service features, this dashboard identifies financial revenue at risk and provides strategic recommendations to boost customer retention.

## Data Preparation & DAX Methodology
- **Data Cleaning**: Resolved blank entries in 'Total Charges', converted formats to Decimal, and handled Regional Locale settings.
- **Segmentation**: Categorized customer tenure into custom age brackets ('0-12 Months', '13-24 Months', '25-48 Months', '49+ Months').
**Core DAX Measures**:
- 'Total Customers = COUNT('Telco Customer Churn Task 2' [customerID])'
- 'Churned Customers = CALCULATE([Total Customers], 'Telco Customer Churn Task 2' [Churn] = "Yes")'
- 'Churn Rate % = DIVIDE([Churned Customers], [TotalCustomers], 0)'
- 'Lost Monthly Revenue (Risk) = CALCULATE(SUM('Telco Customer Churn Task 2' [MonthlyCharges]), 'Telco Customer Churn Task 2' [Churn] = "Yes")'
- 'Average tenure (Months) = AVERAGE('Telco Customer Churn Task 2'[tenure])'

- ## Actionable Recommendations
- **Onboarding Incentives**: Implement a 90 day campaign encouraging new Month-to-Month subscribers to transition to discounted 1 year contracts.
- **Service Bundling**: Offer a complimentary 3 month Tech Support trial for Fiber Optic customers to reduce technical friction.

- ## Dashboard Preview
- ![Customer Churn Dashboard](Task2 Dashboard PNG) 
