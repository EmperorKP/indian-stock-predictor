# 🇮🇳 Indian Stock Price Predictor

**Production-ready** web application for predicting Indian stock prices (NSE/BSE) using advanced machine learning and TensorFlow.js. Features optimized Yahoo Finance API integration with clean, efficient codebase and real-time predictions for major Indian stocks.

## ✨ Features

- **🇮🇳 Indian Stock Market**: Native NSE/BSE support with accurate symbol conversion
- **📊 Real-time Data**: Yahoo Finance API integration with 66+ data points (3 months)
- **🤖 Advanced ML**: Neural network with 9 technical features + statistical fallback
- **📈 Interactive Charts**: Beautiful visualizations with historical & future predictions
- **⚡ Production Optimized**: Clean codebase, minimal logging, fast performance
- **🎯 High Accuracy**: AI confidence scoring (45-90%) with trend analysis
- **📱 Modern UI**: Responsive design with Tailwind CSS
- **�️ Robust**: Error handling, timeout protection, and smart fallbacks
- **🧹 Clean Architecture**: Optimized build with no debug endpoints or unused code

## Tech Stack

- **Next.js 15 with Turbopack** - High-performance React framework
- **TypeScript** - Type-safe development with enhanced error handling
- **TensorFlow.js** - Advanced neural networks for stock prediction
- **Yahoo Finance API** - Real-time Indian stock market data
- **Chart.js & react-chartjs-2** - Interactive financial charts
- **Tailwind CSS** - Modern responsive design
- **Axios** - Optimized HTTP client with timeout protection

## Project Structure

```
stock-predictor/                      # 🧹 Clean, optimized structure
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   └── stock/route.ts        # ✅ Production Yahoo Finance API
│   │   ├── globals.css               # ✅ Tailwind CSS styles
│   │   ├── layout.tsx               # ✅ App layout
│   │   └── page.tsx                 # ✅ ML prediction interface
│   ├── components/
│   │   └── StockChart.tsx           # ✅ Interactive financial charts
│   └── lib/
│       └── ml-utils.ts              # ✅ Optimized TensorFlow.js ML
├── package.json                      # Dependencies & scripts
├── tailwind.config.ts               # Tailwind configuration
├── tsconfig.json                    # TypeScript configuration
└── README.md                        # Documentation

❌ Removed: debug APIs, unused functions, excessive logging
```

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Modern web browser with JavaScript enabled

### Production Optimizations ✨

This application has been **production-optimized** with:
- ❌ **Removed**: Debug APIs (`/api/debug`, `/api/debug-ml`)
- ❌ **Removed**: Unused functions (`predictMultipleDays`)
- ❌ **Removed**: Excessive console logging and debug outputs
- ❌ **Removed**: Outdated API documentation and unused files
- ✅ **Clean**: Minimal bundle size and fast loading
- ✅ **Secure**: No exposed debug endpoints or sensitive data

### Installation

1. Navigate to the project directory:
```bash
cd stock-predictor
```

2. Install dependencies:
```bash
npm install
```

