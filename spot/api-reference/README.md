# LifyX Spot API Reference

Developer reference for public LifyX Spot market data and trading infrastructure.

## Overview

LifyX Spot integrates KalqiX infrastructure to provide high-performance decentralized spot trading, market data and execution functionality.

This reference focuses on public Spot market data workflows available through the integrated infrastructure.

## Infrastructure Provider

KalqiX

## Production API

Base URL:

`https://api.kalqix.com/v1`

## Example Market

Examples commonly use:

`cbBTC_USDC`

Developers can replace this ticker with another supported LifyX Spot market.

## Public Endpoints

### Server Time

`GET /time`

Returns the current server time.

Example:

`https://api.kalqix.com/v1/time`

### Markets

`GET /markets`

Returns available Spot markets.

Example:

`https://api.kalqix.com/v1/markets`

### Market Price

`GET /markets/{ticker}/price`

Returns current price information for a selected market.

Example:

`https://api.kalqix.com/v1/markets/cbBTC_USDC/price`

### Order Book

`GET /markets/{ticker}/order-book`

Returns public bid and ask data for a selected market.

Example:

`https://api.kalqix.com/v1/markets/cbBTC_USDC/order-book`

### Recent Trades

`GET /markets/{ticker}/trades`

Returns recent public trades for a selected market.

Example:

`https://api.kalqix.com/v1/markets/cbBTC_USDC/trades`

## Spot Capabilities

LifyX Spot infrastructure is designed to support:

- Sub-10ms matching
- 250K+ transactions per second
- ZK-proven trades
- Private execution
- Professional order book trading
- High-performance market data
- API-ready trading infrastructure

## Code Examples

Public JavaScript examples are available in:

`lifyx-api-examples/examples/spot/market-data/`

Repository:

https://github.com/LifyXHQ/lifyx-api-examples

Available examples include:

- `get-server-time.js`
- `get-markets.js`
- `get-price.js`
- `get-order-book.js`
- `get-recent-trades.js`

## Security

Public market data endpoints should not require:

- Private keys
- Seed phrases
- Wallet credentials

Never expose private keys, API secrets or sensitive environment variables in public source code.

## Official Links

Website: https://lifyx.exchange

Trading Platform: https://app.lifyx.exchange

GitHub: https://github.com/LifyXHQ

Support: support@lifyx.exchange

---

© 2026 LifyX. All rights reserved.
