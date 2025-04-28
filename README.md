# Generalised Linear Model (GLM) Project - Fertility Analysis

## Overview
- Analysed the relationship between number of children per woman and factors: **years married (duration)**, **residence location**, and **education level**.
- Fitted a **Poisson regression model** accounting for varying numbers of mothers using a **rate model with an offset**.
- Conducted model selection using **stepwise AIC**, **overdispersion checks**, and **diagnostic analysis** to assess model fit and influential points.

## Steps
- **Data Cleaning**: Converted categorical variables (`duration`, `residence`, `education`) into ordered factors.
- **Exploratory Analysis**:  
  - Visualised mean and log-mean number of children across predictors.
  - Created interaction plots to assess potential two-way interactions.
- **Model Fitting**:  
  - Fitted a Poisson GLM including main effects and interactions.
  - Performed **AIC stepwise selection** to find a parsimonious model.
- **Model Checking**:  
  - Verified model adequacy using deviance tests and estimated dispersion parameter (φ̂).
  - Diagnosed residuals, leverage, Cook’s distance, and jackknife residuals.
- **Influence Analysis**:  
  - Identified and removed an influential point (case 57).
  - Refitted model and rechecked diagnostics and overdispersion.
- **Interpretation**:  
  - Longer marriage duration increases children but at a declining rate.
  - Urban and rural families have more children compared to Suva families.
  - Higher education (secondary+) significantly lowers fertility rates.

## Key Methods Used
- **Poisson GLM** with log link and offset
- **Stepwise AIC selection**
- **Deviance tests and overdispersion check (φ̂)**
- **Influential point diagnostics (Cook’s distance, leverage, jackknife residuals)**

## Outcome
- Final model confirmed that **duration**, **residence**, and **education** significantly influence the number of children per woman, with good model fit and no evidence of overdispersion after accounting for outliers.