3. Run the development server:
```bash
npm run dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## How It Works

### 1. Real Data Acquisition
- Fetches live data from Yahoo Finance API for Indian stocks (NSE/BSE)
- Retrieves 3 months of historical price data (66+ data points)
- Automatic symbol format conversion (.NS for NSE, .BO for BSE)
- Smart fallback system with multiple data source attempts

### 2. Advanced ML Processing
- **Primary**: Neural network with 9 technical features (moving averages, volatility, momentum)
- **Fallback**: Fast statistical analysis with linear regression and trend analysis
- **Timeout Protection**: 15-second limit with automatic fallback to statistical methods
- **Multi-layer Processing**: Price normalization, feature engineering, and confidence scoring

### 3. Intelligent Predictions
- **Historical Predictions**: Shows model accuracy on past data for validation
- **Future Forecasts**: Next trading day predictions with confidence scores
- **Trend Analysis**: Up/Down/Stable trend classification with percentage changes
- **Volatility Assessment**: Risk analysis based on historical price movements

### 4. Visualization
- Interactive charts showing actual vs predicted prices
- Future predictions displayed separately
- Model performance metrics for transparency

## Key Components

### StockChart Component
Interactive chart component that displays:
- Historical actual prices (blue line)
- Model predictions on historical data (green dashed line)
- Future predictions (red dashed line)

### ML Engine (`/lib/ml-utils.ts`)
**Optimized prediction system** with:
- 🧠 `trainLinearRegressionModel()` - Advanced neural network training
- 📊 `processStockData()` - Clean data processing pipeline
- 🎯 `calculateR2Score()` & `calculateMSE()` - Performance metrics
- 📈 `getPredictionsForData()` - Batch prediction generation
- 🔮 `predictNextDay()` - Single-day forecasting
- ⚡ **Production optimized**: Minimal logging, efficient processing

### Stock API (`/api/stock`)
**Production-optimized endpoint** featuring:
- 🚀 Yahoo Finance Chart API integration (no authentication required)
- 📊 Automatic NSE (.NS) and BSE (.BO) symbol conversion
- 🔄 Smart retry logic with alternative symbol formats
- ⚡ Clean error responses with helpful suggestions
- 🛡️ Timeout protection and graceful failure handling
- 📈 Returns 66+ historical data points for accurate predictions

## Usage

1. **Enter Indian Stock Symbol**: Type NSE/BSE stock symbols (e.g., RELIANCE, TCS, INFY, HDFCBANK)
2. **Select Exchange**: Choose NSE or BSE exchange
3. **Click "Predict Stock Price"**: The app will:
   - Fetch real-time data from Yahoo Finance
   - Process 3 months of historical Indian stock data
   - Train advanced ML model with timeout protection
   - Display predictions, confidence scores, and trend analysis
   - Show interactive charts with historical and future predictions

## Indian Stock Market Focus

This application is specifically optimized for the Indian stock market:

### Supported Exchanges
- **NSE (National Stock Exchange)**: Primary Indian stock exchange
- **BSE (Bombay Stock Exchange)**: Oldest stock exchange in Asia

### Popular Stocks Supported
| Symbol | Company | Current Range | Market Cap |
|--------|---------|---------------|------------|
| RELIANCE | Reliance Industries | ₹2,600-2,800 | Large Cap |
| TCS | Tata Consultancy Services | ₹4,100-4,300 | Large Cap |
| INFY | Infosys | ₹1,850-1,950 | Large Cap |
| HDFCBANK | HDFC Bank | ₹1,650-1,750 | Large Cap |
| ICICIBANK | ICICI Bank | ₹1,250-1,350 | Large Cap |

## Model Performance

The application provides comprehensive performance metrics:

- **Confidence Score**: AI-generated confidence level (45-90%, higher is better)
- **Trend Direction**: Up/Down/Stable classification with percentage change
- **Prediction Accuracy**: Validated against historical data
- **Volatility Assessment**: Risk analysis for informed decision-making
- **Data Quality**: 66+ data points from 3 months of trading history

## Limitations & Disclaimers

⚠️ **Important**: This is for educational purposes only. Stock predictions are highly uncertain and should not be used for actual investment decisions.

### Current Scope:
- **Market Focus**: Optimized specifically for Indian markets (NSE/BSE)
- **Data-Driven**: Predictions based on 3 months of historical price patterns
- **Technical Analysis**: Uses price trends, moving averages, and volatility
- **API Dependency**: Relies on Yahoo Finance API availability
- **Trading Context**: Market holidays and after-hours trading not considered

### Potential Improvements:
- Add support for global markets (US, European, Asian)
- Implement LSTM networks for sequence learning
- Include volume, market cap, and fundamental data
- Add technical indicators (RSI, MACD, Bollinger Bands)
- Integrate news sentiment analysis
- Implement portfolio-level predictions
- Add real-time alerts and notifications

## 🚀 Production Ready

### ✅ **Optimized Codebase**
- **Clean Architecture**: Removed all debug endpoints and unused functions
- **Minimal Logging**: Production-ready with essential error handling only
- **Optimized Bundle**: No unused dependencies or excessive console outputs
- **Security**: Cleaned environment variables, no exposed debug information

### ✅ **Current Data Sources**

**Yahoo Finance Chart API**: Primary data source
- ✅ NSE/BSE stock data with automatic symbol conversion
- ✅ 3 months of historical data (66+ data points)
- ✅ No API key required - completely free
- ✅ Smart retry logic and comprehensive error handling
- ✅ Real-time price data for accurate predictions

### 📈 **Supported Stocks**

**Major NSE Stocks**: RELIANCE, TCS, INFY, HDFCBANK, ICICIBANK, SBIN, WIPRO, LT, ADANIPORTS, BHARTIARTL

**BSE Equivalent**: All NSE stocks available on Bombay Stock Exchange

### 🔧 **Extending Data Sources**

To add more data sources, extend the optimized `fetchFromYahooFinance()` function in `/api/stock/route.ts`.

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- [TensorFlow.js](https://www.tensorflow.org/js) for browser-based machine learning
- [Chart.js](https://www.chartjs.org/) for beautiful data visualization
- [Next.js](https://nextjs.org/) for the excellent React framework
- [Tailwind CSS](https://tailwindcss.com/) for rapid UI development
