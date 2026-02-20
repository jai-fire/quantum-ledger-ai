# Quantum Ledger AI

An advanced AI-powered futures trading bot with multi-AI ensemble strategies, real-time price monitoring, and automated risk management.

## 📊 Features

### Dashboard
- **Real-time Market Data**: Live price tracking for BTC, ETH, SOL, BNB, ADA, XRP
- **Trading Metrics**: Total P&L, Win Rate, Open Positions, Total Trades
- **Risk Management**: Futures Risk Monitor with position sizing and leverage management
- **AI Signals**: Multi-AI ensemble signals for trade execution
- **Performance Charts**: Cumulative P&L visualization with time-based analysis

### Charts
- **Advanced Charting**: Real-time candlestick charts with OHLC data
- **Multiple Timeframes**: 1m, 5m, 15m, 1h, 4h, 1d intervals
- **Technical Indicators**: Price, volume analysis
- **30+ Crypto Pairs**: Support for major cryptocurrency trading pairs

### Manual Trading
- **Order Placement**: Market, Limit, and Stop orders
- **Trade Modes**: Spot and Futures trading
- **Risk Controls**: Stop Loss and Take Profit management
- **Exchange Integration**: Multi-exchange support with API connectivity

### Automated Strategies
- **BTC Momentum LSTM**: 1h timeframe, 66.7% win rate
- **SOL Scalper GBM**: 15m timeframe, 61.9% win rate
- **ETH Ensemble Pro**: 4h timeframe, 61.1% win rate
- **Performance Tracking**: Real-time P&L monitoring per strategy
- **Strategy Controls**: Enable/disable strategies on-the-fly

### Settings
- **Exchange Configuration**: Add/manage multiple exchange connections
- **API Key Management**: Secure credential storage
- **AI Model Selection**: Choose from multiple AI models
- **Trading Preferences**: Customize trading parameters
- **Testnet Support**: Test on Testnet before live trading

## 🛠️ Tech Stack

- **Frontend**: React.js with modern UI components
- **Charts**: Interactive candlestick chart visualization
- **Backend**: Node.js/Python APIs
- **AI/ML**: TensorFlow LSTM models, ensemble learning
- **Database**: Real-time data storage
- **Deployment**: Base44 platform (serverless)

## 📋 Project Structure

```
quantum-ledger-ai/
├── src/
│   ├── components/
│   │   ├── Dashboard/
│   │   │   ├── DashboardPage.jsx
│   │   │   ├── PriceCard.jsx
│   │   │   ├── MetricsCard.jsx
│   │   │   └── SignalsPanel.jsx
│   │   ├── Charts/
│   │   │   ├── ChartsPage.jsx
│   │   │   ├── CandlestickChart.jsx
│   │   │   └── Timeframe Selector.jsx
│   │   ├── Trade/
│   │   │   ├── ManualTradePage.jsx
│   │   │   ├── OrderForm.jsx
│   │   │   └── OrderTypeSelector.jsx
│   │   ├── Strategies/
│   │   │   ├── StrategiesPage.jsx
│   │   │   ├── StrategyCard.jsx
│   │   │   └── StrategyManager.jsx
│   │   ├── Settings/
│   │   │   ├── SettingsPage.jsx
│   │   │   ├── ExchangeManager.jsx
│   │   │   └── APIKeyManager.jsx
│   │   └── Shared/
│   │       ├── Navigation.jsx
│   │       ├── Layout.jsx
│   │       └── StatusIndicator.jsx
│   ├── hooks/
│   │   ├── useMarketData.js
│   │   ├── useTradingAPI.js
│   │   ├── useWebSocket.js
│   │   └── useAISignals.js
│   ├── utils/
│   │   ├── api.js
│   │   ├── chartUtils.js
│   │   ├── tradingCalculations.js
│   │   └── formatters.js
│   ├── styles/
│   │   ├── global.css
│   │   ├── dashboard.css
│   │   ├── charts.css
│   │   └── components.css
│   └── App.jsx
├── public/
│   ├── index.html
│   └── favicon.ico
├── .gitignore
├── package.json
├── README.md
└── LICENSE
```

## 🚀 Installation & Setup

### Prerequisites
- Node.js 14+
- npm or yarn
- Exchange API keys (Binance, Coinbase, etc.)

### Steps

