# Syntecxhub-Covid19-Data-Analysis
Nigeria COVID-19 Data Analysis: Daily &amp; weekly cases, rolling averages, peak detection, and reproduction trends by region with visualizations.

# Nigeria COVID-19 Data Analysis

## Project Description

This project analyzes COVID-19 trends in Nigeria using regional daily and cumulative data. The analysis includes:

- Cleaning and preprocessing the dataset  
- Computing **daily and weekly new cases** per region  
- Generating **rolling averages** to smooth trends  
- Detecting **peak daily and weekly cases**  
- Estimating **approximate reproduction number (Rt)** per region  
- Producing visualizations and exporting data for reporting  


## Dataset Column Definitions

| Column Name                     | Description                                                   |
|---------------------------------|---------------------------------------------------------------|
| ID                               | Unique row identifier                                         |
| DATE                             | Date of report                                                |
| ISO_3                            | 3-letter country code                                         |
| PAYS                             | Country name                                                  |
| ID_PAYS                          | Country numeric ID                                            |
| REGION                           | Region name                                                   |
| ID_REGION                        | Region numeric ID                                             |
| CONTAMINES                        | Cumulative confirmed COVID-19 cases                           |
| DECES                             | Cumulative deaths                                             |
| GUERIS                            | Cumulative recoveries                                         |
| CONTAMINES_FEMME                   | Cumulative cases in females                                   |
| CONTAMINES_HOMME                   | Cumulative cases in males                                     |
| CONTAMINES_GENRE_NON_SPECIFIE      | Cases with unspecified gender                                  |
| SOURCE                             | Data source                                                   |

**Note:** During cleaning, irrelevant columns (ID, ISO_3, PAYS, ID_PAYS, SOURCE) were removed. Negative values (-1) were replaced with NaN where appropriate. Daily, weekly, and rolling averages were computed per region.


## Analysis Summary

- **Regions analyzed:** 170–207 per dataset  
- **Daily Cases:** Computed from cumulative counts using day-to-day differences  
- **Weekly Cases:** Computed as sum of daily cases per week (weeks ending Monday)  
- **Rolling averages:** 7-day rolling for daily cases; 4-week rolling for weekly cases  
- **Peaks detected:** Both daily and weekly peaks identified per region  
- **Approximate Reproduction Number (Rt):** Calculated as daily cases divided by cases 7 days prior  
- **Insights:**
  - Peak daily and weekly cases vary across regions, reflecting local outbreaks  
  - Rolling averages smooth out noise and reveal trends  
  - Rt approximation highlights periods of faster transmission  


## Plots

| Plot | Description |
|------|-------------|
| `plots/daily_cases_per_region.png` | Daily COVID-19 cases by region |
| `plots/rolling_daily_cases_per_region.png` | 7-day rolling average of daily cases |
| `plots/weekly_cases_per_region.png` | Weekly COVID-19 cases by region |



## CSV Exports

| File | Description |
|------|-------------|
| `nigeria_covid_cleaned.csv` | Original cleaned dataset |
| `nigeria_covid_daily_cases_full.csv` | Daily cases dataset with rolling averages and Rt |
| `nigeria_covid_weekly_cases.csv` | Weekly cases per region with rolling averages |
| `nigeria_covid_peak_daily.csv` | Peak daily cases per region |
| `nigeria_covid_peak_weekly.csv` | Peak weekly cases per region |
| `nigeria_covid_summary.txt` | Brief textual summary of findings |



## Usage

1. Clone the repository:

bash
git clone https://github.com/Olabisimi/nigeria-covid-analysis.git

2. Open the notebook to explore:
Bash
jupyter notebook notebooks/nigeria_covid_analysis.ipynb

3. All cleaned datasets and plots are stored in the repo under the plots/ folder and CSV files.
   
# Requirements
Python 3.x
Pandas
NumPy
Matplotlib
Seaborn
Install required packages via:
Bash
pip install pandas numpy matplotlib seaborn
