# Nyc-311-maintenance-analysis
An end-to-end data analysis project using NYC 311 Residential Maintenance Complaints (Jan–Nov 2025) to uncover building issues, hotspots, resolution delays, and actionable insights.

**Project Objectives**:
Identify the most common residential maintenance issues
Determine geographic hotspots across boroughs and ZIP codes
Measure repair timelines and identify delays
Analyze seasonal complaint patterns
Highlight unresolved or recurring issues
Provide actionable recommendations based on data insights

**Dataset**:
Source: NYC Open Data – 311 Service Requests
Timeframe: Jan 2025 – Nov 9, 2025
Final Dataset: 476k residential maintenance-related records
Key fields selected for analysis:
Complaint Type
Borough
ZIP Code
Created Date
Closed Date
Status
Latitude & Longitude

**Prepare Phase Summary**:
Filtered dataset for residential locations only
Included only maintenance-related complaint types
Removed irrelevant columns (Taxi, Vehicle Type, Highway, etc.)
Standardized ZIP codes (removed decimals)
Converted Created/Closed dates to datetime
Created Is_Closed status flag
Removed rows with missing geolocation
Saved cleaned dataset for analysis

**Process Phase Summary**:
Validated data types
Checked for missing values
Retained meaningful missing Closed Date values
Filled minor missing text fields (“Unknown”, “No update provided”)
Exported cleaned dataset for reuse

**Analysis Summary**:
1. Complaint Frequency
Heat/Hot Water is the most common residential maintenance issue, followed by Unsanitary Condition, Plumbing, and Paint/Plaster.
2. Geographic Hotspots
Bronx and Brooklyn show highest complaint volume
ZIP-level clusters strongly appear in 104xx and 112xx regions
3. Resolution Time
Elevator repairs are the slowest (~30+ days)
Heat/Hot Water complaints resolved fastest due to emergency priority
4. Monthly Trends
Complaints peak January–March
Drop in summer
Rise again in October
5. Unresolved Patterns
Elevator, Appliance, and Unsanitary Condition show highest unresolved rates
Borough × Issue heatmap reveals Manhattan + Bronx problem clusters

**Act Phase: Recommendations**:
Seasonal heating maintenance before winter
Targeted inspections in high-risk ZIP codes
Faster contractor deployment for elevator & exterior issues
Standardized SLAs across boroughs
Predictive maintenance for repeated failures
Dashboarding & automation for real-time monitoring
Improve tenant communication via SMS/email updates

**Project Structure**:
nyc-311-maintenance-analysis/
│
├── data/
│   └── cleaned_nyc311_2025.csv
│
├── images/
│   ├── complaints_by_borough.png
│   ├── complaint_frequency.png
│   ├── resolution_time.png
│   ├── unresolved_heatmap.png
│   ├── zip_hotspots.png
│   └── monthly_trend.png
│
├── notebooks/
│   └── nyc311_analysis.ipynb
│
├── README.md
└── requirements.txt

**Tools Used**:
Python
Pandas, NumPy
Matplotlib, Seaborn
Folium
Jupyter Notebook

**Conclusion**:
This project demonstrates how public 311 complaint data can be used to uncover structural building issues, optimize maintenance workflows, and improve residential living conditions across NYC.
Insights from this analysis support smarter planning, faster repair cycles, and strategic resource allocation.
