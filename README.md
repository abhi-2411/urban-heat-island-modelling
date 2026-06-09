# Chennai Urban Heat Island Analysis

This project explores Urban Heat Island (UHI) patterns in Chennai and surrounding districts using satellite-derived Land Surface Temperature (LST) data from Summer 2023 and Post-Monsoon 2023.

The goal was not just to predict temperature, but to understand which environmental factors drive heat across different seasons and landscapes.

## Overview

The study uses a regime-based approach by separating pixels into urban and rural regions and training independent machine learning models for each group.

Features used include:

* Built-up density
* NDVI (vegetation index)
* MNDWI (water index)
* Elevation
* ESA Land Use / Land Cover classes

Land Surface Temperature (LST) serves as the target variable.

## Methodology

* Landsat-derived LST data collected for two seasons
* Dataset cleaned and filtered for valid observations
* Urban and rural regimes created using built-up density thresholds
* Linear Regression and Random Forest models trained separately
* Spatial block cross-validation used to reduce spatial leakage
* SHAP applied to interpret feature contributions

## Key Findings

* Vegetation (NDVI) was the strongest cooling factor across most scenarios.
* Water-related effects (MNDWI) became much more influential in urban areas during the post-monsoon season.
* Elevation emerged as a major driver of temperature variation in rural post-monsoon conditions.
* Urban and rural regions showed noticeably different thermal behaviour despite similar overall model accuracy.

## Technologies

* Python
* Google Earth Engine
* Scikit-learn
* SHAP
* Pandas
* NumPy
* Matplotlib

## Outcome

The project demonstrates that thermal drivers are not uniform across a city. By separating urban and rural environments and examining seasonal differences, the analysis provides a clearer understanding of how vegetation, water, built-up density, and terrain influence surface temperatures.
