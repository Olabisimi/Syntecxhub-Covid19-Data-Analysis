# Syntecxhub-Covid19-Data-Analysis
Nigeria COVID-19 Data Analysis: Daily &amp; weekly cases, rolling averages, peak detection, and reproduction trends by region with visualizations.

# Project Description
This project analyzes COVID-19 trends in Nigeria using regional daily and cumulative data. The analysis includes:
Cleaning and preprocessing the dataset
Computing daily and weekly new cases per region
Generating rolling averages to smooth trends
Detecting peak daily and weekly cases
Estimating approximate reproduction number (Rt) per region
Producing visualizations and exporting data for reporting
The goal is to provide a clear overview of COVID-19 dynamics in Nigeria and insights into which regions experienced the highest spikes.

# Dataset and Column Definitions
Original columns before cleaning:
Column Name
Description
ID
Unique row identifier
DATE
Date of report
ISO_3
3-letter country code
PAYS
Country name
ID_PAYS
Country numeric ID
REGION
Region name
ID_REGION
Region numeric ID
CONTAMINES
Cumulative confirmed COVID-19 cases
DECES
Cumulative deaths
GUERIS
Cumulative recoveries
CONTAMINES_FEMME
Cumulative cases in females
CONTAMINES_HOMME
Cumulative cases in males
CONTAMINES_GENRE_NON_SPECIFIE
Cases with unspecified gender
SOURCE
Data source

Note: During cleaning, irrelevant columns (ID, ISO_3, PAYS, ID_PAYS, SOURCE) were removed. Negative and placeholder values (-1) were replaced appropriately. Cumulative columns were forward-filled by region, and data types standardized.

# Analysis Summary
Regions analyzed: 170–207 per dataset
Daily Cases: Computed from cumulative counts using day-to-day differences
Weekly Cases: Computed as the sum of daily cases per week (weeks ending Monday)
Rolling averages: 7-day rolling for daily cases; 4-week rolling for weekly cases
Peaks detected: Both daily and weekly peaks identified per region
Approximate Reproduction Number (Rt): Calculated as daily cases divided by cases 7 days prior, clipped to a maximum of 10

# Insights:
Peak daily and weekly cases varied across regions, reflecting local outbreaks
Rolling averages smooth out noise and reveal trends more clearly
Rt approximation highlights periods of faster transmission

# Visualizations
Plot
Description
plots/daily_cases_per_region.png
Daily COVID-19 cases by region
plots/rolling_daily_cases_per_region.png
7-day rolling average of daily cases
plots/weekly_cases_per_region.png
Weekly COVID-19 cases by region

# CSV Exports
File
Description
nigeria_covid_daily_cases_full.csv
Daily cases dataset with rolling averages and Rt
nigeria_covid_weekly_cases.csv
Weekly cases per region with rolling averages
nigeria_covid_peak_daily.csv
Peak daily cases per region
nigeria_covid_peak_weekly.csv
Peak weekly cases per region
nigeria_covid_summary.txt
Brief textual summary of findings
