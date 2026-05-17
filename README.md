# Analyzing-Smart-City-Bike-Sharing-Data-using-Power-BI
Public bike-sharing systems generate continuous data from hundreds of stations across different cities. The task is to analyze this real-time bike station dataset to understand station performance, usage efficiency, and operational patterns across cities.  Applying Power BI skills—from data cleaning and modeling to DAX and dashboarding.

# Dataset:
Source: [Dataset link](https://github.com/GeethaGunasekaran1/Project-Dataset/raw/refs/heads/main/bike-stations-sharing-data.xlsx)

# 🚲 Bike Sharing System Analysis Dashboard

## 📌 Project Overview

This project focuses on analyzing a **Bike Sharing System dataset** using Microsoft Power BI.
The objective of this project is to perform **data cleaning, transformation, and visualization** to derive operational insights related to bike availability, station status, free stands, and capacity utilization.

The dashboard provides an interactive view of station performance, operational issues, and geographic bike distribution. 

---

# 🎯 Project Objectives

* Perform data cleaning and transformation
* Analyze bike station operations
* Monitor bike and stand availability
* Identify operational problem areas
* Visualize geographic distribution of bike stations
* Create an interactive Power BI dashboard

---

# 🛠️ Tools & Technologies Used

* Microsoft Power BI
* Power Query Editor
* DAX (Data Analysis Expressions)
* Data Visualization Techniques

---

# 🧹 Data Cleaning & Transformation

The dataset was cleaned and transformed using **Power Query Editor** in Power BI. 

## ✔️ Cleaning Steps Performed

* Removed unnecessary columns
* Renamed columns for readability
* Replaced null and blank values
* Changed data types
* Filtered invalid records
* Split and merged columns
* Added conditional columns
* Removed duplicate records

## ✔️ Transformation Steps

* Applied calculated fields
* Standardized station data
* Cleaned geographic coordinates
* Improved data consistency

---

# 📊 Dashboard Visualizations

## 📌 Operational Metrics Dashboard

The dashboard displays important KPIs such as:

* Bikes Available
* Stands Available
* Total Capacity
* Bike Fill Rate
* Stand Free Rate

These metrics help monitor the overall operational efficiency of the bike sharing system. 

---

# 📈 Visualizations Included

## 1️⃣ Stations Count by Status

A donut chart was used to visualize the distribution of:

* Open Stations
* Closed Stations

### Insights

* Most stations are operational
* Few stations are currently closed



---

## 2️⃣ Available Bike Stands Analysis

A bar chart was created to compare:

* Available Bike Stands
* Contract Names

### Insights

* Identified stations with low stand availability
* Compared operational efficiency across regions

---

## 3️⃣ Top Problem Areas Table

A detailed matrix/table visualization was created to identify:

* Stations with Bikes
* Stale Stations
* Stations with Free Stands
* Capacity Violations

### Insights

* Brussels-Capitale, Lyon, and Toulouse showed higher operational issues
* Capacity violations were minimal



---

## 4️⃣ Geo Validity & Free Stand KPI Cards

KPI cards were used to display:

* Geo-valid stations
* Stations with free stands

### Insights

* Verified valid geographic locations
* Monitored stand availability effectively

---

## 5️⃣ Capacity vs Bikes Available Scatter Plot

A scatter chart analyzed the relationship between:

* Bike Capacity
* Bikes Available
* Station Status

### Insights

* Open stations generally had higher bike availability
* Some stations showed low utilization despite high capacity



---

## 6️⃣ Geographic Bike Availability Map

A map visualization displayed bike station locations using:

* Latitude
* Longitude

### Insights

* Identified high-density bike regions
* Visualized geographic bike availability patterns


## 7️⃣ Interactive Slicers

Slicers were added for:

* Contract Name
* Station Status
* Banking Bonus

This enabled dynamic filtering and better user interaction with the dashboard.

---

## 8️⃣ Detailed Operational Table

A tabular visualization was used to display:

* Station Name
* Address
* Status
* Bikes Available
* Stands Available
* Capacity
* Year & Month

### Insights

* Helped track station-level operational details
* Improved monitoring and reporting

---

# 📌 Key Insights

* Most bike stations were operational and active
* Certain regions showed higher stale station counts
* Bike availability varied significantly across locations
* Geographic analysis helped identify dense operational zones
* Capacity utilization patterns highlighted optimization opportunities

---

# 📷 Dashboard Preview

## Cleaning & Transformation Steps



## Final Dashboard



---

# 📖 Learning Outcomes

Through this project, I learned:

* Data cleaning and transformation in Power Query
* Building interactive dashboards in Power BI
* KPI and operational analysis
* Geographic data visualization
* Business intelligence reporting techniques

# 📌 Conclusion

This project successfully demonstrates the use of **Power BI for operational analytics and visualization**.
The dashboard provides valuable insights into bike station availability, operational efficiency, and geographic distribution, enabling better monitoring and decision-making for bike sharing systems.

# Executive summary

The provided dataset is station master data (station ID, name/address, latitude/longitude, banking/bonus flags,
station key). It does not include any revenue, cost, trip, or distance (km) fields, so questions like “highest/lowest
revenue per km” and “revenue trends over years” cannot be computed from this extract alone. What we can
conclude today is primarily about network coverage, data quality, and operational readiness by city/contract.
What the current data can tell us (actionable now)
1) Coverage footprint by city/contract
• Use Station_Key (or “Contract Name” derived from it) to quantify station counts by city/contract and
identify where the network is concentrated (e.g., multiple stations visible for Mulhouse, Lyon, Seville, etc.
in the sample).
• This supports decisions like where to prioritize data feeds, QA checks, and operational monitoring.
2) Data quality and usability readiness
• Geo Valid (lat/long present and within bounds) enables a clear map-ready coverage rate; any
invalid/missing coordinates block spatial analysis and routing-based KPIs.
• Is Test Station flags non-production stations; these should be excluded from performance reporting to
avoid skew.
3) Product/service feature coverage
• Banking and Bonus allow a quick segmentation of stations by payment capability and bonus eligibility—
useful for identifying service parity gaps by city/contract (e.g., “which cities have low banking-enabled
station coverage?”).
Why the required revenue questions cannot be answered (and what’s needed)
To answer:
• Which cities earned highest/lowest revenue per km?
• How have revenues changed over the years?
• Which cities are underperforming with low cost efficiency?
You need at minimum (at city and date granularity):
1. Revenue: fare revenue (and ideally pass/subscription allocation rules) with a date field.
2. Distance (km): either actual trip kilometers (preferred) or estimated distance from trip OD
(origin/destination) coordinates.
3. Cost: operating cost by city/date (maintenance, rebalancing, staffing, capex allocation), or a proxy (service
hours, truck rolls, etc.).
4. Time series structure: a transaction or daily summary table with City/Contract, Date, Revenue, Trips, Km,
Cost.
Without those, any “revenue per km” or “cost efficiency” conclusion would be speculative.
