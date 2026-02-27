# Trader Performance vs Market Sentiment (Fear & Greed Index)

## Objective
Analyze how trader performance (Closed PnL) and behavior changes across market sentiment using the Fear & Greed Index. Extract actionable insights and propose sentiment-based strategy adjustments.

## Datasets
1) **Historical Trader Data (Hyperliquid)**
- File: `csv_files/historical_data.csv`
- Key fields used: `Account`, `Timestamp IST`, `Closed PnL`, `Coin`, `Side`

2) **Fear & Greed Index**
- File: `csv_files/fear_greed_index.csv`
- Fields used: `date`, `value (0–100)`, `classification`

## Repository Structure (required)
ds_ice/
├── notebook_1.ipynb
├── csv_files/
│   ├── historical_data.csv
│   └── fear_greed_index.csv
├── outputs/
│   ├── chart_avg_pnl_by_sentiment.png
│   ├── chart_win_rate_by_sentiment.png
│   ├── chart_avg_pnl_by_sentiment_bins.png
│   ├── overall_metrics.csv
│   ├── sentiment_class_performance.csv
│   ├── sentiment_bin_performance.csv
│   └── top_traders_by_total_pnl.csv
├── ds_report.pdf
└── README.md

## How to Run (Google Colab)
1. Open the Colab notebook link: **PASTE_COLAB_LINK_HERE**
2. Ensure Google Drive is mounted in Colab.
3. Ensure the project folder path matches your Drive folder (the notebook expects the `ds_ice/` folder).
4. Run cells top-to-bottom to reproduce:
   - dataset merge (trades + sentiment)
   - summary tables (overall + by sentiment)
   - charts saved under `outputs/`
   - final report generated as `ds_report.pdf`

## Outputs
- Final report: `ds_report.pdf`
- Charts: `outputs/*.png`
- Summary tables: `outputs/*.csv`

## Key Findings (high level)
- Performance differs across sentiment regimes.
- Strongest uplift appears in high sentiment (80–100 / Extreme Greed), while the weakest band appears around 20–40.
- Sentiment-aware risk adjustments can plausibly improve results.

## Strategy Recommendations (rules of thumb)
1. **Aggressive mode in Extreme Greed (or 80–100):**
   Consider higher position sizing / faster entry, while keeping strict risk limits.
2. **Defensive mode in 20–40 sentiment band:**
   Reduce risk (smaller size), tighten stops, and avoid overtrading.
