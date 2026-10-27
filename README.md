# Forex_analyz-

Exploratory Jupyter notebook for XAUUSD (gold) daily data via Alpha Vantage: moving averages, returns, and basic analysis with pandas / matplotlib / scikit-learn.

## Setup

1. Create a virtualenv and install dependencies:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

2. Configure your API key **locally only** (never commit it):

```bash
cp .env.example .env
# edit .env and set ALPHAVANTAGE_API_KEY
```

The notebook loads `ALPHAVANTAGE_API_KEY` with `python-dotenv` / `os.getenv`. If the variable is missing, it raises a clear error.

3. Open the notebook:

```bash
jupyter notebook gold_usd_analysis.ipynb
```

## Security note

Do not hardcode API keys in the notebook or commit `.env`. If a key was ever committed, rotate it at Alpha Vantage and treat the old value as compromised.
