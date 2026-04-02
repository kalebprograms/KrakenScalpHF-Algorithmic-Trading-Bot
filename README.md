# Freqtrade KrakenScalpHF Bot

This repo contains a custom Freqtrade strategy for Kraken spot trading on the 5 minute timeframe.

## Included

- `strategies/KrakenScalpHF.py` - the strategy file
- `user_data/config.example.json` - safe example config with secrets removed
- `backtest-metadata/` - metadata from prior backtest runs
- `.gitignore` - blocks secrets, DB files, and generated runtime files from being committed

## Strategy summary

`KrakenScalpHF` uses:

- EMA fast / EMA slow
- RSI oversold filter
- Bollinger Bands mid/lower behavior
- Volume confirmation
- Simple bounce confirmation from previous close

Current defaults in the strategy:

- Timeframe: `5m`
- ROI: `0.004`
- Stoploss: `-0.007`
- Exit signal: disabled
- Trailing stop: disabled

## Important

Do **not** upload your real API keys, Telegram token, bot password, or other secrets to GitHub.

Before using this bot locally:

1. Copy `user_data/config.example.json` to `user_data/config.json`
2. Add your own real credentials only in the local `config.json`
3. Keep `user_data/config.json` out of Git with the included `.gitignore`

## Suggested repo structure

```
freqtrade-github-repo/
├── strategies/
│   └── KrakenScalpHF.py
├── user_data/
│   └── config.example.json
├── backtest-metadata/
├── .gitignore
├── requirements.txt
└── README.md
```

## Quick start

```bash
git clone <your-repo-url>
cd freqtrade-github-repo
python -m venv .venv
source .venv/bin/activate  # Windows PowerShell: .venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

Create your local config:

```bash
cp user_data/config.example.json user_data/config.json
```

Then edit `user_data/config.json` with your real local credentials.

## Example Git commands

```bash
git init
git add .
git commit -m "Initial commit for KrakenScalpHF freqtrade bot"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
```

## Notes on your uploaded files

Your uploaded config included live secrets, so this repo bundle intentionally replaces them with placeholders.
If those credentials were ever exposed publicly, rotate them before using the bot again.
