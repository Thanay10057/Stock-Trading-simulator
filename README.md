# Stock-Trading-simulator
This code creates a basic paper trading interface where you can "buy" and "sell" stocks using mock data. 
Of course. Here is a README file for the Stock Trading Simulator project.

-----

# Stock Trading Simulator 📈

A simple, client-side stock trading simulator built with vanilla HTML, CSS, and JavaScript. This project provides a paper trading interface where users can practice buying and selling stocks using a starting virtual cash balance. All stock prices are simulated using a mock function, making it easy to run without any API keys.

-----

## Features

  * **Virtual Portfolio:** Start with **$10,000** in virtual cash.
  * **Buy & Sell Stocks:** Execute buy and sell orders for any stock ticker.
  * **Dynamic Portfolio Tracking:** See your cash balance, holdings, and total portfolio value update in real-time after each transaction.
  * **Transaction Validation:** The application prevents you from buying stocks if you don't have enough cash or selling stocks you don't own.
  * **Clean UI:** A responsive and easy-to-use interface for managing your trades and portfolio.

-----

## Technologies Used

  * **HTML5:** For the basic structure and content.
  * **CSS3:** For styling and layout, including Flexbox for a responsive design.
  * **JavaScript (ES6+):** For all the application logic, including state management, event handling, and DOM manipulation.

-----

## How to Run Locally

No complex setup is required. Just follow these steps:

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/stock-trading-simulator.git
    ```

2.  **Navigate to the project directory:**

    ```bash
    cd stock-trading-simulator
    ```

3.  **Open the `index.html` file in your web browser.** That's it\! You can start trading immediately.

-----

## How It Works

The application's logic is contained entirely within the `script.js` file.

  * **State Management:** A single `state` object holds the user's `cash` balance and an array of their `holdings`.
  * **Mock API:** The `fetchStockPrice(ticker)` function simulates an API call by returning a random price for any given stock ticker. This can easily be swapped out with a real financial data API like [Alpha Vantage](https://www.alphavantage.co/) or [Finnhub](https://finnhub.io/).
    ```javascript
    // To use a real API, replace this function
    async function fetchStockPrice(ticker) {
        // Simulate network delay
        await new Promise(resolve => setTimeout(resolve, 200));
        // Generate a random price for simulation
        return 50 + Math.random() * 250; 
    }
    ```
  * **UI Rendering:** The `renderUI()` function is called after every transaction. It recalculates all values and updates the HTML to reflect the current state of the portfolio.
