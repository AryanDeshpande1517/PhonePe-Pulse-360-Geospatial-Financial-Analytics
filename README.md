<p align="center">
  <img src="Assets/8.1-PhonePe-Pulse-360-Banner.png" width="100%" />
</p>

# 📱 PhonePe Pulse 360
### Digital Payments Analytics & Forecasting Engine (Power BI)

> State-wise, District-wise & Category-wise Digital Payments Intelligence  
> Built using official PhonePe Pulse Open Data

## 📌 Project Overview

**PhonePe Pulse 360** is an end-to-end fintech analytics project built using the official PhonePe Pulse Open Data repository.

The dataset consisted of **5000+ nested JSON files**, which required a custom Python ETL pipeline before modeling in Power BI.

The dashboard delivers:
- State-wise transaction intelligence  
- District-level payment contribution  
- Consumer behavior analysis  
- Category growth tracking  
- Forecasting up to 2026  
- Root Cause Analysis using Decomposition Tree  

This project simulates a real-world **Digital Payments Analytics Environment** combining data engineering, BI modeling, and business insights.

## 🎯 Problem Statement

India’s digital payments ecosystem is growing exponentially.

This project answers:
- Which states drive the highest transaction value?
- How do districts contribute to overall state performance?
- Which transaction categories dominate?
- How fast is user adoption scaling?
- What is the projected future growth?
- What factors drive transaction changes at root level?

## 📊 Dashboard Structure

### 🗺 Digital Command Center
- India state-level transaction map  
- Total transaction amount  
- Transaction count  
- Average transaction value  
- Live state rankings  

### 🏙 Regional Analysis
- Top districts by payment amount  
- State contribution breakdown  
- Growth trend visualization  
- District performance matrix  

### 👥 Consumer Insights
- Registered user growth  
- Mobile brand market share  
- Brand loyalty by state  
- User base expansion trend  

### 🧾 Category Analysis
- Spending split by transaction type  
- Category growth wars  
- Average ticket value by category  
- State-level category preference  

### 📈 Growth Engine
- Forecasting up to 2026 (Q4)  
- Rank change tracking  
- Decomposition Tree for Root Cause Analysis  

## 🗺 Geographic Intelligence
The dashboard uses a **custom Shape Map (TopoJSON)** to enable:
- Dynamic state highlighting  
- Interactive regional zooming  
- Conditional color scaling  
- Context-aware filtering  
- Default national view with drill-down support  

This enhances geographic clarity and user experience significantly.

## ⚙️ Data Engineering Approach

The PhonePe Pulse dataset was not provided as flat CSV files.

Instead, it consisted of deeply nested JSON files structured by:
- State  
- Year  
- Quarter  
- Transaction Type  
- User Metrics  

A custom Python ETL pipeline was built to:
- Recursively parse nested JSON files  
- Normalize hierarchical data  
- Extract transaction and user metrics  
- Convert into structured CSV tables  
- Prepare datasets for Star Schema modeling  

All ETL logic is documented inside the `Scripts/PhonePe_Extraction.ipynb` file.

## 🛠 Tools & Technologies

- Python (JSON Parsing & ETL)
- Pandas
- Power BI Desktop
- Power Query
- DAX
- Star Schema Modeling
- Shape Map (TopoJSON)
- Forecasting
- Decomposition Tree

## 📷 Dashboard Preview

### 🗺 Home
![Home](Assets/1-Home.png)

### 🗺 DigiIND Command Center
![DigiIND Command Center](Assets/2-DigiIND-Command-Center.png)

### 🏙 Regional Warfare
![Regional Warfare](Assets/3-Regional-Warfare.png)

### 👥 Consumer Insights
![Consumer Insights](Assets/4-Consumer-Insights.png)

### 🧾 Category Analysis
![Category Analysis](Assets/5-Category-Analysis.png)

### 📈 Growth Engine
![Growth Engine](Assets/6.1-Growth-Engine.png)
![Growth Engine](Assets/6.2-Growth-Engine.png)

## 📂 Data Source

### PhonePe Pulse Open Data
Official Repository:  
https://github.com/PhonePe/pulse#readme  

> Raw JSON files are not redistributed in this repository.

## 📊 Key Metrics Implemented

- Total Transaction Amount  
- Transaction Count  
- Average Transaction Value  
- Registered Users  
- Category Growth  
- Forecasted Growth  
- Root Cause Breakdown  

## 📁 Repository Structure

PhonePe-Pulse-360/
│
├── Assets/ # Dashboard visuals, walkthrough PDF, banner, social preview
│
├── Datasets/ # Dataset references (no raw data included)
│ └── Data-Sources.md
│
├── Scripts/ # ETL + DAX documentation
│ ├── PhonePe_Extraction.ipynb
│ └── DAX-Measures.md
│
├── PhonePe-Pulse-360.pbix # Complete Interactive Power BI Dashboard
│
└── README.md

## 👤 Author

Aryan Deshpande  
> Aspiring Data Analyst
