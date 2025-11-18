# MarketEye

Simple tooling to pull live cryptocurrency prices from Kraken using CCXT.

## What You Get

- Jupyter notebook (`notebooks/00_data_fetch.ipynb`) that:
  - connects to Kraken
  - grabs ETH/BTC plus a few USD pairs
  - prints key stats (last, bid/ask, 24h range, volume, % change)
  - saves the snapshot to `data/market_data_<timestamp>.csv`

## Quick Start

```bash
git clone https://github.com/Nas01010101/-MarketEye.git
cd MarketEye
python -m venv env
source env/bin/activate        # Windows: env\Scripts\activate
pip install -r requirements.txt
cp secrets.json.example secrets.json
```

Edit `secrets.json` so it contains your Kraken API key and secret. That file stays local and is already gitignored.

## Run the Notebook

```bash
jupyter lab
```

Open `notebooks/00_data_fetch.ipynb`, run all cells, and you’ll see:

- connection confirmation
- current ticker info for ETH/BTC
- summary table for BTC/USD, ETH/USD, ETH/BTC
- CSV export path

Change `pairs` inside the notebook if you need different markets.

## Notes

- Python 3.8+ recommended
- Dependencies: ccxt, pandas, jupyter (see `requirements.txt`)
- Output CSV files land in `data/` (already ignored)
- No production trading logic—this is strictly for quick data pulls

That’s it. Keep your API keys private and refresh the notebook whenever you need new snapshots.

