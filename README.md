# Retail-Sales-Analysis-and-Forecasting
## Dataset
Use the UCI Online Retail dataset: https://archive.ics.uci.edu/dataset/352/online+retail  
Citation: Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33  
License: CC BY 4.0.

The UCI record describes 541,909 transaction lines from a UK-based online retailer between 1 December 2010 and 9 December 2011. Download `Online Retail.xlsx` from the source page and place it in this folder.

```

## Outputs
The script creates an `outputs/` folder with:
- data_quality_summary
- kpis
- monthly_sales and weekly_sales
- top_countries and top_products_by_line_value in sales
- forecast_model_comparison
- next_4_week_forecast.csv
- charts as PNG files


## Method choices
- Main sales measure is `Quantity * UnitPrice` for positive quantities/prices on invoices not marked as cancellations.
- This is an analysis proxy for positive invoice-line value, not finance-certified net sales. Analyze cancellations/returns separately for accounting.
- Forecasting uses weekly aggregates, lag and calendar features, a Random Forest regressor, and two baselines. The final weeks are held out chronologically.
- Because the dataset spans only about one year, seasonal extrapolation is uncertain. Forecasts are not guarantees.

## Evidence standard
The report template states only dataset facts available from the UCI documentation. Run the script to generate measured project-specific KPIs and forecast errors. Insert the run-specific outputs into the Word report before submission. Do not claim results from code that has not been executed.
