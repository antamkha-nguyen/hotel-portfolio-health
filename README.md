# Hotel Portfolio Analysis

A brand health analytics project analyzing cancellation risk and revenue performance across hotel types and market segments.

## Business Questions

1. Which hotel type has a higher cancellation risk?
2. Are there seasonal patterns in cancellation rates?
3. Which market segments drive the most cancellations?
4. How does ADR vary by hotel type and season?
5. Which months and segments need the most brand health attention?

## Project Structure
```
hotel_portfolio_analysis/
├── portfolio_health_dashboard.twb   # Tableau dashboard
├── hotel_portfolio_analysis.ipynb   # Python analysis notebook
├── hotel_month_metrics.xlsx         # Aggregated monthly metrics
├── hotel_month_segment.xlsx         # Aggregated segment metrics
└── data/
    └── hotel_bookings.xlsx          # Source data (119K+ bookings)
```
## Dataset

- Source: Hotel booking demand dataset from Kaggle ([Dataset Link](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand))
- Records: ~119K hotel bookings
- Hotels: City Hotel, Resort Hotel
- Key fields: cancellation status, ADR, market segment, arrival month

## Analysis Overview

**Python (Jupyter Notebook)**
- Cleaned and filtered booking data
- Calculated cancellation rate and average ADR per hotel, month, and segment
- Exported aggregated metrics to Excel

**Excel**
- PivotTable validation of monthly cancellation rates by hotel type
- Cross-check against Python outputs
- Created a `Risk Flag` field with a nested `IF` formula to label segments:
  - High Risk if cancellation rate > 40%
  - Watch if cancellation rate between 20 percent and 40 percent
  - OK if cancellation rate <= 20%

**Tableau Dashboard: Hotel Portfolio Health Monitor**
([Dashboard Link](https://public.tableau.com/app/profile/an.tam.kha.nguyen.2002/viz/HotelPortfolioHealthMonitorCancellationRevenueAnalysis/HotelPortfolioHealthMonitor))
- Cancellation Trend: monthly cancellation rate vs 40% risk threshold
- ADR Trend: average daily rate by hotel type across months
- Cancellation Risk by Segment: market segments colored by risk level
- Filters: Hotel type, Year

## Key Findings

- City Hotel exceeds 40% cancellation risk threshold most of the year
- Resort Hotel shows strong ADR seasonality, peaking at ~$185 in August
- Groups and Offline TA/TO are the highest-risk booking segments
- November is the lowest-risk month across both hotel types

## Tools Used

- Python (pandas)
- Microsoft Excel
- Tableau Public

<img width="1233" height="829" alt="Dashboard Image" src="https://github.com/user-attachments/assets/5cef2390-2f1e-408d-8f86-a744b2a28a19" />

