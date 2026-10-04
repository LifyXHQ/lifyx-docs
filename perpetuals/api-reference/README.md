# LifyX Perpetual API Reference

Developer reference for public LifyX Perpetual market data and trading infrastructure.

## Overview

LifyX Perpetuals integrates Orderly infrastructure to provide decentralized perpetual trading, liquidity access, public market data and execution functionality.

This reference focuses on public perpetual market data workflows available through the integrated infrastructure.

## Infrastructure Provider

Orderly

## Production API

Base URL:

`https://api.orderly.org`

## Example Market

Examples commonly use:

`PERP_BTC_USDC`

Developers can replace this symbol with another supported LifyX Perpetual market.

## Public Market Data

### Available Markets

`GET /v1/public/info`

Returns available perpetual markets and trading rules.

Example:

`https://api.orderly.org/v1/public/info`

### Order Book

`GET /v1/public/orderbook/{symbol}`

Returns public bid and ask data for a selected perpetual market.

Example:

`https://api.orderly.org/v1/public/orderbook/PERP_BTC_USDC`

### Public Liquidation Data

`GET /v1/public/liquidated_positions`

Returns public liquidation information.

Example:

`https://api.orderly.org/v1/public/liquidated_positions`

## Official SDK Workflows

Some examples in the LifyX developer repository use the official Orderly SDK workflow.

### Funding Rate

`getPredictedFundingRateForOne(symbol)`

Retrieves the predicted funding rate for a selected perpetual market.

### Funding History

`getFundingRateHistoryForOneMarket(payload)`

Retrieves historical funding rate information.

### Futures Markets

`getFuturesInfoForAllMarkets()`

Retrieves information for available perpetual markets.

### Single Futures Market

`getFuturesForOneMarket(symbol)`

Retrieves market information for a selected perpetual market.

### Recent Trades

`getMarketTrades(symbol, limit)`

Retrieves recent public trades for a selected perpetual market.

### Kline Data

`getKline(symbol, type, limit)`

Retrieves candlestick market data for a selected perpetual market.

## Market Data Resources

LifyX Perpetual examples cover:

- Available markets
- Trading symbols
- Order book data
- Funding rates
- Funding history
- Mark prices
- Index prices
- Recent trades
- Kline data
- Market statistics
- Futures market information

## Code Examples

Public JavaScript examples are available in:

`lifyx-api-examples/examples/perpetuals/market-data/`

Repository:

https://github.com/LifyXHQ/lifyx-api-examples

Available examples include:

- `get-public-data.js`
- `get-markets.js`
- `get-order-book.js`
- `get-funding-rate.js`
- `get-funding-history.js`
- `get-futures-info.js`
- `get-futures-market.js`
- `get-mark-price.js`
- `get-index-price.js`
- `get-recent-trades.js`
- `get-kline.js`
- `get-market-stats.js`

## Security

Public market data endpoints should not require:

- Private keys
- Seed phrases
- Wallet credentials

Never expose:

- Private keys
- API secrets
- Wallet credentials
- Environment secrets

Use secure secret management for authenticated integrations.

## Documentation

LifyX Developer Documentation:

https://github.com/LifyXHQ/lifyx-docs

Orderly:

https://github.com/OrderlyNetwork

## Official Links

Website: https://lifyx.exchange

Trading Platform: https://dex.lifyx.exchange

GitHub: https://github.com/LifyXHQ

Support: support@lifyx.exchange

---

© 2026 LifyX. All rights reserved.
