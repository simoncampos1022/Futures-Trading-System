# 🧭 Botara 3.0 - Futures Trading System [Project ID: P-708]

Advanced algorithmic trading system for crypto, forex, and stock futures markets. Combines multi-indicator strategy with Optuna-optimized parameters and robust risk management for consistent profitability.

## 📚 Table of Contents
- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Screenshots](#screenshots)
- [Contact](#contact)

## About

Botara 3.0 delivers automated futures trading across cryptocurrency, forex, and stock markets using a proven multi-indicator strategy. Built after extensive research and optimized with Optuna's Bayesian optimization across years of historical data from Bitget and Blofin exchanges.

**Key Goals:**
- Achieve consistent profitability through data-driven strategy optimization
- Implement robust risk management with dynamic ATR-based position sizing
- Provide seamless multi-exchange support (Binance, Bitget, Blofin, Bybit, MT4/5)

Currently in successful live testing for 2+ months with positive results.

## Features

- **Multi-Indicator Strategy** - Fisher Transform, RSI, Volume Oscillator, ATR
- **Optuna Optimization** - Bayesian-optimized entry/exit parameters
- **Dual Position Support** - Long + Short positions simultaneously
- **Dynamic Risk Management** - ATR-based stop-loss/take-profit + trailing stops
- **Partial Exits** - 50% position close at first target, trail remainder
- **Real-time Monitoring** - Position checks every second, hourly signals
- **Multi-Exchange** - Binance, Bitget, Blofin, Bybit, MT4/5, TradeStation
- **Interactive CLI** - Manual position control and balance monitoring
- **Performance Tracking** - CSV logs, webhook alerts, daily PnL reports

## Tech Stack

**Languages:** Python 3.8+

**Core Libraries:**
- `pandas`, `numpy` - Data processing
- `requests` - Exchange APIs
- `optuna` - Hyperparameter optimization
- `threading` - Concurrent operations

**Exchanges:** Binance, Bitget, Blofin, Bybit, MT4/5, TradeStation

**Optimization:** Tree-structured Parzen Estimator (TPE), Walk-forward analysis

## Installation

```bash
# Clone the repository
git clone https://github.com/simoncampos1022/Futures-Trading-System.git
cd botara_strategy

# Install dependencies
pip install -r requirements.txt
# or: pip install requests pandas numpy optuna
```

## Configuration

Create `.env` file with your exchange API credentials:

```
API_KEY=your_api_key
API_SECRET=your_api_secret
PASSPHRASE=your_passphrase  # For Blofin/Bybit
```

**Key Parameters:**
```
INITIAL_BALANCE=10000
LEVERAGE=5
POSITION_SIZE_RATIO=0.4  # 40% of balance
INTERVAL=1H
FEE_PERCENT=0.0006
```

**Optuna-Optimized Levels:** FS, RSI thresholds and ATR multipliers for entry/exit

## Usage

```bash
# Start trading bot
python botara3_bot.py
```

**Interactive Commands:**
```
help                 # Show commands
force open long      # Manual long position
force open short     # Manual short position
balance              # Current balance
price                # Current price
exit                 # Shutdown
```

## Screenshots

![Logo](logo.png)

## Contact

**Simon Campos**  
[simon.campos1022@gmail.com](mailto:simon.campos1022@gmail.com)  
Telegram: [@simoncampos1022](https://t.me/simoncampos1022)
