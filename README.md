# Stock Prediction AI App

Stock Prediction AI App is a frontend web app that lets users enter up to 3 stock tickers, fetches recent price data, and generates a short AI-style report with buy/hold/sell guidance in a playful tone.

## Live Demo

- https://stock-prediction-ai-app-d55.pages.dev/
- Access policy: this demo is currently protected by Cloudflare Access and only authorized emails can sign in.

## What the app does

1. User adds stock tickers (3+ characters per ticker, up to 3 tickers recommended by UI text).
2. App requests recent stock data from a Polygon proxy Worker:
   - `https://polygon-api-worker.sngweijie96.workers.dev`
3. App sends consolidated stock data to an OpenAI proxy Worker:
   - `https://openai-api-worker.sngweijie96.workers.dev`
4. The model returns a concise report (about 150 words) with buy/hold/sell style recommendations.
5. Report is rendered in the output panel.

## Tech Stack

- Frontend: HTML, CSS, vanilla JavaScript
- Build tool: Vite
- APIs via Cloudflare Workers:
  - Polygon data worker for market data
  - OpenAI worker for report generation

## Project Structure

- `index.html` - app layout and UI sections
- `index.css` - styling
- `index.js` - ticker input flow, API calls, and report rendering
- `utils/dates.js` - dynamic date range helpers for API requests
- `images/` - icons and UI assets

## Local Development

1. Install dependencies:

```bash
npm install
```

2. Start development server:

```bash
npm run dev
```

3. Build for production:

```bash
npm run build
```

4. Preview production build locally:

```bash
npm run preview
```

## Cloudflare Pages Settings

- Build command: `npm run build`
- Build output directory: `dist`

## Notes

- This project is for educational/demo purposes.
- It is not financial advice.
