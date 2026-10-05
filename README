# Solar Energy Production Zones — Clustering Project

Unsupervised machine learning project that clusters solar project locations across New York State into High, Medium, and Low energy production zones, to help identify priority areas for sales and marketing.

🗺️ **[View Interactive Map](your-github-pages-link-here)**

## Overview

A solar power developer wanted to know which areas have the strongest solar energy output, to focus expansion efforts. This project groups individual solar project locations into energy zones using clustering, based on system size, energy production, and project count.

## Approach

- **Data cleaning**: handled missing values, duplicate Project IDs, inconsistent date formats, and other data quality issues on a statewide dataset of solar projects.
- **Feature engineering**: aggregated individual projects into 2,500 unique locations (by County, City/Town, ZIP), added coordinates via ZIP code lookup.
- **Dimensionality reduction**: the core features (energy, kWac, kWdc) were highly correlated, so PCA was used to reduce them to 2 components while keeping 100% of the variance.
- **Choosing K**: compared Elbow, Silhouette, Davies-Bouldin, and Calinski-Harabasz methods. The metrics favored K=2, but that only separates "big vs small," so K=3 was chosen manually to match the business need for High/Medium/Low zones, backed by a silhouette comparison across K=3-5 and a stability check across multiple random seeds.
- **Model comparison**: tested K-Means, DBSCAN, Hierarchical Clustering, and Gaussian Mixture Models. K-Means performed best across all 3 evaluation metrics.
- **Cluster analysis**: labeled and analyzed the 3 resulting zones, and identified the specific top-performing counties and locations in each.
- **Interactive map**: built with Folium, showing all locations colored by zone, with a heatmap layer and clickable location details.

## Key Findings

- **High Energy Zone**: 765 locations, averaging 7.49M kWh/yr, accounts for the large majority of total production.
- **Medium Energy Zone**: 884 locations, averaging 444K kWh/yr.
- **Low Energy Zone**: 851 locations, averaging 25K kWh/yr.
- Battery storage adoption is highest in the High zone (64%), suggesting it's concentrated in larger, more established installations rather than filling gaps elsewhere.

## Limitations

This clustering is based on system size, energy output, and project count. It doesn't include solar irradiance or installation cost data, which would better reflect a location's true solar potential, that data wasn't accessible in this environment, and is a natural next step for this project.

## Tools Used

Python, pandas, NumPy, scikit-learn, matplotlib, seaborn, Folium, scipy

## Dataset

Statewide solar project records (New York State), including project location, system size, and estimated energy production. The raw dataset is not included in this repository.