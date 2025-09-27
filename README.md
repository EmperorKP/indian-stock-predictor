# Indian Stock Predictor 🇮🇳📈

[![Deploy to Vercel](https://github.com/EmperorKP/indian-stock-predictor/actions/workflows/deploy.yml/badge.svg)](https://github.com/EmperorKP/indian-stock-predictor/actions/workflows/deploy.yml)
[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen)](https://indian-stock-predictor.vercel.app)

AI-powered stock market predictor for Indian stocks (NSE/BSE) using Next.js 15, TypeScript, and TensorFlow.js with real-time data from Yahoo Finance API.

## 🌐 Live Demo

**Production**: https://indian-stock-predictor.vercel.app

The application is automatically deployed to Vercel using GitHub Actions on every push to the main branch. The live demo URL is dynamically updated after each successful deployment.

## ✨ Features

- **Real-time Indian Stock Data**: Fetches live stock prices for NSE and BSE listed companies
- **AI-Powered Predictions**: Uses TensorFlow.js for machine learning predictions
- **Interactive Charts**: Beautiful visualizations with prediction overlays
- **Smart Symbol Recognition**: Supports multiple Indian stock symbol formats
- **Fast & Responsive**: Built with Next.js 15 and Turbopack for optimal performance
- **Type-Safe**: Full TypeScript implementation for reliability
- **Auto-Deployment**: Continuous deployment via GitHub Actions

## 🚀 Supported Indian Stocks

The app supports major Indian stocks including:
- **Banking**: HDFCBANK, ICICIBANK, SBIN, AXISBANK
- **IT**: TCS, INFY, WIPRO, HCLTECH
- **Conglomerates**: RELIANCE, ADANIENTERPRISES
- **Consumer**: HINDUNILVR, ITC, NESTLEIND
- **Auto**: TATAMOTORS, MARUTI, BAJAJ-AUTO
- **Pharma**: SUNPHARMA, DRREDDY, CIPLA

## 🛠️ Technology Stack

- **Frontend**: Next.js 15 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **ML/AI**: TensorFlow.js
- **Charts**: Chart.js with React wrapper
- **API**: Yahoo Finance (via web scraping)
- **Build Tool**: Turbopack
- **Deployment**: Vercel with GitHub Actions CI/CD

## 📊 How It Works

1. **Data Fetching**: Retrieves historical stock data from Yahoo Finance API
2. **Data Processing**: Normalizes and prepares data for machine learning
3. **ML Training**: Trains a neural network model using TensorFlow.js
4. **Prediction**: Generates price predictions and confidence intervals
5. **Visualization**: Displays interactive charts with historical and predicted data

## 🏃‍♂️ Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn

### Installation

```bash
git clone https://github.com/EmperorKP/indian-stock-predictor.git
cd indian-stock-predictor
npm install
```

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production Build

```bash
npm run build
npm start
```

## 🚀 Deployment

### Automatic Deployment (Recommended)

The project uses GitHub Actions for automatic deployment to Vercel:

1. **Push to main branch** → Automatic production deployment
2. **Create pull request** → Automatic preview deployment

### Manual Deployment

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy to production
vercel --prod
```

### GitHub Secrets Setup

To enable automatic deployment, add these required secrets to your GitHub repository:

1. Go to your repository → Settings → Secrets and variables → Actions
2. Add the following secrets with your actual values:
   - `VERCEL_TOKEN`: Your Vercel API token (get from [Vercel Account Settings](https://vercel.com/account/tokens))
   - `ORG_ID`: Your Vercel organization ID (found in project settings)
   - `PROJECT_ID`: Your Vercel project ID (found in project settings)

> ⚠️ **Security Note**: Never commit actual secret values to your repository. Always use GitHub Secrets for sensitive data.

## 🔧 Configuration

The app works out of the box with no additional configuration required. It uses Yahoo Finance's public API for stock data.

## 📈 Usage

1. Enter an Indian stock symbol (e.g., "TCS", "RELIANCE", "HDFCBANK")
2. Select the exchange (NSE or BSE)
3. Click "Predict Stock Price"
4. View the interactive chart with:
   - Historical price data
   - ML predictions
   - Confidence intervals
   - Key metrics

## 🧠 Machine Learning Models

The app uses multiple ML approaches:

- **Linear Regression**: Fast baseline predictions
- **Neural Network**: Advanced pattern recognition
- **Feature Engineering**: Technical indicators and trends
- **Ensemble Methods**: Combines multiple models for better accuracy

## 📊 Project Structure

```
indian-stock-predictor/
├── .github/workflows/          # GitHub Actions for CI/CD
├── src/
│   ├── app/
│   │   ├── api/stock/         # Stock data API endpoint
│   │   ├── globals.css        # Global styles
│   │   ├── layout.tsx         # Root layout component
│   │   └── page.tsx           # Main application page
│   ├── components/
│   │   └── StockChart.tsx     # Interactive chart component
│   └── lib/
│       └── ml-utils.ts        # Machine learning utilities
├── public/                    # Static assets
├── .vercel/                   # Vercel configuration
└── README.md                  # Project documentation
```

## 🎯 Accuracy & Limitations

- **Educational Purpose**: This tool is for learning and research
- **Not Financial Advice**: Do not use for actual trading decisions
- **Market Volatility**: Stock markets are inherently unpredictable
- **Data Dependencies**: Accuracy depends on data quality and market conditions

## 🔄 CI/CD Pipeline

The project uses GitHub Actions for continuous integration and deployment:

1. **Code Push** → Trigger workflow
2. **Install Dependencies** → `npm ci`
3. **Build Project** → `npm run build`
4. **Deploy to Vercel** → Production or Preview
5. **Update Live Site** → Automatic

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Yahoo Finance for stock data
- TensorFlow.js team for the ML framework
- Next.js team for the amazing React framework
- Chart.js for beautiful visualizations
- Vercel for seamless deployment

---

**Disclaimer**: This application is for educational and research purposes only. Stock market predictions are inherently uncertain, and this tool should not be used as the sole basis for investment decisions. Always consult with financial professionals and do your own research before making investment choices.

## ✨ Features

- **🇮🇳 Indian Stock Market**: Native NSE/BSE support with accurate symbol conversion
- **📊 Real-time Data**: Yahoo Finance API integration with 66+ data points (3 months)
- **🤖 Advanced ML**: Neural network with 9 technical features + statistical fallback
- **📈 Interactive Charts**: Beautiful visualizations with historical & future predictions
- **⚡ Production Optimized**: Clean codebase, minimal logging, fast performance
- **🎯 High Accuracy**: AI confidence scoring (45-90%) with trend analysis
- **📱 Modern UI**: Responsive design with Tailwind CSS
- **�️ Robust**: Error handling, timeout protection, and smart fallbacks
- **🧹 Clean Architecture**: Well-structured and maintainable codebase

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
stock-predictor/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   └── stock/route.ts        # Yahoo Finance API integration
│   │   ├── globals.css               # Tailwind CSS styles
│   │   ├── layout.tsx               # App layout
│   │   └── page.tsx                 # ML prediction interface
│   ├── components/
│   │   └── StockChart.tsx           # Interactive financial charts
│   └── lib/
│       └── ml-utils.ts              # TensorFlow.js ML utilities
├── package.json                      # Dependencies & scripts
├── tailwind.config.ts               # Tailwind configuration
├── tsconfig.json                    # TypeScript configuration
└── README.md                        # Documentation
```

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Modern web browser with JavaScript enabled

### Key Features ✨

- ✅ **Production Ready**: Optimized build with minimal bundle size
- ✅ **Fast Performance**: Next.js 15 with Turbopack for rapid loading
- ✅ **Secure**: Clean API endpoints with proper error handling
- ✅ **Type-Safe**: Full TypeScript implementation for reliability

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
- **Clean Architecture**: Well-structured components and API endpoints
- **Essential Logging**: Production-ready with proper error handling
- **Optimized Bundle**: Minimal dependencies for fast loading
- **Security**: Secure API endpoints with proper validation

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
