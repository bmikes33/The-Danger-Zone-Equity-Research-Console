# SMB LLC Macro Research Dashboard — Claude Code Context

## What This Project Is

Single-file React dashboard (`index.html`) deployed to GitHub Pages for tracking macro regime, intermarket analysis, sector rotation, lifecycle-stage positioning, and individual trade setups. Updated through iterative Claude sessions — screenshots in, updated HTML out, push to GitHub, live in 60 seconds.

## Dashboard File Workflow

1. Work on `index.html` in this repo directory
2. Use `str_replace` or direct edits — never overwrite the whole file with a stale copy
3. Use `grep -n` to locate exact strings before editing
4. After edits: `git add index.html && git commit -m "Update: [date] [summary]" && git push`
5. Cache bypass on live site via query string: `?v=N`

## Framework: Lifecycle Valuation Model

Five stages with distinct valuation methods and technical approaches:

- **Young Growth** → EV/SAM, EV/Sales — avoid in bear markets
- **High Growth** → EV/Sales, EV/Gross Profit — avoid when VIX >25, HYG broken
- **Mature Growth** → Forward PE, PEG, P/FCF — selective (energy/non-rate-sensitive only in bear)
- **Maturity** → PE, EV/EBITDA — PRIMARY allocation in corrections/bear markets. Oscillator entries (RSI <35 + Stochastic crossover below 20)
- **Decline** → P/B, P/Liquidation — caution when credit stress elevated

## Framework: Technical Analysis

### Moving Average Conventions (CRITICAL — never misread these)
- **Volatility instruments (VIX, VVIX):** Blue = 10 SMA, Orange = 50 SMA
- **All other instruments:** White = 21 EMA, Orange = 50 SMA, Purple = 200 SMA

### Key Indicators
- MACD (12, 26, 9)
- RSI (14)
- Stochastics (%K/%D)
- Fibonacci retracements (0.382, 0.5, 0.618, 0.786)
- OBV (On Balance Volume)
- RVWAP

### Bear Market Rules
- Oversold bounces are selling opportunities, not buying opportunities
- Must see 200 SMA reclaim on CLOSING basis before upgrading regime
- Intraday touches without closes = failed rallies
- Credit (HYG) leads equities — HYG must confirm any equity recovery

## Framework: Intermarket Analysis (John Murphy)

- Rising yields → compress equity multiples (especially growth/duration)
- Falling dollar → supports commodities, metals, crypto
- Gold surging + equities rising = someone is wrong
- Oil above $100 = stagflationary, constrains Fed
- Copper = purest global growth bellwether
- MOVE above 100 = bond market stress, separate equity headwind
- VIX above 25 = elevated regime; above 30 = fear
- VVIX above 120 = warning; below 110 = all-clear
- JP 10Y above 2.50% = carry unwind trigger

## BMNR CSP Put Ladder Rules

- BMNR is an ETH-linked digital asset trust
- Never roll at delta below 0.80
- Top of ladder: 2-4 weeks duration; bottom layer: weekly
- Only add new top-layer strikes after price holds new level for 1-2 full daily closes
- Macro freeze rule: freeze new positions if BTC drops 3-8% in a single session
- Close tail positions at 90%+ profit capture with under 5 DTE
- Deep ITM strikes with minimal extrinsic value are capital-inefficient — roll or close
- BTC $62,300 = key structural level; breach projects BMNR into mid-teens
- ETH/BTC ratio above 0.035 = alt season signal (not there yet)

## Sector Rules

- XLI and XLC = highest-conviction hunting grounds in normal regimes
- IGV and XLF = explicit avoids
- Software/SaaS excluded regardless of composite score
- Sector chart health must be cross-referenced with lifecycle stage bias before adding any name

## Watchlist (Current)

### Long Candidates
- GAP, T, ERIC, CRH (deep research complete)

### Short Candidates
- RKLB, F, H

## Dashboard Update Process

When I share screenshots, here's the workflow:

1. **Read the screenshots** — extract all values, changes, percentages
2. **Update the MACRO object** — regime, regimeColor, desc, stageBias, sectors (sorted by performance), narrative, calendar, news
3. **Update INSTRUMENT_DETAILS** — value, change, signal, color, chartTime, levels, analysis, keyWatch for each instrument shown
4. **Update UPDATED timestamp**
5. **Intermarket synthesis** — cross-reference rates, credit, vol, commodities, currency before making regime calls
6. **Commit and push**

### Data in screenshots typically includes:
- Image 1: Volatility + equity indexes + factor ETFs
- Image 2: Rates, currency, metals, oil
- Image 3: Sector ETFs (XLK through IGV)
- Image 4: Individual stock watchlist
- Image 5: Crypto instruments
- Images 6-8: TradingView daily charts (read MAs, RSI, MACD, OBV, volume, Fibonacci, support/resistance)

## Communication Style

- Direct, numbers-first
- No restating context I've already provided
- Cross-reference competing reads critically — don't just affirm
- Correct chart misreads immediately when flagged
- Batch related edits for efficiency
- Regime assessment is progressive — update as new data arrives within a session
