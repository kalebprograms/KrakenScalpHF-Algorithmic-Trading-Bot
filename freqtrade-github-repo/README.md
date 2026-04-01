# 🚀 KrakenScalpHF Algorithmic Trading Bot

High-frequency cryptocurrency trading bot built with Freqtrade for Kraken spot markets.

## 📊 Overview

This project implements a short-term scalping strategy optimized for a 5-minute timeframe, combining technical indicators and price action confirmation to identify high-probability entries.

Designed to demonstrate:

- Algorithmic trading logic  
- Quantitative strategy development  
- Backtesting and performance analysis  
- Python-based automation workflows  

---

## ⚙️ Strategy Summary

KrakenScalpHF uses a confluence-based approach:

- EMA (Fast & Slow): trend direction and pullback entries  
- RSI: oversold condition detection  
- Bollinger Bands: price positioning within volatility range  
- Volume Filter: confirms market participation  
- Bounce Confirmation: avoids entering during continued downward momentum  

### Default Parameters

- Timeframe: `5m`  
- ROI Target: `0.4%`  
- Stoploss: `-0.7%`  
- Trailing Stop: Disabled  
- Exit Signal: Disabled (ROI-based exits)  

---

## 🛠 Tech Stack

- Python  
- Freqtrade  
- Pandas  
- TA-Lib  

---

## 📁 Project Structure

freqtrade-github-repo/
├── strategies/
│   └── KrakenScalpHF.py
├── user_data/
│   └── config.example.json
├── backtest-metadata/
├── .gitignore
├── requirements.txt
└── README.md

---

## 🚀 Getting Started

### 1. Clone the Repository

git clone https://github.com/kalebprograms/KrakenScalpHF-Algorithmic-Trading-Bot.git  
cd KrakenScalpHF-Algorithmic-Trading-Bot  

### 2. Set Up Environment

python -m venv .venv  

Activate environment:

Mac/Linux:  
source .venv/bin/activate  

Windows PowerShell:  
.venv\Scripts\Activate.ps1  

### 3. Install Dependencies

pip install -r requirements.txt  

---

## 🔑 Configuration Setup

Create your local config file:

cp user_data/config.example.json user_data/config.json  

Then edit:

user_data/config.json  

Add your:

- Exchange API keys  
- Telegram bot credentials (optional)  
- Custom settings  

---

## ▶️ Running the Bot

freqtrade trade --config user_data/config.json --strategy KrakenScalpHF  

---

## 📈 Backtesting

freqtrade backtesting --config user_data/config.json --strategy KrakenScalpHF --timeframe 5m  

Backtest metadata is included in:  
backtest-metadata/  

---

## 🔒 Security Notice

Sensitive data is NOT included in this repository.

Never commit:

- API keys  
- Exchange secrets  
- Telegram tokens  
- Passwords  

If any credentials were previously exposed, rotate them immediately.

---

## 📌 Future Improvements

- Hyperparameter optimization (Freqtrade Hyperopt)  
- Multi-timeframe signal confirmation  
- Machine learning-based entry signals  
- Performance visualization dashboard  

---

## 💼 Resume Description

KrakenScalpHF Algorithmic Trading Bot

- Developed a Python-based automated trading system using Freqtrade  
- Implemented EMA, RSI, and Bollinger Band strategies for short-term scalping  
- Designed entry logic using volume filtering and price action confirmation  
- Performed backtesting and optimization across multiple cryptocurrency pairs  
- Integrated risk management with stop-loss and ROI targets  

---

## 📄 License

This project is for educational and portfolio purposes.
