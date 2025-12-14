# British Airways Customer Review Analysis 

## Project Overview

This Tableau project provides a comprehensive analysis of **British Airways customer reviews** spanning from **2016 to 2023**. The interactive dashboard is designed to monitor airline performance across key service touchpoints, helping stakeholders identify areas for improvement in passenger satisfaction.

By visualizing sentiment data, the dashboard enables deep-dives into specific metrics such as **Cabin Staff Service**, **Entertainment**, and **Seat Comfort**, while also offering granular views by aircraft type, traveler type, and geographic region.

## Data Sources

The project utilizes two primary datasets:

1.  **`ba_reviews.csv`**: Contains **1,324 customer reviews** with the following key attributes:
    * **Qualitative Data:** Review text, headers, and recommendations.
    * **Quantitative Ratings (1-5):** *Overall Rating, Seat Comfort, Cabin Staff Service, Food & Beverages, Ground Service, Value for Money,* and *Entertainment*.
    * **Flight Details:** Aircraft model (`aircraft`), Route, Seat Type (`Economy`, `Business`, `First`), and Date Flown.
2.  **`Countries.csv`**: A lookup table containing **Country Names, Codes, Continents, and Regions**. This dataset is joined with the review data to map reviewer locations to continents for geospatial analysis.

## Dashboard Features

The dashboard is composed of several interactive visualizations:

### 1. Dynamic KPI Scorecard
* **Top Banner:** Displays the overall average rating (4.2) alongside specific service metrics:
    * Cabin Staff Service (3.3)
    * Entertainment (1.4)
    * Food & Beverages (2.4)
    * Ground Service (3.0)
    * Seat Comfort (2.9)
    * Value For Money (2.8)

### 2. Temporal Analysis
* **Line Chart:** "Average [Metric] by Month" tracks the selected performance metric over time (2016–2023), allowing users to spot trends, seasonality, or sharp declines in service quality.

### 3. Geospatial Intelligence
* **Interactive Map:** "Average [Metric] by Country" visualizes global sentiment, highlighting which regions report higher or lower satisfaction levels.

### 4. Fleet Performance
* **Dual-Axis Bar Chart:** "Average [Metric] Rating by Aircraft" compares:
    * **Average Rating (Blue Bars):** Satisfaction level for specific aircraft (e.g., Boeing 777, A380).
    * **Number of Reviews (Red Bars):** The volume of feedback, providing statistical context to the ratings.

## Interactivity & Filters

The dashboard includes a robust control panel on the left sidebar:

* **"Pick a Metric":** A parameter control that dynamically updates **all charts** to focus on a specific KPI (e.g., switching the view from *Cabin Staff Service* to *Food*).
* **Global Filters:**
    * **Continent:** Filter data by specific global regions.
    * **Aircraft (Group):** Analyze specific fleets.
    * **Month of Date:** Time-slider to narrow down the analysis period (e.g., March 2016 – Oct 2023).
    * **Seat Type:** Toggle between *Business Class, Economy Class, First Class*, etc.
    * **Traveller Type:** Filter by *Business, Couple Leisure, Family Leisure*, etc.
