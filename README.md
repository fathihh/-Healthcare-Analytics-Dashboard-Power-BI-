# 📊 Healthcare Analytics Dashboard (Power BI)

An end-to-end Power BI project focused on analyzing **patient waiting list data** to generate actionable insights for healthcare decision-making.

---

## 🔹 Project Objective
- Track current patient waiting list status  
- Analyze trends across Inpatient, Outpatient, and Day Case  
- Provide insights by specialty, age group, and time bands  

---

## 🔹 Key Features
- KPI Cards: Latest Month Wait List & Previous Year Comparison  
- Trend Analysis: Monthly waiting list patterns  
- Dynamic DAX Measures: Average vs Median toggle  
- Category Comparison: Inpatient vs Outpatient  
- Detailed Analysis: Specialty-level & age-group insights  
- Interactive Dashboard: Slicers, tooltips, navigation  

---

## 🔹 Tech Stack
- Power BI Desktop  
- Power Query (ETL)  
- DAX (Data Analysis Expressions)  
- Data Modeling  

---

## 🔹 Workflow
1. Requirement Gathering  
2. Data Collection (Folder Connector)  
3. Data Transformation (Power Query)  
4. Data Modeling (Relationships & Mapping)  
5. Dashboard Design & Visualization  
6. Interactivity (Filters, Tooltips, Navigation)  
7. Testing & Validation  

---

## 🔹 Key DAX Measures
```DAX
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
