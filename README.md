# Stock News Sentiment Analysis

This project analyzes and compares multiple stock trading strategies including news sentiment analysis using NLP models and traditional technical indicators (MACD, RSI, SMA, BB) against a Buy & Hold baseline.

## Project Overview

- Utilizes pre-trained NLP models (FinBERT, GGBERT) to generate trading signals from financial news sentiment.
- Implements classical technical strategies: Moving Average (SMA), Relative Strength Index (RSI), Moving Average Convergence Divergence (MACD), and Bollinger Bands (BB).
- Computes and compares the following performance metrics:
  - Cumulative Return
  - Maximum Drawdown (MDD)
  - Sharpe Ratio
- Visualizes performance metrics to evaluate and compare strategies.

## Repository Structure


├── data # Input stock price data and sentiment labels<br>
├── sentiment_data # The output from model <br>
├── Bert_sentiment_anaylsis.ipynb # Fine-tuning model <br>
├── FinalEvaluation.ipynb # Evaluation <br>
├── Label_with_FinBert.ipynb # Labeling with finBERT<br>
├── Performance_test.ipynb # Accuracy <br>
├── Preprocessed_Stock_News.ipynb # Data cleansing <br>
├── Sentiment_test_data.ipynb.ipynb # Using model to predict ouput<br>
└── Stock_news_data_collection.ipynb # Web scraping


## Strategies Compared

| Strategy                            | Description                                               |
|-------------------------------------|-----------------------------------------------------------|
| `FinBERT`                           | Sentiment-based strategy using FinBERT signals            |
| `GGBERT`                            | Sentiment-based strategy using GGBERT signals             |
| `FinBERT / GGBERT + FinBERT Label`  | Combined prediction using FinBERT-generated labels        |
| `FinBERT / GGBERT + Return Next Label` | Strategy based on predicted next-day return direction |
| `Buy & Hold`                        | Benchmark strategy                                        |
| `MACD`, `RSI`, `SMA`, `BB`          | Technical indicator-based strategies                      |

## Metrics Explained

- **Cumulative Return** – The compounded return over the entire period.
- **Maximum Drawdown (MDD)** – The maximum observed loss from a peak to a trough.
- **Sharpe Ratio** – A measure of risk-adjusted return. Higher values indicate better risk-reward performance.

## How To Use

1. Clone the repository:

   ```bash
   git clone https://github.com/Takedaxz/NLP_Stock-Sentiment-Analysis.git
   cd NLP_Stock-Sentiment-Analysis
2. Install dependencies:

    ```bash
    pip install -r requirements.txt
### References
FinBERT: https://arxiv.org/abs/1908.10063 <br>
GGBERT model: https://huggingface.co/google-bert/bert-base-uncased
