# SaaS-GAAP-Financial-Analysis-with-Power-BI

**Project Overview**


This project demonstrates an end-to-end GAAP-aligned SaaS financial analysis built entirely in Power BI. It showcases advanced data modeling, Power Query transformations, and DAX techniques to calculate and analyze core SaaS metrics such as MRR, ARR, churn, retention, cohorts, unit economics, profitability, and cash flow.
The project is designed to mirror real-world FP&A, RevOps, and SaaS analytics workflows, with all KPIs calculated from first principles (no pre-aggregated metrics in the dataset).

**Project Link:** 

**Objectives**

- Build a GAAP-style SaaS financial model in Power BI
- Apply advanced DAX time intelligence, iterators, and context transitions
- Analyze revenue growth, customer retention, and unit economics
- Create executive-ready dashboards and financial insights
- Demonstrate interview-ready analytics and business storytelling skills

**Dataset Summary**

**Grain:** Customer × Month
**Source:** CSV (synthetic GAAP-style SaaS data)

**Key Fields**

- CustomerID
- MonthDate
- OriginalFee
- DiscountPct
- NetMRR
- ExpansionMRR
- ChurnStatus (Yes / No)
- CAC
- GrossMarginPct
- OperatingMarginPct
- CashInflow
- CashOutflow

No KPIs (ARR, retention, churn rates, etc.) are pre-calculated.

**Data Preparation (Power Query)**

- Imported CSV using Get Data → CSV
- Cleaned and validated data types
- Removed duplicates and invalid rows
- Standardized churn status values
- Unpivoted cash flow columns for waterfall analysis
- Created a centralized fact table
- Built supporting dimension tables (Calendar)

**Data Modeling**

- Star-schema design
- Fact table connected to a dedicated Calendar table
- Relationships built on MonthDate
- Calculated columns for:
    - First Active Month
    - Months Since Sign-Up
    - Numeric Churn Flag

**KPIs & Metrics Calculated (DAX)**


**Revenue & Growth**

- Monthly Recurring Revenue (MRR)
- Annual Recurring Revenue (ARR)
- Net New MRR
- MRR MoM % and YoY %
- Rolling 3- and 12-Month MRR

**Customer & Retention**

- Churn Rate
- Retention %
- New Customers
- Cohort Retention Analysis
- Active vs Churned Customers

**Monetization & Unit Economics**
  
- ARPU (Average Revenue per User)
- ARPPU (Average Revenue per Paying User)
- Expansion Rate
- Customer Lifetime Value (LTV)
- CAC and LTV/CAC Ratio
- CAC Payback Period (Months)

**Profitability & Finance**

- Gross Margin
- Operating Margin
- Operating Cash Flow
- Net Cash Flow

**Dashboards**


**Executive SaaS Overview**

- Monthly Recurring Revenue (MRR) Trend
- MRR Month-over-Month Growth (%)
- Revenue Composition: Base vs Expansion vs Churn
- Annual Recurring Revenue (ARR) Trend

**Customer Retention & Cohort Analysis**

- Customer Retention by Cohort Month
- Monthly Customer Churn Rate
- Active vs Churned Customers Over Time
- Customer Lifecycle: Months Since Sign-Up

**Monetization & Unit Economics**

- ARPU vs ARPPU Trend
- Expansion MRR Contribution
- CAC Payback Period

**Financial Performance & Cash Flow**

- Gross Margin Trend
- Operating Margin Trend
- Operating Cash Flow Waterfall
- Cash Inflows vs Cash Outflows

**Key DAX Concepts Demonstrated**

- Time intelligence (MoM, YoY, rolling periods)
- Iterators (SUMX, AVERAGEX)
- Context transition with CALCULATE
- Filter context manipulation (ALL, ALLSELECTED)
- Cohort and lifecycle analysis

**Validation & Best Practices**

- Numeric flags used for calculations; text used only for display
- Retention calculated using starting customer base
- ARPPU calculated with explicit paying-customer filter
- GAAP-aware revenue and margin logic


**Business Value**

This project simulates how SaaS companies monitor growth and revenue quality, identify churn and retention risks, Evaluate unit economics and scalability, Balance growth vs profitability (Rule of 40)
