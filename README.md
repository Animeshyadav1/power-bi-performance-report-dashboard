# 📊 Power BI Performance Report Dashboard

## Overview

This Power BI project was created by following and implementing concepts from the "The Only Power BI Portfolio Project You Need" tutorial by Mo Chen. The dashboard provides a comprehensive view of business performance through interactive visualizations and advanced DAX calculations.

## Project Objectives

- Analyze Year-to-Date (YTD) business performance.
- Compare current year metrics with previous year performance.
- Monitor Sales, Quantity, and Gross Profit trends.
- Create dynamic KPI selection using slicers.
- Build an interactive dashboard for business decision-making.

## Dashboard Features

### Key Performance Indicators (KPIs)
- YTD Sales
- YTD Quantity
- YTD Gross Profit
- Previous Year YTD Metrics (PYTD)
- Year-over-Year Variance

### Interactive Elements
- Dynamic Metric Selection
- Date Filtering
- Product Filtering
- Interactive Visualizations

### Business Insights
- Sales Performance Analysis
- Profitability Trends
- Product Performance Tracking
- Time Intelligence Analysis

## Tools & Technologies

- Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Microsoft Excel

## Data Model

The project utilizes:
- Fact Table (Sales Data)
- Date Dimension Table
- Product Dimension Table
- Customer Dimension Table

## DAX Concepts Used

- CALCULATE()
- SAMEPERIODLASTYEAR()
- TOTALYTD()
- SWITCH()
- SELECTEDVALUE()
- Time Intelligence Functions

## Sample Measures

### Previous Year YTD Sales

```DAX
PYTD_Sales =
CALCULATE(
    [Sales],
    SAMEPERIODLASTYEAR(Dim_Date[Date])
)
```

### Dynamic KPI Selection

```DAX
S_PYTD =
VAR SelectedValue =
    SELECTEDVALUE(Slc_Values[Values])
RETURN
SWITCH(
    SelectedValue,
    "Sales", [PYTD_Sales],
    "Quantity", [PYTD_Quantity],
    "Gross Profit", [PYTD_GrossProfit]
)
```

## Dashboard Preview

<img width="1357" height="747" alt="Dashboard" src="https://github.com/user-attachments/assets/b6aa8bfa-2127-41a9-ba01-2dd5ff38b17a" />


## Files Included

- Performance Report.pbix
- Plant_DTS.xls
- Dashboard Screenshots
- README.md

## Learning Outcomes

Through this project I gained experience in:

- Data Modeling
- Power Query Transformations
- DAX Calculations
- Time Intelligence Functions
- Dashboard Design
- Business Performance Analysis

## Author

**Animesh Yadav**

GitHub: https://github.com/Animeshyadav1
