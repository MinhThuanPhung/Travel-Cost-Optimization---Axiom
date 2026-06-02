# Travel-Cost-Optimization---Axiom
This report presents a Tableau dashboard developed using Axiom Inc.’s corporate travel data. The dashboard supports finance analysis by examining travel expenditure, departmental spending, route pricing trends, and premium class usage. The insights help identify opportunities for cost optimisation and more efficient travel management.
# Travel Cost Optimisation Dashboard

## Project Overview

This project analyses corporate travel expenditure for Axiom Inc. using Tableau Prep Builder and Tableau Desktop. The dashboard was developed to support Finance Analysts in evaluating travel cost efficiency, monitoring policy compliance, and identifying opportunities for cost optimisation.

---

## Business Problem

Following rapid business growth between 2015 and 2024, Axiom Inc. experienced a significant increase in corporate travel expenditure. The Finance team required a dashboard to answer the following questions:

- Is travel expenditure being managed efficiently?
- Which departments generate the highest travel costs?
- Which routes are becoming more expensive?
- Are employees complying with the company’s premium-class travel policy?
- Where can travel costs be reduced?

---

## Dashboard Preview

![Dashboard](images/dashboard.png)

---

## Data Sources

| Dataset | Description |
|----------|------------|
| Employee Flights | Historical employee flight bookings |
| Oceanic Airlines | Additional airline booking records |
| Department File | Employee-to-department mapping |
| Airport Geolocation Extract | Airport coordinates for route mapping |

---

## Data Preparation (Tableau Prep Builder)

The data preparation workflow included:

- Data cleaning and standardisation
- Union of multiple booking datasets
- Route-level aggregation
- Department enrichment through joins
- Geospatial enrichment for route mapping
- Creation of calculated fields
- Data quality validation

### Tableau Prep Flow

![Prep Flow](images/prep_flow.png)

---

## Key Performance Indicators (KPIs)

### Total Cost
Total travel expenditure.

### Total Flights
Total number of trips taken.

### Cost Per Trip
Average ticket cost per trip.

### Premium Class Rate
Percentage of Business and First-Class bookings.

---

## Dashboard Features

### Travel Cost Trend Analysis
- Travel expenditure by year
- Cost per trip trends
- Airline transition analysis

### Department Analysis
- Flight expenditure by department
- Cost per trip by department
- Premium class usage by department

### Route Analysis
- Interactive route map
- Top 10 most expensive routes
- Route-level cost benchmarking

---

## Key Insights

### 1. Travel volume decreased significantly in 2024
Total flights fell by more than 50%, reducing overall travel expenditure.

### 2. Some departments exceed the company benchmark
Several departments recorded higher-than-average ticket prices and premium-class usage.

### 3. Premium-class usage remains a controllable cost driver
Certain departments and routes exceeded the internal threshold of 35% premium-class bookings.

### 4. Route-level analysis identified high-cost routes
Several routes experienced substantial increases in average ticket prices between 2023 and 2024.

---

## Recommendations

- Strengthen monitoring of premium-class bookings.
- Review high-cost routes annually.
- Introduce route-specific travel budgets.
- Increase visibility of departmental travel performance.
- Expand dashboard usage for quarterly travel reviews.

---

## Tools Used

- Tableau Desktop
- Tableau Prep Builder
- Microsoft Excel

---

## Skills Demonstrated

- Business Intelligence
- Data Cleaning
- Data Transformation
- Dashboard Design
- KPI Development
- Data Visualisation
- Financial Analysis
- Cost Optimisation Analysis

---

## Author

**Thi Minh Thuan Phung**

MBS Finance & Business Analytics  
South East Technological University (SETU)
