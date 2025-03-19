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

- **Media Mix Optimization Report.pdf**: Executive summary and detailed findings for business users
- **MMM Analysis.pdf**: Technical analysis with full implementation details and methodology
- **MMM DataGenerator.pdf**: Documentation of the data generation process
- **notebooks/**: Directory containing all Jupyter notebooks
  - **Media Mix Optimization Report.ipynb**: Business-focused report with insights and recommendations
  - **MMM Analysis.ipynb**: Core analytical notebook with model development and optimization
  - **MMM DataGenerator.ipynb**: Utility notebook for generating the simulated marketing data
- **data/**: Contains the dataset used in the analysis
  - **MMM_data.csv**: Simulated marketing data with channel spend and sales
- **images/**: Visualizations used in the report and analysis

## Key Findings

Our analysis revealed several critical insights:

- **Current marketing budget is significantly overallocated** - All channels are operating beyond their efficiency thresholds, resulting in suboptimal returns
- **Two viable optimization strategies** were identified:
  - **ROI Optimization**: Reduces budget by 60% (from $50,375 to $20,150 monthly) while increasing ROI by 113% (from 3.11 to 6.63)
  - **Sales Maximization**: Maintains current budget while increasing sales by 18.6% (an additional $350,631 annually)
- **Channel performance varies dramatically**:
  - **TV and Digital** show positive ROI but operate far beyond their efficiency thresholds
  - **Print** demonstrates surprisingly strong long-term impact due to high carryover effects
  - **Radio** consistently underperforms and should be significantly reduced or eliminated

## Technical Approach

The modeling methodology includes several sophisticated techniques:

1. **Adstock Modeling**: We implemented channel-specific decay rates to capture carryover effects:
   - TV: λ=0.60 (moderate persistence)
   - Digital: λ=0.20 (short-lived effects)
   - Print: λ=0.80 (strong persistence)
   - Radio: λ=0.50 (moderate persistence)

2. **Diminishing Returns**: We used Hill transformations with optimized parameters to model non-linear response curves:
   - Each channel shows a unique diminishing returns pattern
   - Parameters were optimized using Ridge regression with cross-validation

3. **Background Variables**: The model incorporates external factors:
   - Seasonal events (e.g., Christmas adds $14,564 to sales)
   - Economic conditions (growth periods boost sales by $3,761)
   - Long-term trends

4. **Budget Optimization**: We developed two distinct allocation strategies:
   - ROI Optimization focuses on efficiency, using only 40% of the current budget
   - Sales Maximization prioritizes total impact, reallocating the full budget

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
   1. MMM DataGenerator.ipynb (if you need to generate fresh sample data)
   2. MMM Analysis.ipynb (to run the technical analysis)
   3. Media Mix Optimization Report.ipynb (to view the business findings)

## Visualizations

The analysis includes numerous visualizations to illustrate marketing dynamics:
- Channel response curves showing diminishing returns
- Adstock patterns demonstrating carryover effects
- Budget allocation comparisons across optimization scenarios
- ROI vs. sales impact tradeoff analysis
