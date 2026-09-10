# 📈 Stock Trading Platform

A full-stack stock trading platform inspired by modern brokerage applications such as Zerodha. The project provides a trading-style interface for viewing holdings, orders, positions, portfolio performance, and placing simulated stock orders.

The application is built using React for the frontend and dashboard, Node.js/Express for the backend, and MongoDB for persistent data storage.

## 🚀 Live Demo

**Frontend:**  
https://stock-trading-platform-one.vercel.app/

**GitHub Repository:**  
https://github.com/mansi2004mehra18/StockTradingPlatform

---

## ✨ Features

### 📊 Trading Dashboard

- View stock holdings and portfolio information
- Display quantity, average cost, LTP, current value, and P&L
- View net change and day change for holdings
- View current portfolio value and total investment
- Visualize stock data using charts

### 📋 Orders Management

- View placed orders
- Display instrument, quantity, price, and current value
- Submit new buy orders through the trading interface
- Store order details in MongoDB

### 📌 Positions

- View current trading positions
- Display product, instrument, quantity, average price, LTP, P&L, and change
- Calculate position-level profit and loss

### 💰 Portfolio Analytics

- Calculate current holding value using quantity and stock price
- Calculate profit and loss based on average cost and current value
- Display portfolio summaries
- Visualize holdings using Chart.js

### 🛒 Order Placement

- Interactive buy order window
- Enter stock quantity and price
- Select buy order action
- Send order information to the backend API

### 🌐 Landing Website

The project also includes a separate React-based landing website with sections for:

- Home
- Products
- Pricing
- About
- Support
- Account opening
- Navigation and footer

---

## 🛠️ Tech Stack

### Frontend

- React.js
- React Router
- Axios
- HTML
- CSS
- JavaScript

### Dashboard

- React.js
- Material UI
- Chart.js
- React Chart.js 2
- Axios
- React Router

### Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- CORS
- Body Parser
- dotenv

### Deployment

- Vercel
- Render

---

## 🏗️ Project Structure

```text
StockTradingPlatform/
│
├── backend/
│   ├── index.js
│   ├── model/
│   │   ├── HoldingsModel.js
│   │   ├── OrdersModel.js
│   │   └── PositionsModel.js
│   │
│   ├── schemas/
│   │   ├── HoldingsSchema.js
│   │   ├── OrdersSchema.js
│   │   └── PositionsSchema.js
│   │
│   └── package.json
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── landing_page/
│   │   ├── index.js
│   │   └── index.css
│   └── package.json
│
├── dashboard/
│   ├── public/
│   ├── src/
│   │   └── components/
│   │       ├── Dashboard.js
│   │       ├── Holdings.js
│   │       ├── Orders.js
│   │       ├── Positions.js
│   │       ├── Funds.js
│   │       ├── Summary.js
│   │       ├── BuyActionWindow.js
│   │       ├── DoughnoutChart.js
│   │       ├── VerticalGraph.js
│   │       └── ...
│   └── package.json
│
└── README.md
```

---

## 🔄 How It Works

The application follows a client-server architecture.

```text
React Frontend
      │
      ▼
Trading Dashboard
      │
      ▼
Axios API Requests
      │
      ▼
Node.js + Express Backend
      │
      ▼
MongoDB + Mongoose
```

The dashboard fetches holdings and order information through backend API endpoints and displays the returned data in tables and charts.

---

## 🔌 Backend API

The backend provides REST-style endpoints for managing trading data.

### Get All Holdings

```http
GET /allHoldings
```

Returns all stored holdings.

### Get All Positions

```http
GET /allPositions
```

Returns all stored positions.

### Get All Orders

```http
GET /allOrders
```

Returns all stored orders.

### Create New Order

```http
POST /newOrder
```

Creates and stores a new order using:

```json
{
  "name": "STOCK_NAME",
  "qty": 1,
  "price": 100,
  "mode": "BUY"
}
```

---

## 📈 Portfolio Calculations

The dashboard calculates important portfolio metrics from holdings data.

### Current Value

```text
Current Value = Stock Price × Quantity
```

### Profit / Loss

```text
P&L = (Current Price − Average Cost) × Quantity
```

These calculations are used to display portfolio performance and identify profitable or loss-making holdings.

---

## 📊 Data Visualization

The dashboard uses Chart.js to visualize stock holdings and portfolio data.

The holdings chart dynamically uses stock names as labels and stock prices as the corresponding dataset values.

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/mansi2004mehra18/StockTradingPlatform.git
cd StockTradingPlatform
```

### 2. Setup Backend

```bash
cd backend
npm install
```

Create a `.env` file inside the `backend` directory:

```env
MONGO_URL=your_mongodb_connection_string
PORT=3002
```

Start the backend:

```bash
npm start
```

### 3. Setup Frontend

Open a new terminal:

```bash
cd frontend
npm install
npm start
```

### 4. Setup Dashboard

Open another terminal:

```bash
cd dashboard
npm install
npm start
```

The frontend and dashboard can then be accessed through their respective local development servers.

---

## 🔐 Environment Variables

Sensitive configuration values are stored using environment variables.

```env
MONGO_URL=your_mongodb_connection_string
PORT=your_port
```

Do not commit `.env` files or database credentials to GitHub.

---

## 🌐 Deployment

The project uses:

- Vercel for the frontend deployment
- Render for backend deployment

The production application communicates with the deployed backend through HTTP API requests.

---

## 📌 Future Improvements

- Add real-time stock market data using a financial market API
- Implement complete user authentication and authorization
- Add user-specific portfolios
- Add sell-order functionality
- Add order history and transaction tracking
- Add watchlist functionality
- Add advanced portfolio analytics
- Add interactive stock price charts
- Add real-time P&L updates
- Add stock search functionality
- Improve mobile responsiveness
- Add automated testing
- Add stronger API validation and error handling

---

## 👩‍💻 Author

**Mansi Mehra**

B.Tech Mechanical Engineering  
IIEST Shibpur

GitHub:  
https://github.com/mansi2004mehra18
