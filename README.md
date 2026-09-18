## NorthBridge Healthcare Operations - Excel & Power Query

This project documents the Excel and Power Query stage of the NorthBridge healthcare operations analytics project.

The work began with the raw healthcare service-ticket dataset and focused on cleaning, validating and exploring the data before it was taken into SQL and Power BI. The final cleaned dataset contained 3,500 tickets and was loaded back into Excel as Tickets_Clean.

## Project Objectives
Clean and standardise the raw ticket data
Validate data quality and consistency
Create response and resolution time measures
Add useful agent and client information
Analyse SLA performance and operational workload
Establish baseline findings for the later SQL and Power BI stages
Power Query — Data Cleaning & Validation

**Power Query was used to clean and validate the Tickets dataset.**

Key checks included:

Duplicate TicketID and TicketReference checks
Missing-value checks for key fields
Data-type validation
SLA breach value validation
Response, resolution and SLA due-date checks
SLA breach logic validation

No duplicate TicketIDs or TicketReferences were found, and no missing values were identified in the main required fields. Timestamp and SLA checks also returned no errors.

Expected blanks in FirstResponseAt and ResolvedAt were retained as nulls for open tickets rather than being converted to zero.

**Calculated Fields**

Power Query was also used to create:

ResponseTimeHours
ResolutionTimeHours

These measures were calculated from ticket creation time to first response and resolution respectively.

**Excel Analysis**

The cleaned data was then explored in Excel to establish baseline operational insights.

**SLA Performance**
Total tickets: 3,500
SLA breaches: 754
Overall SLA breach rate: 21.54%
Highest priority breach rate: P1 — 28.68%
Highest category breach rate: Category 5 — 24.34%
Highest channel breach rate: Phone — 23.87%
Highest status breach rate: Escalated — 47.37%
Response & Resolution
Average response time: 5.06 hours
P1 average response time: 1.18 hours
P4 average response time: 14.24 hours
P1 average resolution time: 5.29 hours
P4 average resolution time: 83.44 hours
Agent & Workload Analysis

Excel was used to analyse ticket volume, agent capacity, workload pressure, roles and hubs.

The workload-pressure calculation was treated as an indicator rather than true daily utilisation, because ticket counts covered the analysis period rather than necessarily one working day.

**Hub & Client Analysis**

The analysis also examined workload by hub and client-level SLA performance.

Highest hub workload: Manchester — 1,346 tickets
Highest identified client SLA breach rate: Marshfield Health Associates — 33.33%
Excel Techniques Used

The analysis used:

XLOOKUP for agent and client information
PivotTables for grouped analysis and percentages
SUMIF for hub-level totals
UNIQUE for distinct hub lists
SORTBY for workload rankings
Calculated SLA breach rates
Date grouping by year, quarter and month

These calculations created an audit trail from the cleaned dataset to the operational insights later reproduced in SQL and visualised in Power BI.

Data Flow
Raw Healthcare Data
        ↓
Excel
        ↓
Power Query — Cleaning & Validation
        ↓
Excel — Exploratory Analysis
        ↓
SQL
        ↓
Power BI — 9 Interactive Dashboards
Tools Used

Excel | Power Query

**Repository Description**

Excel and Power Query analysis of a healthcare service-ticket dataset, covering data cleaning, validation, SLA performance, response and resolution times, agent workload, hub workload and client analysis before the SQL and Power BI stages.

## Stream Wave Project Overview

This project focused on analysing streaming content engagement and subscriber retention using Excel. The analysis examined viewing behaviour across different genres to understand which types of content generated the highest engagement, repeat viewership, and subscriber retention.

### Data Preparation

The project began by importing multiple CSV files into Excel and preparing the data for analysis.

The data preparation process included:

* Importing multiple CSV files
* Removing duplicate records
* Handling missing values
* Standardising genre names
* Ensuring the data was consistent and suitable for analysis

### Genre Engagement Analysis

Pivot tables were created to summarise total watch hours by genre, allowing different genres to be compared based on overall viewing activity.

Additional engagement metrics were calculated, including:

* Average completion rate by genre
* Repeat viewers by genre
* Distinct users who watched multiple titles within the same genre

These metrics provided a broader view of engagement beyond total viewing hours.

### Subscriber Retention Analysis

The project analysed the relationship between genres viewed and subscription status by comparing subscribers who renewed with those who cancelled.

A cross-tabulation was used to identify patterns between genre engagement and subscriber retention, highlighting genres that appeared to be associated with lower churn and stronger subscriber retention.

### Visualisation

Excel visualisations were created to communicate the key findings clearly.

The analysis included:

* Bar charts showing total viewing hours by genre
* Line charts showing monthly viewing trends for the top five genres
* Interactive dashboard elements for exploring the results

### Genre Performance Ranking

Genres were ranked based on their overall performance across three key areas:

* **Engagement**
* **Subscriber retention**
* **Repeat viewership**

This approach provided a more comprehensive assessment of genre performance rather than ranking genres solely by viewing hours.

### Executive Dashboard

The final stage of the project involved creating an interactive Excel executive dashboard** designed to present the key findings to decision-makers.

The dashboard brought together key metrics, visualisations, and genre rankings in one accessible view. Excel slicers were incorporated to allow users to interactively filter and explore the results.

### Project Outcome

The project provided a data-driven understanding of which genres attracted viewers, encouraged repeat viewing, and contributed to subscriber retention.

The analysis and dashboard supported content and subscription decision-making by highlighting high-performing genres and examining the relationship between content engagement and customer retention.


# Credit Card Customer Segmentation Analysis Project Overview

This project focused on analysing and segmenting credit card customers using Excel to understand customer value, spending behaviour, and retention patterns.

The analysis used RFM-related measures, including Recency/Frequency/Monetary scoring, to classify customers into different value and spending segments. The dashboard provided an interactive view of customer behaviour through slicers for RFM Score, Frequency, Monetary value, credit limit, and purchase-related measures.

The analysis examined customer value by comparing high-value and low-value customers, while the spender segmentation categorised customers into Excellent Spender, Good Spender, Low Spender, and No Spender groups.

The project also analysed customer churn and retention, identifying customers who were at risk, churned, or retained. This provided a clearer understanding of customer retention patterns and helped highlight segments that could require additional engagement or retention strategies.

The final Excel dashboard brought these analyses together into an interactive reporting tool, allowing customer segments and financial characteristics to be explored through slicers and visualisations.

# Bike Sales Project Overview

This project focused on analysing customer characteristics and purchasing behaviour to understand the factors associated with bike purchases.

The Excel dashboard examined bike purchasing patterns across different customer demographics, including gender, age bracket, income, marital status, and commute distance.

The analysis compared customers who purchased bikes with those who did not, providing insights into differences in average income and purchasing behaviour across demographic groups.

Customer age was also grouped into age brackets, allowing bike purchases to be compared across adolescent, middle-age, and older customers. The dashboard further examined the relationship between commute distance and bike purchases, showing purchasing patterns across different commuting ranges.

An interactive Marital Status slicer was included to allow users to filter the analysis between married and single customers. The dashboard therefore provided a consolidated view of customer demographics and purchasing behaviour, making the analysis easier to interpret for business decision-making.
