# Phillips Curve Analysis: Pre and Post COVID (2015–2025)

## Overview
This project examines whether the traditional Phillips Curve relationship 
between unemployment and inflation held in the United States before and 
after the COVID-19 pandemic using publicly available data from the Federal 
Reserve (FRED).

## Question
Did the relationship between unemployment and inflation change after COVID?

## Data
- **Unemployment Rate**: FRED series UNRATE, monthly, 2015–2025
- **Inflation Rate**: FRED series CPALTT01USM657N, monthly, 2015–2025

## Methods
- Data cleaning and merging in R
- Time series visualization
- OLS regression split by pre-COVID (before March 2020) and 
  post-COVID (June 2020 onward)

## Key Findings
- The simple Phillips Curve showed no statistically significant 
  relationship in either period
- Pre-COVID R-squared: 0.004, p-value: 0.635
- Post-COVID R-squared: ~0, p-value: 0.98
- Results suggest inflation is driven by more than unemployment alone, 
  consistent with post-COVID supply chain disruptions and fiscal stimulus

## Tools
R, Quarto, ggplot2

## Data Source
Federal Reserve Bank of St. Louis (FRED) — fred.stlouisfed.org
