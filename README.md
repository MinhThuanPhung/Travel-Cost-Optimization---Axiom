# Travel-Cost-Optimization-Axiom
This report presents a Tableau dashboard developed using Axiom Inc.’s corporate travel data. The dashboard supports finance analysis by examining travel expenditure, departmental spending, route pricing trends, and premium class usage. The insights help identify opportunities for cost optimisation and more efficient travel management.
# Travel Cost Optimisation Dashboard

## Project Overview

This project analyses corporate travel expenditure for Axiom Inc. using Tableau Prep Builder and Tableau Desktop. The dashboard was developed to support Finance Analysts in evaluating travel cost efficiency, monitoring policy compliance, and identifying opportunities for cost optimisation.

---

## Scenario
Following a period of rapid business expansion between 2016 and 2023, Axiom Inc. observed a significant increase in overall operational expenditure and corporate travel included in it. As the company entered 2025 under pressure to optimize costs across all operational areas, the CFO requested a comprehensive review of travel spend as part of a broader cost efficiency initiative. In that case, the Finance Analyst was tasked with examining the efficiency of corporate travel expenditure and identifying optimization opportunities. This research uses a dashboard which displays travel cost trends throughout different departments and travel routes and booking patterns. The study applies two assumptions for its analysis. First, it is assumed that Axiom Inc. operated with multiple airline providers prior to 2020, before transitioning exclusively to Oceanic Airlines from 2020 onwards. The second assumption states that Axiom Inc. maintains an internal travel policy which limits departments to less than 35 percent of their total trips for premium class bookings.
 ## Strategic Purpose
The main strategic objective of this project aims to assess Axiom Inc.'s corporate travel spending efficiency through cost management evaluation and identification of cost-saving areas. The main goal of this research shows that total cost data needs additional information because decreased expenses may result from fewer trips instead of actual efficiency gains.
The Finance Analyst works to achieve this objective through two main tasks which include measuring cost efficiency for each trip and identifying departments and routes that exceed their established spending limits and assessing how well employees follow corporate travel booking rules especially their use of premium class tickets.Together, these areas of focus provide the evidence base needed to deliver actionable recommendations to senior management.

To address this purpose, the dashboard provides an overview of travel expenditure spanning ten years from 2015 to 2024. The analysis then narrows its focus to 2023 and 2024 as the most recent years, enabling more practical and actionable insights into current cost efficiency and optimisation opportunities. 


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

The Tableau Prep flow comprised the following key steps:
The data preparation flow in Tableau Prep Builder comprised the following sequential steps:
Input Sources. The system processed two main datasets which included Southwest 2021(oceanic 2021) and Employee Flights (Airline employee bookings). The system added a Department file together with a geospatial Extract file that contained airport longitude and latitude coordinates at subsequent points in the process.
<img width="624" height="336" alt="Picture3" src="https://github.com/user-attachments/assets/24faa150-24ca-44c5-90fa-326255f9fa76" />

 
**Clean 1 & Clean 2**. The first steps of the cleaning process were conducted separately for each source of input because they needed to remove system-generated columns that included table names and file paths before the datasets could be merged. Before that one, Oceanic 2021 is unioned with other tables names Oceanic 2022, Oceanic 2023, Oceanic 2024. Removed columns : RowID, file path, Tables Names
The Oceanic 2021 Employee Flights dataset Union 1 was transformed into a single table that recorded all employee flight bookings throughout its entire operational period.
**Clean 0**. A post-union cleaning step standardised field naming and resolved mismatched fields resulting from the union operation.
**Aggregate 1**. Following the initial union and cleaning, the dataset was aggregated by route to calculate the average ticket price per route. This step produced a route-level reference table used in the subsequent join.
**Join 1 & Clean 3**. The main dataset was joined with the Aggregate 1 output. The additional information was added is average ticket per route.Replace 1st class ìn fare type by First Class. 
**Clean 3** then addressed null values in the airline column by Oceanic, group AA, American and American Airline into 1 group named American Airline. Standardised data types such as travel date, purchase date to date. Split route into 2 part then rename 2 them into Arrival and Departure then change role of these new field into airport.  Created calculated fields including booking timing classification and price comparison relative to route average. Removed PassengerID, 
 
**Aggregate 2**. Booking timing (early/late) and price comparison relative to route average (above/below) were aggregated to examine whether a relationship existed between booking behavior and ticket pricing. No meaningful insight was identified, and the relevant fields were subsequently removed from the final dataset.
 
**Clean 8.** Employee email uniqueness was verified by counting email occurrences per person, ensuring that the forthcoming department join would produce accurate one-to-one matches.

 <img width="624" height="496" alt="Picture4" src="https://github.com/user-attachments/assets/ec5e3bc1-d974-4763-915c-e3845df348e1" />

