# Media Mix Modeling (MMM) Analysis

A comprehensive marketing budget optimization framework using Media Mix Modeling to quantify channel effectiveness and maximize ROI.

This repository contains a complete media mix modeling analysis for optimizing marketing budget allocation across multiple channels. The analysis demonstrates how to build a sophisticated marketing attribution model that accounts for diminishing returns, adstock effects, and external factors. The data used in this analysis is simulated using the functions in the MMM DataGenerator notebook to provide a realistic but controlled marketing dataset.

## What is Media Mix Modeling?

Media Mix Modeling (MMM) is a statistical analysis technique used by marketers to measure the impact of various marketing activities on sales or conversions. Unlike attribution models that focus on individual customer journeys, MMM takes a top-down approach by analyzing aggregate data over time to determine how different marketing channels contribute to overall business outcomes. 

This approach is particularly valuable for:
- Quantifying the effectiveness of both online and offline marketing channels
- Accounting for external factors like seasonality, economic conditions, and competitive activity
- Measuring the true incremental impact of marketing spend
- Optimizing budget allocation across channels to maximize ROI or total sales

## Repository Contents

- **Media Mix Optimization Report.pdf**: Executive summary and detailed findings in PDF format (accessible without running code)
- **MMM Analysis.html**: Static HTML version of the analysis notebook (accessible without running code)
- **MMM DataGenerator.html**: Static HTML version of the data generating notebook (accessible without running code)
- **notebooks/Media Mix Optimization Report.ipynb**: Executive summary and detailed findings as a Jupyter notebook
- **notebooks/MMM Analysis.ipynb**: The core analytical notebook containing all modeling steps and implementation
- **notebooks/MMM DataGenerator.ipynb**: Utility notebook for generating the simulated marketing data used in the analysis

## Project Overview

This project implements a comprehensive media mix modeling approach to:

1. Quantify the impact of marketing spend across TV, Digital, Radio, and Print channels
2. Account for carryover effects (adstock) in each channel
3. Model diminishing returns using Hill transformations
4. Incorporate external factors like seasonality and economic conditions
5. Optimize budget allocation to maximize either ROI or total sales impact

## Key Findings

- All marketing channels are currently operating beyond their optimal efficiency points
- Significant opportunity exists to improve marketing ROI by reallocating budget
- Two optimization strategies were developed:
  - ROI Maximization: Reduces budget by 60% while increasing efficiency by 113%
  - Sales Maximization: Maintains current budget while increasing impact by 18.6%
- Digital and TV are the most effective channels, though both are currently overfunded

## Technical Approach

The modeling methodology includes:

1. **Exploratory Data Analysis**: Examining historical spend patterns and sales trends
2. **Adstock Modeling**: Capturing carryover effects with channel-specific decay rates
3. **Diminishing Returns**: Implementing Hill transformations with optimized parameters
4. **Ridge Regression**: Using regularized regression to handle collinearity
5. **Cross-Validation**: Employing time series cross-validation for robust parameter estimation

## Getting Started

To run these notebooks:

1. Clone this repository
2. Ensure you have Jupyter and the following dependencies installed:
   - numpy
   - pandas 
   - matplotlib
   - statsmodels
   - scikit-learn
   - seaborn
   - scipy
3. Execute the notebooks in the following order:
   1. MMM DataGenerator.ipynb (if you need to generate sample data)
   2. MMM Analysis.ipynb
   3. Media Mix Optimization Report.ipynb

## Visualizations

The analysis includes numerous visualizations to illustrate marketing dynamics:
- Channel response curves showing diminishing returns
- Adstock patterns demonstrating carryover effects
- Budget allocation comparisons across optimization scenarios
- ROI vs. sales impact tradeoff analysis
