# Trader Performance vs Market Sentiment
**Primetrade.ai — Data Science Intern Assignment**


## Overview
This project analyzes how Bitcoin market sentiment (Fear/Greed Index) relates to trader behavior and performance on the Hyperliquid DEX. The goal is to uncover actionable patterns that inform smarter trading strategies.


## Datasets
| Dataset | Rows | Description |

| `fear_greed_index.csv` | 2,644 | Daily Bitcoin Fear/Greed classifications (2018–2025) |


| `historical_data.csv` | 211,224 | Hyperliquid trade records across 32 accounts & 246 coins (May 2023 – May 2025) |



## Setup & How to Run

### Requirements

pip install pandas numpy matplotlib seaborn scipy jupyter nbformat


### Run the Notebook

jupyter notebook Trader_Sentiment_Analysis.ipynb


Place both CSV files in the same directory as the notebook, then run all cells top to bottom.


## Project Structure
Trader_Sentiment_Analysis.ipynb   # Main analysis notebook
README.md                          # This file
WRITEUP.md                         # 1-page methodology + insights summary
fear_greed_index.csv               # Input dataset 1
historical_data.csv                # Input dataset 2
 charts
─ chart1_performance_by_sentiment.png
─ chart2_behavior_by_sentiment.png
─ chart3_segment_analysis.png
─ chart4_timeseries.png
─ chart5_risk_metrics.png
─ chart6_winners_vs_losers.png
─ table1_performance_by_sentiment.csv
─ table2_segment_profiles.csv
─ table3_leverage_x_sentiment.csv
─ daily_account_sentiment_merged.csv
─ account_summary.csv


## Key Findings (Summary)

| Metric | Fear Days | Greed Days | Delta |

| Median Daily PnL | $122.7 | $265.2 | **+116% on Greed** |
| Avg Win Rate | 84.2% | 85.6% | Similar |
| Avg Trades/Day | 105.4 | 76.9 | **+37% more on Fear** |
| Avg Leverage | 0.91x | 1.21x | Higher FOMO on Greed |
| Long Bias | 52.2% | 47.2% | Contrarian on Greed |


## Strategy Recommendations

1. **Leverage Gate:** Cap leverage at 1x on Fear days; allow up to 2x on Greed days
2. **Counter-Trend Positioning:** Increase long exposure on Extreme Fear; trim longs on Extreme Greed
3. **Trade Frequency Control:** Reduce trade count by 50% on Fear days to avoid panic overtrading
