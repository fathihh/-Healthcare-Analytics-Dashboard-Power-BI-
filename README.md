# -Healthcare-Analytics-Dashboard-Power-BI-
This project presents an end-to-end Power BI dashboard built to analyze and monitor patient waiting list data. The goal is to transform raw healthcare data into meaningful insights that support operational and strategic decision-making.
🔹 Project Objective
Track current patient waiting list status
Analyze trends across Inpatient, Outpatient, and Day Case categories
Provide detailed insights by specialty, age group, and time bands
🔹 Key Features
📌 KPI Cards: Latest Month Wait List & Previous Year Comparison
📈 Trend Analysis: Monthly waiting list patterns
🔄 Dynamic Measures: Average vs Median toggle using DAX
🏥 Category Breakdown: Inpatient vs Outpatient performance
🧩 Granular Insights: Specialty-level & age-group analysis
🎯 Interactive Dashboard: Slicers, tooltips, and navigation
🔹 Tech Stack
Power BI Desktop
Power Query (Data Cleaning & Transformation)
DAX (Calculated Measures & KPIs)
Data Modeling (Relationships & Mapping Tables)
🔹 Data Processing Workflow
Requirement Gathering
Data Collection (Folder Connector)
Data Transformation (Cleaning, Appending, Structuring)
Data Modeling (Relationships & Mapping)
Dashboard Design & Visualization
Interactivity (Filters, Buttons, Tooltips)
Testing & Validation
🔹 Key DAX Measures
Latest Month Wait List = 
CALCULATE(
    SUM(All_Data[Total]),
    All_Data[Archive_Date] = MAX(All_Data[Archive_Date])
)

PY Latest Month Wait List = 
CALCULATE(
    SUM(All_Data[Total]),
    All_Data[Archive_Date] = EDATE(MAX(All_Data[Archive_Date]), -12)
)

Average Wait List = AVERAGE(All_Data[Total])

Median Wait List = MEDIAN(All_Data[Total])
🔹 Outcomes
Identified waiting list trends and peak demand periods
Enabled comparison across healthcare service categories
Delivered a clean and interactive dashboard for end users
🔹 How to Use
Download the dataset
Open .pbix file in Power BI Desktop
Refresh data (if needed)
Explore dashboard using slicers and filters
🔹 Future Improvements
Real-time data integration
Advanced forecasting using time-series models
Row-Level Security (RLS) implementation
