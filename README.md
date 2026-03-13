# Hotel Booking Performance Dashboard (2015–2017) | Power BI

## Overview
This project analyzes hotel booking performance data (2015–2017) to compare **City Hotel** vs **Resort Hotel** across key commercial and operational metrics. The dashboard highlights revenue performance, booking volume trends, cancellation behavior, average daily rate (ADR), length of stay, and estimated revenue impact from cancellations.

## Business Questions
- Which hotel type generates higher revenue and booking volume?
- How do bookings and revenue change month-by-month (seasonality)?
- How do cancellation levels differ between City and Resort hotels?
- What is the overall cancellation rate and its revenue impact?
- How does average length of stay differ by hotel type?

## Key KPIs (Dashboard Metrics)
- **Total Revenue:** 42.72M  
- **Total Bookings:** 119K  
- **Total Nights:** 409K  
- **Average ADR:** 102.44  
- **Cancellation Rate:** 37.24%  
- **Estimated Lost Revenue (Cancellations):**
  - City Hotel: 10.9M
  - Resort Hotel: 5.8M

## Key Insights (Summary)
- **City Hotel** generates higher total revenue than Resort Hotel (≈25M vs ≈17M).
- Booking and revenue patterns show strong **seasonality**, with a peak around **August**.
- **Cancellations are material** (37.24%), with higher cancellation volume in City Hotel.
- Estimated lost revenue due to cancellations is significant, especially for City Hotel (10.9M).
- **Resort Hotel** has a longer average length of stay (4.36 nights) compared to City Hotel (2.99 nights).

## Data Preparation (Power Query)
The dataset was cleaned and transformed in **Power Query**, including:
- Creating a **Date** column (Year + Month + Day) for time-series analysis
- Converting Month name text to a proper date format
- Creating calculated fields:
  - **Total Nights** = stays_in_weekend_nights + stays_in_week_nights
  - **Revenue** = Total Nights * ADR
- Ensuring correct data types for accurate calculations (Date, Decimal, Whole Number)

## DAX Measures (Examples)
Key measures used in the dashboard:
- **Total Revenue** = SUM(Revenue)
- **Total Bookings** = COUNTROWS(Table)
- **Total Nights** = SUM(Total Nights)
- **Average ADR** = AVERAGE(ADR)
- **Cancellation Rate** = Cancelled Bookings / Total Bookings (formatted as %)

## Tools Used
- **Power BI** (Data modeling, DAX measures, interactive dashboard)
- **Power Query** (Data cleaning, transformations, calculated columns)
