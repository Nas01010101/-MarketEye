# MarketEye 👁️

A Python-based cryptocurrency market data analysis tool that fetches and analyzes real-time market data from the Kraken exchange using the CCXT library.

## 🚀 Features

- Fetch real-time cryptocurrency ticker data from Kraken exchange
- Support for multiple trading pairs (BTC/USD, ETH/USD, ETH/BTC, etc.)
- Display key market metrics (last price, bid/ask, 24h high/low, volume, change %)
- Export data to CSV for further analysis
- Interactive Jupyter notebooks for data exploration

## 📋 Prerequisites

- Python 3.8 or higher
- Kraken exchange account with API credentials
- pip package manager

## 🔧 Installation

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/MarketEye.git
cd MarketEye
```

2. Create and activate a virtual environment:
```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```

3. Install required dependencies:
```bash
pip install -r requirements.txt
```

4. Set up your API credentials:
   - Copy `secrets.json.example` to `secrets.json`
   - Edit `secrets.json` and add your Kraken API credentials:
```json
{
  "kraken_api_key": "your-api-key-here",
  "kraken_api_secret": "your-api-secret-here"
}
```

⚠️ **Important**: Never commit your `secrets.json` file to version control!

## 📊 Usage

### Running the Jupyter Notebook

1. Start Jupyter Lab:
```bash
jupyter lab
```

2. Navigate to `notebooks/00_data_fetch.ipynb` and run the cells

### What the Notebook Does

- **Connects** to Kraken exchange using your API credentials
- **Fetches** real-time market data for cryptocurrency trading pairs
- **Displays** formatted market metrics including:
  - Current price
  - Bid/Ask spread
  - 24-hour high/low
  - Trading volume
  - Price change percentage
- **Exports** data to CSV files in the `data/` directory

## 📁 Project Structure

```
MarketEye/
├── README.md                    # This file
├── requirements.txt             # Python dependencies
├── secrets.json.example         # Template for API credentials
├── secrets.json                 # Your API credentials (gitignored)
├── .gitignore                   # Git ignore rules
├── notebooks/
│   └── 00_data_fetch.ipynb     # Main data fetching notebook
├── data/                        # CSV output directory (gitignored)
└── scripts/                     # Future automation scripts
```

## 🔑 Getting Kraken API Credentials

1. Log in to your Kraken account
2. Navigate to Settings → API
3. Click "Generate New Key"
4. Set permissions (you only need "Query Funds" and "Query Open Orders & Trades" for read-only access)
5. Save your API Key and Private Key securely

## 📈 Supported Trading Pairs

The notebook currently fetches data for:
- BTC/USD (Bitcoin to US Dollar)
- ETH/USD (Ethereum to US Dollar)
- ETH/BTC (Ethereum to Bitcoin)

You can easily modify the notebook to fetch data for any trading pair available on Kraken.

## 🛠️ Dependencies

- **ccxt**: Cryptocurrency exchange trading library
- **pandas**: Data manipulation and analysis
- **jupyter**: Interactive notebook environment
- **matplotlib**: Data visualization (for future enhancements)

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests

## ⚠️ Disclaimer

This tool is for educational and informational purposes only. Cryptocurrency trading carries risk. Always do your own research before making investment decisions.

## 📝 License

This project is open source and available under the MIT License.

## 🔮 Future Enhancements

- [ ] Historical data fetching
- [ ] Price charts and visualizations
- [ ] Technical indicators (RSI, MACD, Moving Averages)
- [ ] Automated data collection scripts
- [ ] Support for multiple exchanges
- [ ] Price alerts and notifications
- [ ] Portfolio tracking

## 📧 Contact

For questions or feedback, please open an issue on GitHub.

---

Made with ❤️ for the crypto community

