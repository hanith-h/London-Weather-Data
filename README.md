# London Weather Data Analysis (1979–2023)

## Overview
This repository contains a complete exploratory data analysis (EDA) and machine learning preparation pipeline for **daily weather observations in London** from January 1, 1979 to December 31, 2023.

The main file `Phase_1.ipynb` performs:
- Data cleaning & preprocessing
- Statistical analysis
- Rich visualizations
- Skewness & kurtosis checks
- Feature selection
- Scaling and train-test split

The ultimate goal is to **predict daily maximum temperature (TX)** with high accuracy using historical weather patterns.

## Dataset
- **File**: `london_weather_data_1979_to_2023.csv`
- **Rows**: 16,436 (one record per day)
- **Period**: 1979-01-01 to 2023-12-31

### Columns
| Column | Description                              | Unit                  |
|-------|-------------------------------------------|------------------------|
| DATE  | Date                                      | YYYYMMDD              |
| TX    | Maximum temperature                       | tenths of °C (÷10 → °C) |
| TN    | Minimum temperature                       | tenths of °C          |
| TG    | Mean grass temperature                    | tenths of °C          |
| SS    | Sunshine duration                         | hours × 10            |
| SD    | Sunshine duration (alternative)           | hours × 10            |
| RR    | Daily rainfall                            | tenths of mm          |
| QQ    | Global radiation                          | J/cm²                 |
| PP    | Mean sea level pressure                   | tenths of hPa         |
| HU    | Relative humidity                         | %                     |
| CC    | Cloud cover                               | octas (0–9)           |
| Q_*   | Quality flags (0 = good, 1+ = suspect)    | —                     |

> **Note**: All temperature values are stored in **tenths of a degree Celsius** (e.g., 156 = 15.6°C).

## Requirements
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
