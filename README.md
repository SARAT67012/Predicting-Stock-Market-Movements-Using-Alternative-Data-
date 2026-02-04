# Predicting Stock Market Movements  
### A WorldQuant University Group Project (MSc in Financial Engineering)

---

## Project Overview

This group project was completed as part of the **MSc in Financial Engineering (MScFE)**
program at **WorldQuant University**, under the course **Financial Data (M6)**.

The project critically evaluates and partially replicates a published academic study on
**predicting stock market movements in emerging markets** using **optimized technical
indicators, machine learning, and neural networks**, and extends the analysis through
hands-on implementation and alternative data evaluation.

The work is divided into two major industry-relevant components:

1. **Assessing predictive models using alternative technical data**
2. **Evaluating satellite imagery as a form of alternative financial data**

---

## Introduction

Financial institutions face a constant challenge:

> **How can we extract predictive signals from noisy, high-dimensional financial data,
especially in volatile emerging markets where traditional models fail?**

This project directly addresses problems faced by:
- Quantitative hedge funds
- Asset management firms
- Trading and research desks
- FinTech and alternative data teams
- Risk management and macro research units

It demonstrates **how academic research can be translated into practical, testable
financial models**.

---

## Part 1: Intelligent Stock Prediction Using Alternative Technical Data

### Financial Problem Statement

The core financial problem addressed is **directional prediction**:
> Will a stock or ETF move up or down tomorrow?

Rather than forecasting exact prices (which is unstable and noisy), the project
formulates the task as a **classification problem**, aligning with how real trading
strategies operate (long/short, buy/sell decisions).

This approach is especially critical for **emerging markets**, which:
- Exhibit higher volatility
- Are more sensitive to local political and macro shocks
- Often violate assumptions used in developed-market models

---

## Data Understanding & Feature Engineering

### Data Used
- Daily **Open, High, Low, Close (OHLC)** prices
- Trading volume
- Data sourced from **Yahoo Finance**

### Feature Construction
- Over **200 technical indicators** generated using `PandasTA`
- Indicators include:
  - Momentum (RSI, Williams %R)
  - Trend (Moving Averages, Bollinger Bands)
  - Volume-based metrics
  - Price–volume interactions

### Industry Relevance
Technical indicators compress historical price and volume behavior into signals that
machine learning models can process efficiently—mirroring real quant research
pipelines.

---

## Security Analysis (ETF Focus)

The group analyzed **iShares MSCI Chile Capped ETF (ECH)**:
- Asset type: Emerging market equity ETF
- Market: Chilean equities
- Trading venue: NYSE
- Timeframe analyzed: 2009–2020

Emerging market ETFs like ECH are ideal test cases due to:
- Higher volatility
- Less informational efficiency
- Greater potential alpha opportunities

---

## Methodology

### Model Design
- Binary classification target:
  - 1 → price increases
  - 0 → price decreases

### Feature Selection & Optimization
To avoid overfitting and noise:
- Pearson correlation (descriptive analysis)
- LASSO (penalized feature selection)
- Dimensionality reduction
- Dispersion Ratio (custom technical metric)

Only ~**5% of indicators** were retained, improving:
- Predictive accuracy
- Computational efficiency

---

## Model Validation & Performance

- **10-fold cross-validation** used to ensure generalization
- Logistic regression used for replication experiments
- Accuracy improved from ~77% to ~79% in the paper’s main results
- Training time reduced by ~85%

**Key insight for industry:**
> More data is not always better. Carefully optimized features outperform brute-force
approaches.

---

##  Practical Implementation

As part of hands-on replication:
- ETF data was downloaded programmatically
- Custom technical indicators were computed
- Binary classification targets were constructed
- Cross-validation was implemented
- Key charts were reproduced:
  - Price history
  - Cumulative directional movements

This step mirrors **real-world model validation workflows** used by quant teams.

---

## Part 2: Evaluating Alternative Data — Satellite Imagery

### Why Satellite Data?

Satellite imagery is one of the **most commercially valuable alternative data sources**
used by hedge funds and asset managers today.

It enables:
- Real-time economic activity tracking
- Revenue and demand nowcasting
- Supply-chain and logistics monitoring
- ESG and infrastructure analysis

---

## Satellite Data :

### Data Sources
- **Public:** NASA, ESA, USGS, NOAA
- **Commercial:** Planet Labs, Maxar, Airbus, BlackSky

### Types of Data
- Night-time light intensity (economic activity proxy)
- Vehicle, ship, and container counts
- Infrastructure utilization
- Change-detection metrics

---

## Data Quality, Ethics & Governance

Key issues addressed:
- Cloud cover and noise
- Geographic and urban bias
- Unequal access to high-cost data
- Privacy and geopolitical concerns


## Python Implementation & EDA

The project includes:
- Python workflows to import satellite-derived datasets
- Panel-data structuring
- Exploratory analysis:
  - Correlation analysis
  - Principal Component Analysis (PCA)
  - Fixed-effects panel regressions

These techniques align with **best practices in quantitative finance research**.




## Skills :-

- Financial data analysis
- Feature engineering & selection
- Machine learning validation
- Cross-validation techniques
- Alternative data evaluation
- Python for quantitative finance
- Translating academic research into applied models



## References

Sagaceta-Mejía et al. (2024). *An Intelligent Approach for Predicting Stock Market
Movements in Emerging Markets Using Optimized Technical Indicators and Neural Networks.*

Sun et al. (2024). *Alternative Data in Finance and Business: Emerging Applications and
Theory Analysis.*