**Join 2 & Clean 9**. The dataset was joined with the Department file (By passenger email) to assign each employee's department, with unnecessary columns removed post-join. The process starts with passenger mail-1 column removal, followed by department field assignment with NA values except for rull. 
**Join 3 & Clean 8**. The first join added arrival airport longitude and latitude data from the geospatial extract which let users see geographic routes through Tableau Desktop. The combination of clean 8 and clean 10 generates Join 4. The process of clean 8 discarded these columns: Aerial Lattitude, arrival Longgitue, Airport code, airpot name. 
**Join 4 & Clean 9**. The combination of clean 8 and clean 10 generates Join 4. The dataset received complete geospatial enrichment when the final join added departure airport longitude and latitude coordinates.
**Clean 10**. Final cleaning applied to the fully joined dataset prior to output.
**Output**. The cleaned dataset was exported as the final data source for Tableau Desktop visualisation.
<img width="624" height="307" alt="Picture5" src="https://github.com/user-attachments/assets/04018b08-fdec-4ba4-949e-2536e542955d" />


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


### Lower travel expenditure was driven by reduced travel activity, not improved efficiency
In 2024, total travel costs dropped by 36.80% to reach $81,825, while total flights decreased by 53.19% to 675 trips. The Cost Per Trip decreased by 1.33% to $125.50, which showed that the cost decrease happened because of higher operational volumes instead of real efficiency gains. The Premium Class Rate increased by 2.46% to 25.77% despite decreased travel activity, which created a possible violation of corporate travel booking policy.
 
### The transition to Oceanic Airlines significantly reduced long-term travel costs
The dual-axis chart shows how Axiom Inc.'s travel expenses changed after they switched to Oceanic Airlines in 2020. Before the transition, airlines charged more than $300 to $400 for ticket prices which dropped to under $200 after the transition. The total flight expenditures maintained similar levels between 2021 to 2023 because travel volume doubled from pre-transition years, which proved that using one airline system delivered substantial financial savings. This suggests that the strategic decision to transition exclusively to Oceanic Airlines was well-founded and has been effective in containing unit costs at scale.

However, while the transition represents a sound long-term cost management strategy at the macro level, it does not preclude the need for ongoing efficiency optimisation at a more granular level. The sustained low average ticket price establishes a favourable baseline from which further analysis can identify year-on-year variations, departmental overspending, and route-level inefficiencies , all of which are examined in the subsequent charts to determine where additional cost optimisation opportunities exist within the current operating model.

 
### Business Development, Account Management and HR present the greatest cost-control opportunities
The two departments with the highest spending level for their operations work expenses because they need to travel more than other departments. The HR department together with the NA department spends the least amount of money because they travel less than other departments do.

The highest total expenditures belong to BD and Operation yet AM and HR maintain their lead in average ticket costs which reach $131.70 and $129.00 respectively both exceeding the business average. The departments show high travel expenses because they travel less often which makes their costs per trip more expensive than before. BD need to to pay attention in this scenario as it has highest epxenditures and cost per trip higher than average. Chart below also show that some top route, BD also need to reduce propotion of premium class ( DAL-LAG, DAL-ELP)
 
 
### Premium-class usage exceeded policy thresholds in several departments and routes
NA (other department) and AM recorded their highest premium class usage increase from the previous year, which showed they had worse policy compliance according to their results shown in coral. The Operation department and the BD department and the HR department showed minimal to negative changes which resulted in stable compliance or better compliance results for these departments.
 
Depend on the top route information for AM below , we can see that  ,AM need more strict rules in booking class for route DAL – LGA and DAL-ELP as these route increase propotion of premium class quite high compared with 2023 with 29.37% and 26.09$ respectively, and rate of premium class in these route also more than 25%, even 75%. This shows the managerment is ineffectively.
 
### Route-level analysis revealed that distance is not the primary driver of travel costs
The map shows all routes start from Dallas which creates a hub-and-spoke system for Axiom Inc. The map shows that multiple short-haul routes have darker blue encoding which means their average ticket prices exceed those of some longer-distance corridors. Axiom travel expenses show that route distance cannot predict ticket prices. The orange dot intensity shows that short-haul routes have higher flight volumes than longer routes which creates a situation where short corridors with high frequency and above-average unit pricing become an excessive cost burden that needs  investigation.
 
### DAL–LGA emerged as the highest-priority route for cost optimisation 
The premium class rates from DAL-LGA and DAL-ELP reach their highest point at 47.83% and 50.00% which exceeds the 35% benchmark. The premium class usage at DAL-LGA increased by 29.37% which represented the highest growth of all routes while the average ticket price rose by 5.02% making it the top route for cost optimization. The airline routes of DAL-HOU DAL-AUS and DAL-PHX showed decreasing average prices which indicated that company were making more economical booking choices for these routes.
 
 

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
