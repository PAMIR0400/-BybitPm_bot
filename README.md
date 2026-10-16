# Bybit Signal Bot — Telegram Mini App prototype

This first prototype is a responsive dark black/gold interface designed for mobile and desktop. It uses public Bybit V5 market endpoints only and does not need an API key for market data.

## Local preview
Open `index.html` in a modern browser. Use **Получить сигнал** to fetch public linear USDT tickers and hourly candles and compute a basic technical screening result.

## Current limitations
- The screener currently checks a curated watchlist of 20 major USDT perpetual symbols.
- Technical screening uses EMA(20/50/100), RSI(14), relative volume, and local range breakout checks.
- Displayed score is a rule-match score, **not** a probability of profit.
- TP/SL values are heuristic ATR-based illustrative levels, not guaranteed targets.
- This is not a validated strategy and does not place or modify orders.
- Browser CORS or network restrictions may prevent direct REST requests in some environments; a production deployment should proxy market requests through a backend.
- Telegram bot authentication, persistent users/history, WebSocket streaming, full backtests, notifications, and AI provider integration are not implemented yet.

## Deployment on Render
Create a Static Site from this repository:
- Build command: leave blank (plain HTML)
- Publish directory: `.`
- Branch: `main`

No secrets are required for this static prototype. For production, move market-data requests into an API backend and add Telegram Mini App validation before adding authenticated features.
