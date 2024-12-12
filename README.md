# Spatio-Temporal Epidemiology of Chickenpox in Hungary

This repository contains an analysis of the spatio-temporal patterns of chickenpox cases in Hungary from 2005 to 2015. The analysis explores both temporal and spatial aspects of chickenpox outbreaks across Hungary’s 20 counties, and investigates factors like seasonality, trends, and autocorrelation. 

The analysis was performed using **R** and documented through **RMarkdown**. The final outputs include HTML reports, interactive visualizations, and statistical analysis of chickenpox case data.

## Table of Contents

- [Introduction](#introduction)
- [Data Preparation](#data-preparation)
- [National Trends](#national-trends)
- [Seasonality Analysis](#seasonality-analysis)
- [Interactive County-Level Comparison](#interactive-county-level-comparison-large-display)
- [Temporal Autocorrelation Analysis](#temporal-autocorrelation-analysis)
- [Spatial Autocorrelation Analysis](#spatial-autocorrelation-analysis)
- [Weekly Heatmap of Chickenpox Cases by County (2005-2015)](#weekly-heatmap-of-chickenpox-cases-by-county-2005-2015)
- [Monthly Heatmap of Chickenpox Cases by County](#monthly-heatmap-of-chickenpox-cases-by-county)
- [Conclusion](#conclusion)

## Introduction

This report investigates the spatio-temporal patterns of chickenpox cases in Hungary over a period of 10 years. The analysis is based on weekly data for each of Hungary's 20 counties, covering the period from 2005 to 2015. The primary objectives of this project are:

1. To explore long-term trends in chickenpox cases at the national and county levels.
2. To analyze intra-annual seasonality of chickenpox cases.
3. To compare trends across counties.
4. To investigate temporal and spatial autocorrelation in chickenpox cases.

The analysis was performed using **R** and documented with **RMarkdown**, with output in **HTML**.

## Data Preparation

Data for this analysis comes from two key datasets:

1. **Chickenpox Case Data** (`hungary_chickenpox.csv`): Contains weekly reported chickenpox cases for each county.
2. **County Adjacency Data** (`hungary_county_edges.csv`): Contains spatial relationships between counties for spatial autocorrelation analysis.

Both datasets are loaded and cleaned for analysis, with necessary transformations performed to ensure the data is in the correct format for time series analysis.

## National Trends

The **National Trend** section summarizes chickenpox cases across Hungary by aggregating data from all counties. A line plot is generated to visualize the overall national trend from 2005 to 2015.

## Seasonality Analysis

The **Seasonality Analysis** examines the fluctuation of chickenpox cases over the course of the year. A bar plot visualizes the total number of cases per month to reveal any seasonal patterns, which can inform vaccination timing and public health strategies.

## Interactive County-Level Comparison (Large Display)

This section provides an **interactive plot** comparing chickenpox cases across all counties. Users can isolate specific counties by clicking on the legend or hover over data points for detailed information.

## Temporal Autocorrelation Analysis

The **Temporal Autocorrelation Analysis** computes the autocorrelation function (ACF) for chickenpox cases in a selected county. This analysis helps identify patterns of persistence or seasonality over time.

## Spatial Autocorrelation Analysis

In this section, **Moran’s I test** is applied to analyze the spatial autocorrelation of chickenpox cases. The spatial adjacency matrix is used to assess whether chickenpox cases in one county are correlated with those in neighboring counties.

## Weekly Heatmap of Chickenpox Cases by County (2005-2015)

This section generates a **heatmap** showing the weekly distribution of chickenpox cases for each of Hungary’s counties. This visualization helps identify high-risk periods and regions with recurring outbreaks.

## Monthly Heatmap of Chickenpox Cases by County

A **monthly heatmap** is created to show the total chickenpox cases for each month and year, with a separate plot for each county. This helps to visualize intra-annual seasonality, revealing months with the highest disease burden.

## Conclusion

This analysis sheds light on the spatio-temporal dynamics of chickenpox in Hungary over a 10-year period. Key findings include clear seasonal trends, county-level variations in outbreaks, and significant spatial and temporal autocorrelation. These insights can guide public health interventions, such as targeted vaccination campaigns, to reduce chickenpox outbreaks.

## How to Run the Analysis

To replicate the analysis, clone the repository and run the **RMarkdown** file in an R environment with the necessary packages. You can use **RStudio** for an interactive experience.

### Prerequisites

- R version 4.4.1 or later
- Required R packages: `tidyverse`, `lubridate`, `sf`, `spdep`, `forecast`, `plotly`, `shiny`, `RColorBrewer`, `ggplot2`

### Running the Analysis

1. Clone the repository:
   ```bash
   git clone https://github.com/ChaimaeBinjach/Chickenpox-Analysis.git
   ```

2. Open the **Chickenpox_annalysis.Rmd** file in **RStudio**.

3. Install the required R packages (if not already installed):
   ```r
   install.packages(c("tidyverse", "lubridate", "sf", "spdep", "forecast", "plotly", "shiny", "RColorBrewer"))
   ```

4. Knit the **RMarkdown** file to generate the HTML report:
   In RStudio, click on the "Knit" button at the top of the **RMarkdown** file.

