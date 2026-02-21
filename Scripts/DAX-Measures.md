# 📊 DAX Measures Documentation

This document outlines the key DAX measures implemented in **PhonePe Pulse 360**.

The measures are grouped into:

- Core Financial Metrics  
- Time Intelligence  
- Forecasting Support  

All calculations were implemented inside Power BI using DAX.

# 📈 Core Financial Metrics

## Total Transaction Amount

```DAX
Total Transaction Amount =
SUM('phonepe_aggregated_transactions'[Transaction_Amount])
```

## Total Transaction Count

```DAX
Total Transaction Count =
SUM('phonepe_aggregated_transactions'[Transaction_Count])
```

## Avg Transaction Value

Calculates the average ticket size per transaction.

```DAX
Avg Transaction Value =
SUM('phonepe_aggregated_transactions'[Transaction_Amount]) /
SUM('phonepe_aggregated_transactions'[Transaction_Count])
```

# 📅 Time Intelligence

## Transaction Date

Creates a proper date column from Year and Quarter for time-series modeling.

```DAX
Transaction Date =
DATE([Year], ([Quarter] * 3) - 2, 1)
```

This enables:

- Trend analysis  
- Forecasting  
- Quarterly comparisons  
- Year-over-year growth  

# 📊 Forecasting & Growth Analysis

Forecasting is implemented using:

- Power BI built-in forecasting  
- Time-based modeling using Transaction Date  
- Decomposition Tree for root cause analysis  

# 🧩 Modeling Notes

The data model follows a Star Schema design:

### Fact Tables
- Aggregated Transactions  
- Aggregated Users  
- District-Level Transactions  

### Dimension Tables
- State  
- District  
- Year  
- Quarter  

The model is optimized for:

- Cross-filtering  
- Drill-down analysis  
- Geographic visualization  
- Growth forecasting  
- Root cause exploration  

# 📝 Summary

The DAX layer enables:

- Transaction value analysis  
- Time-series modeling  
- Forecast-driven projections  
- Root cause diagnostics  

This completes the analytical layer of the PhonePe Pulse 360 dashboard.