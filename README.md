# Travel-Cost-Optimization-Axiom
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

<img width="624" height="424" alt="Picture1" src="https://github.com/user-attachments/assets/4becc97c-42fc-462c-9cc8-dd70ac968aaf" />


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

<img width="624" height="349" alt="Picture2" src="https://github.com/user-attachments/assets/e287d20e-0560-4907-bfe6-647bdd4c65f7" />


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

### 1. Travel expenditure decreased despite rising ticket prices

<img width="624" height="105" alt="Picture4" src="https://github.com/user-attachments/assets/cf9d9a9b-f5d5-4c12-b765-dd36bf1e7904" />

Total travel expenditure fell by 36.8% in 2024, while total flights decreased by 53.2%. However, the average cost per trip only declined by 1.3%, indicating that most savings resulted from reduced travel volume rather than improved travel cost efficiency.


### 2. Administrative and HR departments recorded the highest travel costs

<img width="624" height="96" alt="Picture5" src="https://github.com/user-attachments/assets/c1348a1d-6719-44a8-b924-f2cf1f6836ba" />


The Administration department generated the highest overall travel expenditure, while HR reported the highest average cost per trip. Both departments consistently exceeded the company-wide average ticket price benchmark, suggesting potential opportunities for cost control and travel policy review.

### 3. Premium-class usage exceeded policy thresholds in several areas

The company’s internal policy assumes premium-class bookings should remain below 35% of total trips. Analysis identified departments and routes that exceeded this threshold, increasing travel costs and indicating potential non-compliance with travel guidelines.

### 4. Several routes experienced significant cost inflation

<img width="468" height="182" alt="Picture6" src="https://github.com/user-attachments/assets/c065c108-9bc2-4acf-b1b7-6a43990894aa" />

Route-level analysis revealed that some routes recorded double-digit increases in average ticket prices between 2023 and 2024. In addition, more than 50% of bookings on certain routes were priced above their route-specific average, highlighting potential supplier pricing issues or inefficient booking behaviour.

### 5. Route performance varied significantly across the network

The Top 10 route analysis showed that high expenditure was not always driven by travel volume. Some routes generated disproportionately high costs because of higher ticket prices and elevated premium-class usage, making them priority candidates for cost optimisation initiatives.

---

## Recommendations

### 1. Strengthen control of premium-class bookings

Several departments and routes exceeded the company's assumed premium-class threshold of 35%. Management should introduce an approval process for Business and First-Class bookings above predefined limits and monitor compliance through monthly exception reports.

### 2. Review high-cost routes and negotiate with airline providers

Route-level analysis identified routes with substantial increases in average ticket prices between 2023 and 2024. The company should conduct periodic reviews of these routes and explore alternative airlines, negotiated corporate rates, or revised travel policies to reduce costs.

### 3. Focus on cost per trip rather than total expenditure

The analysis showed that lower total travel expenditure in 2024 was primarily driven by a reduction in travel volume rather than significant improvements in travel efficiency. Management should therefore use Cost Per Trip as the primary KPI when evaluating travel cost performance.

### 4. Establish department-level travel benchmarks

Departments such as Administration and HR recorded average ticket prices above the company benchmark. Introducing department-specific travel budgets and monitoring average ticket prices can improve accountability and encourage more cost-conscious travel decisions.

### 5. Integrate the dashboard into quarterly financial reviews

The dashboard should be incorporated into regular financial review meetings to monitor travel expenditure trends, policy compliance, and route performance. This would allow management to identify cost issues earlier and take corrective action before annual budgets are exceeded.

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
