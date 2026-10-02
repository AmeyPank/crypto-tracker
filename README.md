# CryptoTracker 📈

A modern, responsive cryptocurrency tracking and analytics web application built with **React 18**, **Material UI**, and **Chart.js**, powered by the **CoinGecko API**. CryptoTracker provides real-time market data, interactive historical charts, watchlist management, and dark/light mode support.

---

## 🚀 Features

- **📊 Live Crypto Dashboard**: Explore top 100 cryptocurrencies ranked by market cap with real-time price updates, 24h percentage changes, market cap, and total volume.
- **🔍 Instant Search**: Filter coins in real time by name or symbol with debounced user experience.
- **🔲 Dual View Layout**: Switch effortlessly between visual **Grid Cards** and compact **List Views**.
- **📈 Interactive Historical Charts**: Analyze price trends, total volume, and market capitalization across multiple timeframes (7, 30, 60, 90, 120, and 365 days) powered by Chart.js.
- **⭐ Persistent Watchlist**: Bookmark favorite coins using localStorage so your tracked assets remain saved across sessions.
- **🌓 Dark & Light Theme**: Seamlessly toggle between dark and light themes with preference saved in localStorage.
- **📱 Fully Responsive**: Optimized for desktops, tablets, and smartphones with a custom mobile drawer navigation.
- **✨ Fluid Animations**: Smooth layout animations and card reveals powered by Framer Motion.
- **📄 Pagination & Navigation**: Smooth client-side pagination (10 coins/page) with a floating "Back to Top" shortcut button.

---

## 🛠️ Tech Stack

| Category | Technologies / Libraries |
| :--- | :--- |
| **Frontend Framework** | React 18 (Create React App) |
| **Routing** | React Router DOM v6 |
| **UI & Styling** | Material UI (MUI v5), MUI Icons, Custom CSS Variables |
| **Data Visualization** | Chart.js, React-Chartjs-2 |
| **Animations** | Framer Motion |
| **HTTP Client** | Axios |
| **Notifications & Sharing** | React Toastify, React Web Share |
| **Data Source** | [CoinGecko API](https://www.coingecko.com/en/api) |

---

## 📂 Project Structure

```text
crypto-tracker/
├── public/                     # Static assets and index.html
├── src/
│   ├── Assets/                 # Images, mockups, and vector graphics
│   ├── Components/             # Modular and reusable UI components
│   │   ├── Coin/               # Coin details page components (LineChart, CoinInfo, PriceToggle, SelectDays)
│   │   ├── Common/             # Global components (Header, Footer, Button, Loader, BackToTop)
│   │   ├── Compare/            # Coin comparison components (SelectCoin)
│   │   ├── DashBoard/          # Dashboard components (Grid, List, Pagination, Search, Tabs)
│   │   └── LandingPage/        # Hero section & CTA for the home page
│   ├── functions/              # Utility functions and API integrations
│   │   ├── addToWatchlist.js   # Adds coin ID to localStorage watchlist
│   │   ├── coinObject.js       # Normalizes API response to coin object
│   │   ├── convertDate.js      # Date formatter helper
│   │   ├── convertNumbers.js   # Formats large numbers (K, M, B)
│   │   ├── get100Coins.js      # Fetches top 100 cryptocurrencies
│   │   ├── getCoinData.js      # Fetches details for a single coin
│   │   ├── getCoinPrices.js    # Fetches market chart data (price/market cap/volume)
│   │   ├── hasBeenAdded.js     # Checks if coin is in watchlist
│   │   ├── removeFromWatchlist.js # Removes coin ID from localStorage
│   │   └── settingChartData.js # Prepares datasets and configs for Chart.js
│   ├── Pages/                  # Route-level views
│   │   ├── home.js             # Landing page
│   │   ├── Dashboard.js        # Main cryptocurrency listing & search
│   │   ├── Coin.js             # In-depth coin analytics and charts
│   │   ├── watchlist.js        # Saved coins view
│   │   └── Compare.js          # Coin comparison view
│   ├── App.css                 # Global theme colors and variables
│   ├── App.js                  # Application routing setup
│   ├── constants.js            # API base endpoints
│   ├── index.css               # Base CSS reset
│   └── index.js                # App entry point
├── package.json                # Project dependencies and npm scripts
└── README.md                   # Project documentation
```

---

## 🚦 Getting Started

### Prerequisites

Ensure you have the following installed on your machine:
- **Node.js** (v14.x, v16.x, or v18.x recommended)
- **npm** (v6.x or higher) or **yarn**

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd crypto-tracker
   ```

2. **Install project dependencies:**
   ```bash
   npm install
   ```

3. **Start the development server:**
   ```bash
   npm start
   ```

4. **Open in browser:**
   Navigate to [http://localhost:3000](http://localhost:3000) to view the application.

---

## 📜 Available Scripts

In the project root, you can run:

- **`npm start`**: Runs the app in development mode with hot-reloading at [http://localhost:3000](http://localhost:3000).
- **`npm test`**: Launches the test runner in interactive watch mode.
- **`npm run build`**: Compiles the production-ready build to the `build` directory with minified assets.
- **`npm run eject`**: Removes the single build tool dependency (Note: this is an irreversible action).

---

## 🌐 API Reference

Data is retrieved from the **CoinGecko Public API (v3)**:

- **Top Coins Market Data**:
  `GET https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=100&page=1&sparkline=false`
- **Single Coin Details**:
  `GET https://api.coingecko.com/api/v3/coins/{id}`
- **Historical Market Data**:
  `GET https://api.coingecko.com/api/v3/coins/{id}/market_chart?vs_currency=usd&days={days}&interval=daily`

> **Note:** CoinGecko's free public tier has a rate limit (approximately 10–30 requests/minute). If data does not load immediately, wait a minute or consider configuring an API key.

---

## 🔮 Roadmap & Upcoming Features

- [ ] Complete the **Compare Page** for side-by-side coin comparison.
- [ ] Multi-currency support (e.g., EUR, GBP, INR, JPY).
- [ ] Real-time crypto price alerts and notifications.
- [ ] Conversion calculator / exchange calculator widget.

---

## 🤝 Acknowledgements

- Built as part of the **AccioJob Frontend Project** program.
- Cryptocurrency market data provided by [CoinGecko API](https://www.coingecko.com/).
