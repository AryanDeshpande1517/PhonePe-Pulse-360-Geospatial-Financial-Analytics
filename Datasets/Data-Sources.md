# 📂 Dataset Documentation

## PhonePe Pulse Open Data

**Official Repository:**  
https://github.com/PhonePe/pulse#readme  

The dataset consists of 5000+ nested JSON files organized hierarchically by:

- State
- Year
- Quarter
- Transaction Type
- Registered Users
- Device Information

## 📁 Dataset Structure (Original Format)

The data was stored in nested directory form:

```
state/year/quarter/transaction_type.json
```

Each JSON file contained structured transaction and user data for specific time periods and regions.

## ⚙️ Data Engineering Process

Since the dataset was not provided in flat tabular format:

A custom Python ETL pipeline was built to:

- Recursively parse nested JSON files
- Normalize hierarchical structures
- Extract transaction metrics
- Extract user metrics
- Aggregate data into structured CSV tables
- Prepare datasets for Star Schema modeling in Power BI

The ETL pipeline is documented inside:

```
Scripts/PhonePe_Extraction.ipynb
```

## ⚠️ Licensing & Redistribution

This repository does **not redistribute raw JSON files** from PhonePe Pulse.

To reproduce this project:

1. Clone or download the official PhonePe Pulse repository.
2. Run the provided ETL notebook.
3. Import generated CSV files into Power BI.
4. Apply DAX measures as documented.

## 📊 Data Prepared for Modeling

After ETL, the following structured datasets were generated:

- Aggregated Transactions
- Aggregated Users
- Category-Level Transactions
- District-Level Data
- Time-Based Master Calendar

These datasets were then modeled using a Star Schema design.