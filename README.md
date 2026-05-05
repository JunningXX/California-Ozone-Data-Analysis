# 🌫️ California Ozone Concentration Analysis (2024)

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458.svg)
![Plotly](https://img.shields.io/badge/Plotly-Interactive_Viz-3F4F75.svg)
![Quarto](https://img.shields.io/badge/Quarto-Scientific_Publishing-447099.svg)

## 📌 Project Overview
Ground-level ozone is a severe respiratory irritant and a highly seasonal secondary pollutant. This project performs an end-to-end **Exploratory Data Analysis (EDA)** on 54,750 daily ozone observations across 160 monitoring sites in California during 2024. 

Beyond standard spatial-temporal trend analysis, this project critically evaluates data integrity by comparing two distinct sources: the EPA's rigorously validated historical record (**AQS**) and real-time, uncalibrated sensor data (**AirNow**).

## 🚀 Key Insights
1. **The "Mountain Trap" Effect (Geospatial Analysis):** The highest ozone hazards do not stay in the urban centers where the precursor emissions (NOx/VOCs) are generated. Prevailing winds blow emissions inland, trapping them against high-altitude areas (e.g., Sequoia & Kings Canyon National Parks), which record the state's highest concentrations.
2. **The "Weekend Effect":** Despite a massive drop in heavy commuter traffic on weekends, baseline ozone levels remain statistically identical to weekdays (0.043 ppm). This highlights complex atmospheric chemistry: without fresh NOx emissions from weekend traffic to "scavenge" existing ozone, pollution levels persist.
3. **Data Quality & Reporting Biases:** Comparing the two data sources revealed severe spatial biases. Relying purely on real-time AirNow data results in underestimating peak extreme events (0.058 ppm vs AQS's 0.061 ppm) and introduces "False Clean" anomalies caused by uncorrected sensor failures in highly polluted urban areas.

## 🛠️ Data Science Skills Demonstrated
* **Advanced Data Cleaning:** * Reconstructed misaligned and malformed calendar dates using programmatic row-offset logic to prevent cross-site data bleeding.
  * Addressed 5% missing data in the target variable using **rolling 5-day historical means** grouped by individual monitoring sites.
  * Flattened complex MultiIndex dataframes resulting from multi-variable aggregations.
* **Interactive Data Visualization:** Designed publication-ready, interactive charts using `Plotly Graph Objects` and `Plotly Express` (Bar charts, Subplots with shared axes, Time-series).
* **Geospatial Mapping:** Built interactive choropleth and scatter mapbox visualizations mapping localized concentrations to California county boundaries using FIPS codes.
* **Reproducible Reporting:** Authored the final analysis utilizing **Quarto (`.qmd`)**, featuring responsive multi-column layouts, tabset panels, and custom HTML/CSS styling.
