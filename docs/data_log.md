# Data Log

## Purpose
This file documents every dataset used in this project — where it came from, when it was downloaded, and how it is stored locally.

| Date Downloaded | Source | Series Name | Series ID | URL | File Saved As | Date Range | Frequency | Notes |
|---|---|---|---|---|---|---|---|---|
| 2025-03-15 | FRED | US Unemployment Rate | UNRATE | https://fred.stlouisfed.org/series/UNRATE | data/raw/unemployment.csv | Jan 2015 - Sep 2025 | Monthly | Removed Oct 2025 row due to missing value |
| 2025-03-15 | FRED | US CPI Inflation Rate | CPALTT01USM657N | https://fred.stlouisfed.org/series/CPALTT01USM657N | data/raw/inflation.csv | Jan 2015 - Sep 2025 | Monthly | OECD measure, year over year percent change |

## Processed Data
| File | Description | Created From | Date Created |
|---|---|---|---|
| data/processed/merged_data.csv | Merged unemployment and inflation by date | unemployment.csv + inflation.csv | 2025-03-15 |
| data/processed/unemployment_rate.csv | Cleaned unemployment data | unemployment.csv | 2025-03-15 |
| data/processed/inflation_rate.csv | Cleaned inflation data | inflation.csv | 2025-03-15 |
