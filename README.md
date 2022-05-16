# Module-4-Challenge

For this project, I evaluated four different fund portfolios to determine the fund with the highest investment potential. I used different measures to determine the investment potential, including daily and cumulative returns, standard deviation, sharpe ratios, covariance, and beta.

---

## Technologies

This project uses pandas programming language and utilizes Anaconda, Git Bash, Jupyter Lab, and Github.

---

## Installation Guide

These are the required libraries and dependencies:

import pandas as pd
from pathlib import Path
import numpy as np
%matplotlib inline

You must also read in the whale_navs.csv file.

---

## Usage

I first created the daily returns dataframe as a starting point:

daily_returns = whale_df.pct_change().dropna(how='all')brought in historical data:


I calculated and sorted the standard deviations. Then, I compared all the rolling standard deviations in a plot graph.

standard_deviation = daily_returns.std()
daily_returns.rolling(window=21).std().plot(title='21-Day Rolling Standard Deviations', figsize=(10,5))

I then compared the sharpe ratios, covariance, and beta between two of the funds.

sharpe_ratios = average_annual_return / annualized_standard_deviation
berkshire_rolling_60_covariance = daily_returns['BERKSHIRE HATHAWAY INC'].rolling(window=60).cov(market_rolling_60_variance)
berkshire_average_beta = berkshire_rolling_60_beta.mean()

---

## Contributors

Allyssa Carmin

---

## License

SMU Fintech Course