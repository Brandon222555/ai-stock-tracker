# AI Stock Tracker — Live Portfolio Dashboard

A single-file, interactive stock tracker for 25 AI companies with live prices, portfolio allocation strategies, and deep-dive company analysis.

**[Live Demo](https://yourusername.github.io/ai-stock-tracker/)** *(update this link after deploying)*

## Features

- **25 AI Stocks** across 4 categories: Large Cap, Rising Stars, Comeback Kings, Pure Play
- **Live Prices** from Finnhub API with auto-refresh (1m / 5m / 15m / 1hr intervals)
- **Click Any Stock** for a detailed modal with open/high/low, trend chart, bull/bear thesis, and analyst targets
- **Editable Budget** — change your investment amount and everything recalculates instantly
- **5 Allocation Strategies** — Balanced, Conservative, Rising Stars, Comeback Kings, Aggressive
- **Performance Chart** with color-coded YTD returns
- **Market Status Indicator** — shows if US markets are open/closed/pre-market
- **Fully Responsive** — works on desktop, tablet, and mobile
- **Zero Dependencies** — single HTML file, no build step, no server needed

## Stocks Tracked

| Category | Tickers |
|----------|---------|
| Large Cap | NVDA, MSFT, GOOGL, META, AMZN |
| Rising Stars | MU, AVGO, TSM, AMD, CRWD, SNOW, ARM, CIEN |
| Comeback Kings | ORCL, CRM, ADBE, INTC, S, MRVL, SNAP |
| Pure Play | PLTR, AI, SOUN, BBAI, PATH |

## Quick Start

1. Download `index.html`
2. Open it in any browser
3. That's it — prices load automatically

## Deploy to GitHub Pages (Free Hosting)

See the step-by-step guide below to host this live on the internet for free.

### Step 1: Create a GitHub Account
Go to [github.com](https://github.com) and sign up (it's free).

### Step 2: Create a New Repository
1. Click the **+** button (top right) → **New repository**
2. Name it: `ai-stock-tracker`
3. Set it to **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

### Step 3: Upload Your Files
1. On your new repo page, click **"Add file"** → **"Upload files"**
2. Drag and drop `index.html` into the upload area
3. Click **"Commit changes"**

### Step 4: Enable GitHub Pages
1. Go to your repo's **Settings** tab
2. In the left sidebar, click **Pages**
3. Under "Source", select **Deploy from a branch**
4. Under "Branch", select **main** and **/ (root)**
5. Click **Save**
6. Wait 1-2 minutes, then your site will be live at:
   ```
   https://yourusername.github.io/ai-stock-tracker/
   ```

### Step 5: Share Your Link
Your dashboard is now live on the internet! Share the link with anyone.

## How the Auto-Refresh Works

The dashboard fetches live stock quotes from the [Finnhub API](https://finnhub.io/) (free tier). You can control the refresh interval with the buttons in the header:

| Button | Interval | Best For |
|--------|----------|----------|
| 1m | Every minute | Active trading hours |
| 5m | Every 5 minutes | Default — good balance |
| 15m | Every 15 minutes | Casual monitoring |
| 1h | Every hour | Set it and forget it |
| Off | Manual only | Save API calls |

The free Finnhub API key included has a limit of 60 calls/minute. With 25 stocks, each refresh uses 25 calls, so 1-minute refresh is the practical minimum.

## Get Your Own API Key (Optional)

The dashboard includes a demo Finnhub API key. For reliable long-term use:

1. Go to [finnhub.io](https://finnhub.io/)
2. Sign up for a free account
3. Copy your API key from the dashboard
4. In `index.html`, find this line near the top of the `<script>`:
   ```js
   const FINNHUB_KEY = 'cvt2mupr01qhb8co7ic0cvt2mupr01qhb8co7icg';
   ```
5. Replace the key with your own

## Customize

**Add a stock:** Find the `stocks` array in the `<script>` and add a new entry following the same format.

**Change strategies:** Edit the `strategies` array to adjust allocation percentages.

**Change default budget:** Update the `value="500"` in the budget input field.

## Disclaimer

This dashboard is for educational purposes only — not financial advice. Prices may be delayed. Past performance doesn't guarantee future results. Always do your own research.

## License

MIT — do whatever you want with it.