1. **Clone the repository**:
```bash
git clone https://github.com/jai-fire/quantum-ledger-ai.git
cd quantum-ledger-ai
```

2. **Install dependencies**:
```bash
npm install
```

3. **Create environment variables**:
```bash
cp .env.example .env
```

4. **Configure your exchange API keys** in `.env`:
```env
REACT_APP_BINANCE_API_KEY=your_api_key
REACT_APP_BINANCE_SECRET=your_secret
REACT_APP_COINBASE_API_KEY=your_api_key
REACT_APP_COINBASE_SECRET=your_secret
```

5. **Start development server**:
```bash
npm start
```

6. **Build for production**:
```bash
npm run build
```

## 📡 API Endpoints

### Market Data
- `GET /api/prices` - Get current prices
- `GET /api/charts/:symbol/:timeframe` - Get OHLC data
- `GET /api/signals` - Get AI trading signals

### Trading
- `POST /api/orders` - Place new order
- `GET /api/orders` - Get order history
- `GET /api/positions` - Get open positions
- `POST /api/orders/:id/cancel` - Cancel order

### Strategies
- `GET /api/strategies` - List all strategies
- `POST /api/strategies/:id/execute` - Execute strategy
- `GET /api/strategies/:id/performance` - Strategy performance

### Exchanges
- `GET /api/exchanges` - List connected exchanges
- `POST /api/exchanges` - Add new exchange
- `DELETE /api/exchanges/:id` - Remove exchange

## 🤖 AI Models

### Momentum LSTM
- **Timeframe**: 1 hour
- **Asset**: BTC/USDT
- **Accuracy**: 66.7%
- **Strategy**: Momentum-based price prediction

### GBM Scalper
- **Timeframe**: 15 minutes
- **Asset**: SOL/USDT
- **Accuracy**: 61.9%
- **Strategy**: Gradient Boosting Machine for quick scalps

### Ensemble Pro
- **Timeframe**: 4 hours
- **Asset**: ETH/USDT
- **Accuracy**: 61.1%
- **Strategy**: Ensemble voting across multiple ML models

## 📊 Trading Metrics

- **Win Rate**: Percentage of profitable trades
- **P&L**: Profit/Loss in USD
- **Drawdown**: Maximum peak-to-trough decline
- **Sharpe Ratio**: Risk-adjusted returns
- **Risk/Reward Ratio**: Trade risk vs potential reward

## 🔐 Security

- ✅ API keys encrypted in transit
- ✅ Testnet mode for paper trading
- ✅ Rate limiting on all endpoints
- ✅ Two-factor authentication support
- ✅ Secure WebSocket connections (WSS)

## ⚠️ Risk Disclaimer

This is a trading bot for automated cryptocurrency futures trading. Trading cryptocurrency is high-risk and involves substantial financial risk. You may lose more than your initial investment. Past performance is not indicative of future results. Always:

- Start with small amounts
- Use testnet before live trading
- Set appropriate stop losses
- Never risk more than you can afford to lose
- Understand the risks involved

## 🐛 Troubleshooting

### Connection Issues
```bash
# Check API connectivity
curl https://api.binance.com/api/v3/ping
```

### Missing Signals
- Ensure AI models are enabled in Settings
- Check exchange API keys are valid
- Verify sufficient market data (minimum 100 candles)

### Order Execution Fails
- Check account balance
- Verify order parameters (size, price)
- Test on testnet first

## 📚 Documentation

- [Trading Guide](./docs/TRADING_GUIDE.md)
- [API Documentation](./docs/API.md)
- [Strategy Development](./docs/STRATEGY_DEVELOPMENT.md)
- [Configuration Guide](./docs/CONFIG.md)

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚡ Performance

- Dashboard loads in < 1 second
- Real-time price updates every 1 second
- Chart data refreshes every 5 seconds
- API response time < 200ms

## 🎯 Roadmap

- [ ] Advanced backtesting framework
- [ ] Strategy optimizer with genetic algorithms
- [ ] Mobile app (iOS/Android)
- [ ] Discord/Telegram bot integration
- [ ] Advanced risk management models
- [ ] Options trading support
- [ ] Market maker strategies

## 📞 Support

For issues and feature requests, please open a GitHub issue or contact the development team.

## 🙏 Acknowledgments

- Built with React and modern web technologies
- AI models powered by TensorFlow
- Market data from Binance, Coinbase, and other exchanges
- Deployed on Base44 serverless platform
