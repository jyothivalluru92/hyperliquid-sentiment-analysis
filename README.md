# Hyperliquid Trader Behavior & Sentiment Analysis

This project analyzes the relationship between market sentiment (Fear & Greed Index) and trader performance on the Hyperliquid exchange. The goal is to identify behavioral patterns, segment traders into archetypes, and propose data-driven trading strategies.

## 🚀 Setup & Installation

To run the analysis locally, ensure you have Python 3.8+ installed.

# 1. Clone the repository:
git clone https://github.com/jyothivalluru92/hyperliquid-sentiment-analysis.git

# 2. Enter the directory:
cd hyperliquid-sentiment-analysis

# 3. Install Required Libraries:
pip install pandas matplotlib seaborn scikit-learn

# 4. Run the Analysis:
Open Hyperliquid_Analysis.ipynb in Jupyter Notebook or VS Code and run all cells.

📊 Methodology
1. Data Integration: Merged high-frequency trader data (historical_data.csv) with daily market sentiment scores (fear_greed_index.csv) using time-series alignment.

2. Feature Engineering: Created performance metrics (Win Rate, PnL Efficiency) and behavioral proxies (Trade Frequency, Position Size, Order Aggression).

3. Segmentation: Grouped accounts into behavioral archetypes using K-Means Clustering.

4. Predictive Modeling: Developed a Random Forest Classifier to forecast next-day profitability.

💡 Key Insights

# 1. The "Momentum Trap": While overall win rates are highest during "Extreme Greed," the Long/Short ratio actually drops. This suggests that the most successful traders are taking profits or reversing positions while retail sentiment peaks.

# 2, The Panic-Trading Penalty: Trade frequency is 4x higher during "Extreme Fear" than during "Neutral" days, yet retail win rates drop significantly. This proves that emotional over-trading is a primary cause of capital erosion.

# 3. The Agility Paradox: Smaller, "Calculated" traders (Cluster 2) maintain a higher win rate (41.17%) compared to "Whales" (Cluster 1). This indicates that smaller accounts benefit from higher agility and better exit liquidity.

📈 Strategy Recommendations (Actionable Output)

Rule 1: The Volatility Buffer
Finding: Retail traders lose the most when frequency spikes during Fear.
Action: During Extreme Fear (<25), enforce a 50% reduction in position size and a hard cap of 2 trades per day to prevent emotional "revenge trading."

Rule 2: The Contrarian Filter
Finding: Short win rates climb to 59% during Extreme Greed.
Action: When Sentiment crosses >80, freeze new Long positions and transition to trailing stop-losses to exit into retail FOMO liquidity.

🤖 Machine Learning Bonus Results
# 1. Predictive Accuracy: The Random Forest model achieved 61.16% accuracy in predicting next-day trader profitability.

# 2. Behavioral Archetypes: Identified three distinct groups: High-Frequency Scalpers, Institutional Whales, and Calculated Retailers.
