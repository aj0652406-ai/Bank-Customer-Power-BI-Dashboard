# ABC Bank Customer Overview Dashboard – Power BI

A simple one-page Power BI portfolio project built from the cleaned ABC Bank customer analytics dataset.

## Dashboard KPIs
- Total Customers: 100,000
- Average Balance: ₹752,740
- Churned Customers: 49,831
- Churn Rate: 49.8%

## Dashboard Visuals
- Customer Churn donut chart
- Customers by Age Group bar chart
- Average Balance by Account Type column chart
- Churn Rate by Income Group bar chart

## Slicers
- Gender
- Account Type
- City

## Power BI Skills Demonstrated
- Data modeling
- Power Query
- DAX measures
- KPI cards
- Interactive charts
- Slicers and filtering

## Open the project
1. Unzip the project folder.
2. Open `BankCustomerDashboard.pbip` in Power BI Desktop on Windows.
3. The dashboard data is embedded in the semantic model, so the project does not depend on a local CSV path.
4. Save as `.pbix` if you want a single Power BI file.

## DAX Measures
```DAX
Total Customers = DISTINCTCOUNT ( 'Bank'[Customer_ID] )
Average Balance = AVERAGE ( 'Bank'[Balance] )
Churned Customers = CALCULATE ( [Total Customers], 'Bank'[Churn] = "Yes" )
Churn Rate = DIVIDE ( [Churned Customers], [Total Customers], 0 )
```
