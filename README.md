# Official Documentation for the CoinGlass APIs and WebSocket.

* WebSocket, endpoints, parameters, payloads, etc. described in the documents in this repository are considered **official** and **supported**.
* The use of any other WebSocket, endpoints, parameters, or payloads, etc. is **not supported**; **use them at your own risk and with no guarantees.**

Name | Description
------------ | ------------
[introduction.md](./introduction.md)    | CoinGlass API Introduction
[authentication.md](./authentication.md)    | CoinGlass API Authentication
[errors-rate-limits.md](./errors-rate-limits.md)    | Error codes and rate limits
[rest-api.md](./rest-api.md)                      | CoinGlass REST API 
[web-socket-api.md](./web-socket-api.md)          | CoinGlass  WebSocket API


#  CoinGlass API Endpoint Overview

## Futures - Trading Market

| Name                         | github                                                              | docs                                                                    |
| ---------------------------- | ------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Supported Coins              | [Link](./rest/Futures/Trading-Market/coins.md)                      | [Link](https://docs.coinglass.com/reference/coins)                      |
| Supported Exchanges          | [Link](./rest/Futures/Trading-Market/supported-exchanges.md)        | [Link](https://docs.coinglass.com/reference/supported-exchanges)        |
| Supported Exchange and Pairs | [Link](./rest/Futures/Trading-Market/instruments.md)                | [Link](https://docs.coinglass.com/reference/instruments)                |
| Coins Markets                | [Link](./rest/Futures/Trading-Market/coins-markets.md)              | [Link](https://docs.coinglass.com/reference/coins-markets)              |
| Pairs Markets                | [Link](./rest/Futures/Trading-Market/pairs-markets.md)              | [Link](https://docs.coinglass.com/reference/pairs-markets)              |
| Coins Price Change           | [Link](./rest/Futures/Trading-Market/coins-price-change.md)         | [Link](https://docs.coinglass.com/reference/coins-price-change)         |
| Price History (OHLC)         | [Link](./rest/Futures/Trading-Market/price-ohlc-history.md)         | [Link](https://docs.coinglass.com/reference/price-ohlc-history)         |
| Delisted Pairs               | [Link](./rest/Futures/Trading-Market/delisted-exchange-and-pair.md) | [Link](https://docs.coinglass.com/reference/delisted-exchange-and-pair) |
| Exchange Rank                | [Link](./rest/Futures/Trading-Market/exchange-list.md)              | [Link](https://docs.coinglass.com/reference/exchange-list)              |

## Futures - Open Interest

| Name                                        | github                                                                               | docs                                                                                      |
| ------------------------------------------- | ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| History (OHLC)                              | [Link](./rest/Futures/Open-Interest/oi-ohlc-histroy.md)                              | [Link](https://docs.coinglass.com/reference/oi-ohlc-histroy)                              |
| Aggregated History (OHLC)                   | [Link](./rest/Futures/Open-Interest/oi-ohlc-aggregated-history.md)                   | [Link](https://docs.coinglass.com/reference/oi-ohlc-aggregated-history)                   |
| Aggregated Stablecoin Margin History (OHLC) | [Link](./rest/Futures/Open-Interest/oi-ohlc-aggregated-stablecoin-margin-history.md) | [Link](https://docs.coinglass.com/reference/oi-ohlc-aggregated-stablecoin-margin-history) |
| Aggregated Coin Margin History (OHLC)       | [Link](./rest/Futures/Open-Interest/oi-ohlc-aggregated-coin-margin-history.md)       | [Link](https://docs.coinglass.com/reference/oi-ohlc-aggregated-coin-margin-history)       |
| Exchange List                               | [Link](./rest/Futures/Open-Interest/oi-exchange-list.md)                             | [Link](https://docs.coinglass.com/reference/oi-exchange-list)                             |
| Exchange History Chart                      | [Link](./rest/Futures/Open-Interest/oi-exchange-history-chart.md)                    | [Link](https://docs.coinglass.com/reference/oi-exchange-history-chart)                    |

## Futures - Funding Rate

| Name                      | github                                                          | docs                                                                  |
| ------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------------- |
| History (OHLC)            | [Link](./rest/Futures/Funding-Rate/fr-ohlc-histroy.md)          | [Link](https://docs.coinglass.com/reference/fr-ohlc-histroy)          |
| OI Weight History (OHLC)  | [Link](./rest/Futures/Funding-Rate/oi-weight-ohlc-history.md)   | [Link](https://docs.coinglass.com/reference/oi-weight-ohlc-history)   |
| Vol Weight History (OHLC) | [Link](./rest/Futures/Funding-Rate/vol-weight-ohlc-history.md)  | [Link](https://docs.coinglass.com/reference/vol-weight-ohlc-history)  |
| Exchange List             | [Link](./rest/Futures/Funding-Rate/fr-exchange-list.md)         | [Link](https://docs.coinglass.com/reference/fr-exchange-list)         |
| Cumulative Exchange List  | [Link](./rest/Futures/Funding-Rate/cumulative-exchange-list.md) | [Link](https://docs.coinglass.com/reference/cumulative-exchange-list) |
| Arbitrage                 | [Link](./rest/Futures/Funding-Rate/fr-arbitrage.md)             | [Link](https://docs.coinglass.com/reference/fr-arbitrage)             |

## Futures - Long-Short Ratio

| Name                          | github                                                                        | docs                                                                            |
| ----------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Global Account Ratio          | [Link](./rest/Futures/Long-Short-Ratio/global-longshort-account-ratio.md)     | [Link](https://docs.coinglass.com/reference/global-longshort-account-ratio)     |
| Top Account Ratio History     | [Link](./rest/Futures/Long-Short-Ratio/top-longshort-account-ratio.md)        | [Link](https://docs.coinglass.com/reference/top-longshort-account-ratio)        |
| Top Position Ratio History    | [Link](./rest/Futures/Long-Short-Ratio/top-longshort-position-ratio.md)       | [Link](https://docs.coinglass.com/reference/top-longshort-position-ratio)       |
| Exchange Taker Buy/Sell Ratio | [Link](./rest/Futures/Long-Short-Ratio/taker-buysell-volume-exchange-list.md) | [Link](https://docs.coinglass.com/reference/taker-buysell-volume-exchange-list) |
| Net Position                  | [Link](./rest/Futures/Long-Short-Ratio/net-position.md)                       | [Link](https://docs.coinglass.com/reference/net-position)                       |
| Net Position (v2)             | [Link](./rest/Futures/Long-Short-Ratio/net-position-v2.md)                    | [Link](https://docs.coinglass.com/reference/net-position-v2)                    |

## Futures - Liquidation

| Name                            | github                                                                      | docs                                                                               |
| ------------------------------- | --------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Pair Liquidation History        | [Link](./rest/Futures/Liquidation/liquidation-history.md)                   | [Link](https://docs.coinglass.com/reference/liquidation-history)                   |
| Coin Liquidation History        | [Link](./rest/Futures/Liquidation/aggregated-liquidation-history.md)        | [Link](https://docs.coinglass.com/reference/aggregated-liquidation-history)        |
| Liquidation Coin List           | [Link](./rest/Futures/Liquidation/liquidation-coin-list.md)                 | [Link](https://docs.coinglass.com/reference/liquidation-coin-list)                 |
| Liquidation Exchange List       | [Link](./rest/Futures/Liquidation/liquidation-exchange-list.md)             | [Link](https://docs.coinglass.com/reference/liquidation-exchange-list)             |
| Liquidation Order               | [Link](./rest/Futures/Liquidation/liquidation-order.md)                     | [Link](https://docs.coinglass.com/reference/liquidation-order)                     |
| Pair Liquidation Heatmap Model1 | [Link](./rest/Futures/Liquidation/liquidation-heatmap.md)                   | [Link](https://docs.coinglass.com/reference/liquidation-heatmap)                   |
| Pair Liquidation Heatmap Model2 | [Link](./rest/Futures/Liquidation/liquidation-heatmap-model2.md)            | [Link](https://docs.coinglass.com/reference/liquidation-heatmap-model2)            |
| Pair Liquidation Heatmap Model3 | [Link](./rest/Futures/Liquidation/liquidation-heatmap-model3.md)            | [Link](https://docs.coinglass.com/reference/liquidation-heatmap-model3)            |
| Coin Liquidation Heatmap Model1 | [Link](./rest/Futures/Liquidation/liquidation-aggregate-heatmap.md)         | [Link](https://docs.coinglass.com/reference/liquidation-aggregate-heatmap)         |
| Coin Liquidation Heatmap Model2 | [Link](./rest/Futures/Liquidation/liquidation-aggregate-heatmap-model2.md)  | [Link](https://docs.coinglass.com/reference/liquidation-aggregate-heatmap-model2)  |
| Coin Liquidation Heatmap Model3 | [Link](./rest/Futures/Liquidation/liquidation-aggregated-heatmap-model3.md) | [Link](https://docs.coinglass.com/reference/liquidation-aggregated-heatmap-model3) |
| Pair Liquidation Map            | [Link](./rest/Futures/Liquidation/liquidation-map.md)                       | [Link](https://docs.coinglass.com/reference/liquidation-map)                       |
| Coin Liquidation Map            | [Link](./rest/Futures/Liquidation/liquidation-aggregated-map.md)            | [Link](https://docs.coinglass.com/reference/liquidation-aggregated-map)            |
| Liquidation Max Pain            | [Link](./rest/Futures/Liquidation/liquidation-max-pain.md)                  | [Link](https://docs.coinglass.com/reference/liquidation-max-pain)                  |

## Futures - Order Book

| Name                                      | github                                                                    | docs                                                                              |
| ----------------------------------------- | ------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Pair Orderbook Bid&Ask(±range)            | [Link](./rest/Futures/Order-Book/futures-orderbook-history.md)            | [Link](https://docs.coinglass.com/reference/futures-orderbook-history)            |
| Coin Aggregated Orderbook Bid&Ask(±range) | [Link](./rest/Futures/Order-Book/futures-aggregated-orderbook-history.md) | [Link](https://docs.coinglass.com/reference/futures-aggregated-orderbook-history) |
| Orderbook Heatmap                         | [Link](./rest/Futures/Order-Book/orderbook-heatmap.md)                    | [Link](https://docs.coinglass.com/reference/orderbook-heatmap)                    |
| Large Orderbook                           | [Link](./rest/Futures/Order-Book/large-orderbook.md)                      | [Link](https://docs.coinglass.com/reference/large-orderbook)                      |
| Large Orderbook History                   | [Link](./rest/Futures/Order-Book/large-orderbook-history.md)              | [Link](https://docs.coinglass.com/reference/large-orderbook-history)              |

## Futures - Hyperliquid Positions

| Name                                      | github                                                                                   | docs                                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| Hyperliquid Whale Alert                   | [Link](./rest/Futures/Hyperliquid-Positions/hyperliquid-whale-alert.md)                  | [Link](https://docs.coinglass.com/reference/hyperliquid-whale-alert)                  |
| Hyperliquid Whale Position                | [Link](./rest/Futures/Hyperliquid-Positions/hyperliquid-whale-position.md)               | [Link](https://docs.coinglass.com/reference/hyperliquid-whale-position)               |
| Hyperliquid Wallet Positions by Coin      | [Link](./rest/Futures/Hyperliquid-Positions/hyperliquid-position.md)                     | [Link](https://docs.coinglass.com/reference/hyperliquid-position)                     |
| Hyperliquid Wallet Positions by Address   | [Link](./rest/Futures/Hyperliquid-Positions/hyperliquid-user-position.md)                | [Link](https://docs.coinglass.com/reference/hyperliquid-user-position)                |
| Hyperliquid Wallet Positions Distribution | [Link](./rest/Futures/Hyperliquid-Positions/hyperliquid-wallet-position-distribution.md) | [Link](https://docs.coinglass.com/reference/hyperliquid-wallet-position-distribution) |
| Hyperliquid Wallet PNL Distribution       | [Link](./rest/Futures/Hyperliquid-Positions/hyperliquid-wallet-pnl-distribution.md)      | [Link](https://docs.coinglass.com/reference/hyperliquid-wallet-pnl-distribution)      |

## Futures - Taker Buy/Sell

| Name                                     | github                                                                           | docs                                                                                 |
| ---------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Pair Taker Buy/Sell History              | [Link](./rest/Futures/Taker-Buy/Sell/taker-buysell-volume.md)                    | [Link](https://docs.coinglass.com/reference/taker-buysell-volume)                    |
| Coin Taker Buy/Sell History              | [Link](./rest/Futures/Taker-Buy/Sell/aggregated-taker-buysell-volume-history.md) | [Link](https://docs.coinglass.com/reference/aggregated-taker-buysell-volume-history) |
| Footprint History (90d)                  | [Link](./rest/Futures/Taker-Buy/Sell/futures-footprint.md)                       | [Link](https://docs.coinglass.com/reference/futures-footprint)                       |
| Cumulative Volume Delta (CVD)            | [Link](./rest/Futures/Taker-Buy/Sell/futures-cvd-history.md)                     | [Link](https://docs.coinglass.com/reference/futures-cvd-history)                     |
| Aggregated Cumulative Volume Delta (CVD) | [Link](./rest/Futures/Taker-Buy/Sell/futures-aggregated-cvd-history.md)          | [Link](https://docs.coinglass.com/reference/futures-aggregated-cvd-history)          |

## Spots - Trading market

| Name                        | github                                                              | docs                                                                      |
| --------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Supported Coins             | [Link](./rest/Spots/Trading-market/spot-supported-coins.md)         | [Link](https://docs.coinglass.com/reference/spot-supported-coins)         |
| Suported Exchange and Pairs | [Link](./rest/Spots/Trading-market/spot-suported-exchange-pairs.md) | [Link](https://docs.coinglass.com/reference/spot-suported-exchange-pairs) |
| Coins Markets               | [Link](./rest/Spots/Trading-market/spot-coins-markets.md)           | [Link](https://docs.coinglass.com/reference/spot-coins-markets)           |
| Pairs Markets               | [Link](./rest/Spots/Trading-market/spot-pairs-markets.md)           | [Link](https://docs.coinglass.com/reference/spot-pairs-markets)           |
| Price OHLC History          | [Link](./rest/Spots/Trading-market/price-history.md)                | [Link](https://docs.coinglass.com/reference/price-history)                |

## Spots - Order book

| Name                           | github                                                       | docs                                                                   |
| ------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------------------------- |
| Pair Orderbook Bid&Ask(±range) | [Link](./rest/Spots/Order-book/spot-orderbook-history.md)    | [Link](https://docs.coinglass.com/reference/spot-orderbook-history)    |
| Coin Orderbook Bid&Ask(±range) | [Link](./rest/Spots/Order-book/spot-aggregated-history.md)   | [Link](https://docs.coinglass.com/reference/spot-aggregated-history)   |
| Orderbook Heatmap              | [Link](./rest/Spots/Order-book/orderbook-history-1.md)       | [Link](https://docs.coinglass.com/reference/orderbook-history-1)       |
| Large Orderbook                | [Link](./rest/Spots/Order-book/large-limit-order-1.md)       | [Link](https://docs.coinglass.com/reference/large-limit-order-1)       |
| Large Orderbook History        | [Link](./rest/Spots/Order-book/large-orderbook-history-2.md) | [Link](https://docs.coinglass.com/reference/large-orderbook-history-2) |

## Spots - Taker Buy/Sell

| Name                                     | github                                                                       | docs                                                                               |
| ---------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Pair Taker Buy/Sell History              | [Link](./rest/Spots/Taker-Buy/Sell/spot-taker-buysell-ratio-history.md)      | [Link](https://docs.coinglass.com/reference/spot-taker-buysell-ratio-history)      |
| Coin Taker Buy/Sell History              | [Link](./rest/Spots/Taker-Buy/Sell/spot-aggregated-taker-buysell-history.md) | [Link](https://docs.coinglass.com/reference/spot-aggregated-taker-buysell-history) |
| Footprint History (90d)                  | [Link](./rest/Spots/Taker-Buy/Sell/spot-footprint.md)                        | [Link](https://docs.coinglass.com/reference/spot-footprint)                        |
| Cumulative Volume Delta (CVD)            | [Link](./rest/Spots/Taker-Buy/Sell/spot-cvd-history.md)                      | [Link](https://docs.coinglass.com/reference/spot-cvd-history)                      |
| Aggregated Cumulative Volume Delta (CVD) | [Link](./rest/Spots/Taker-Buy/Sell/spot-aggregated-cvd-history.md)           | [Link](https://docs.coinglass.com/reference/spot-aggregated-cvd-history)           |

## Options

| Name                           | github                                                   | docs                                                                        |
| ------------------------------ | -------------------------------------------------------- | --------------------------------------------------------------------------- |
| Option Max Pain                | [Link](./rest/Options/option-max-pain.md)                | [Link](https://docs.coinglass.com/reference/option-max-pain)                |
| Options Info                   | [Link](./rest/Options/info.md)                           | [Link](https://docs.coinglass.com/reference/info)                           |
| Exchange Open Interest History | [Link](./rest/Options/exchange-open-interest-history.md) | [Link](https://docs.coinglass.com/reference/exchange-open-interest-history) |
| Exchange Volume History        | [Link](./rest/Options/exchange-volume-history.md)        | [Link](https://docs.coinglass.com/reference/exchange-volume-history)        |

## On-Chain - Exchange data

| Name                   | github                                                          | docs                                                                |
| ---------------------- | --------------------------------------------------------------- | ------------------------------------------------------------------- |
| Exchange Assets        | [Link](./rest/On-Chain/Exchange-data/exchange-assets.md)        | [Link](https://docs.coinglass.com/reference/exchange-assets)        |
| Exchange Balance List  | [Link](./rest/On-Chain/Exchange-data/exchange-balance-list.md)  | [Link](https://docs.coinglass.com/reference/exchange-balance-list)  |
| Exchange Balance Chart | [Link](./rest/On-Chain/Exchange-data/exchange-balance-chart.md) | [Link](https://docs.coinglass.com/reference/exchange-balance-chart) |

## On-Chain - Transactions

| Name                                 | github                                                             | docs                                                                    |
| ------------------------------------ | ------------------------------------------------------------------ | ----------------------------------------------------------------------- |
| Exchange On-chain Transfers (ERC-20) | [Link](./rest/On-Chain/Transactions/exchange-onchain-transfers.md) | [Link](https://docs.coinglass.com/reference/exchange-onchain-transfers) |
| Whale Transfer                       | [Link](./rest/On-Chain/Transactions/whale-transfer.md)             | [Link](https://docs.coinglass.com/reference/whale-transfer)             |

## On-Chain - Token

| Name              | github                                            | docs                                                          |
| ----------------- | ------------------------------------------------- | ------------------------------------------------------------- |
| Token Unlock List | [Link](./rest/On-Chain/Token/coin-unlock-list.md) | [Link](https://docs.coinglass.com/reference/coin-unlock-list) |
| Token Vesting     | [Link](./rest/On-Chain/Token/token-vesting.md)    | [Link](https://docs.coinglass.com/reference/token-vesting)    |

## ETF - Bitcoin ETF

| Name                         | github                                                                 | docs                                                                              |
| ---------------------------- | ---------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Bitcoin ETF List             | [Link](./rest/ETF/Bitcoin-ETF/bitcoin-etfs.md)                         | [Link](https://docs.coinglass.com/reference/bitcoin-etfs)                         |
| Hong Kong ETF Flows History  | [Link](./rest/ETF/Bitcoin-ETF/hong-kong-bitcoin-etf-flow-history.md)   | [Link](https://docs.coinglass.com/reference/hong-kong-bitcoin-etf-flow-history)   |
| ETF NetAssets History        | [Link](./rest/ETF/Bitcoin-ETF/bitcoin-etf-netassets-history.md)        | [Link](https://docs.coinglass.com/reference/bitcoin-etf-netassets-history)        |
| ETF Flows History            | [Link](./rest/ETF/Bitcoin-ETF/etf-flows-history.md)                    | [Link](https://docs.coinglass.com/reference/etf-flows-history)                    |
| ETF Premium/Discount History | [Link](./rest/ETF/Bitcoin-ETF/bitcoin-etf-premium-discount-history.md) | [Link](https://docs.coinglass.com/reference/bitcoin-etf-premium-discount-history) |
| ETF History                  | [Link](./rest/ETF/Bitcoin-ETF/etf-history.md)                          | [Link](https://docs.coinglass.com/reference/etf-history)                          |
| ETF Price History            | [Link](./rest/ETF/Bitcoin-ETF/etf-price-ohlc-history.md)               | [Link](https://docs.coinglass.com/reference/etf-price-ohlc-history)               |
| ETF Detail                   | [Link](./rest/ETF/Bitcoin-ETF/etf-detail.md)                           | [Link](https://docs.coinglass.com/reference/etf-detail)                           |
| ETF AUM                      | [Link](./rest/ETF/Bitcoin-ETF/etf-aum.md)                              | [Link](https://docs.coinglass.com/reference/etf-aum)                              |

## ETF - Ethereum ETF

| Name                  | github                                                            | docs                                                                        |
| --------------------- | ----------------------------------------------------------------- | --------------------------------------------------------------------------- |
| ETF NetAssets History | [Link](./rest/ETF/Ethereum-ETF/ethereum-etf-netassets-history.md) | [Link](https://docs.coinglass.com/reference/ethereum-etf-netassets-history) |
| Ethereum ETF List     | [Link](./rest/ETF/Ethereum-ETF/ethereum-etf-list.md)              | [Link](https://docs.coinglass.com/reference/ethereum-etf-list)              |
| ETF Flows History     | [Link](./rest/ETF/Ethereum-ETF/ethereum-etf-flows-history.md)     | [Link](https://docs.coinglass.com/reference/ethereum-etf-flows-history)     |

## ETF - Grayscale

| Name            | github                                                    | docs                                                                   |
| --------------- | --------------------------------------------------------- | ---------------------------------------------------------------------- |
| Holdings List   | [Link](./rest/ETF/Grayscale/grayscale-holding-list.md)    | [Link](https://docs.coinglass.com/reference/grayscale-holding-list)    |
| Premium History | [Link](./rest/ETF/Grayscale/grayscale-premium-history.md) | [Link](https://docs.coinglass.com/reference/grayscale-premium-history) |

## ETF - Solana ETF

| Name              | github                                                    | docs                                                                  |
| ----------------- | --------------------------------------------------------- | --------------------------------------------------------------------- |
| ETF Flows History | [Link](./rest/ETF/Solana-ETF/solana-etf-flows-history.md) | [Link](https://docs.coinglass.com/reference/solana-etf-flows-history) |

## ETF - XRP ETF

| Name              | github                                              | docs                                                               |
| ----------------- | --------------------------------------------------- | ------------------------------------------------------------------ |
| ETF Flows History | [Link](./rest/ETF/XRP-ETF/xrp-etf-flows-history.md) | [Link](https://docs.coinglass.com/reference/xrp-etf-flows-history) |

## Indic - Futures

| Name                                         | github                                                  | docs                                                                 |
| -------------------------------------------- | ------------------------------------------------------- | -------------------------------------------------------------------- |
| Coin RSI List                                | [Link](./rest/Indic/Futures/futures-rsi-list.md)        | [Link](https://docs.coinglass.com/reference/futures-rsi-list)        |
| Pair RSI                                     | [Link](./rest/Indic/Futures/futures-indicators-rsi.md)  | [Link](https://docs.coinglass.com/reference/futures-indicators-rsi)  |
| Moving Average (MA)                          | [Link](./rest/Indic/Futures/futures-indicators-ma.md)   | [Link](https://docs.coinglass.com/reference/futures-indicators-ma)   |
| Exponential Moving Average (EMA)             | [Link](./rest/Indic/Futures/futures-indicators-ema.md)  | [Link](https://docs.coinglass.com/reference/futures-indicators-ema)  |
| Bollinger Bands (BOLL)                       | [Link](./rest/Indic/Futures/futures-indicators-boll.md) | [Link](https://docs.coinglass.com/reference/futures-indicators-boll) |
| Moving Average Convergence Divergence (MACD) | [Link](./rest/Indic/Futures/futures-indicators-macd.md) | [Link](https://docs.coinglass.com/reference/futures-indicators-macd) |
| Futures Basis                                | [Link](./rest/Indic/Futures/basis.md)                   | [Link](https://docs.coinglass.com/reference/basis)                   |
| Whale Index                                  | [Link](./rest/Indic/Futures/whale-index.md)             | [Link](https://docs.coinglass.com/reference/whale-index)             |
| CGDI Index                                   | [Link](./rest/Indic/Futures/cgdi-index.md)              | [Link](https://docs.coinglass.com/reference/cgdi-index)              |
| CDRI Index                                   | [Link](./rest/Indic/Futures/cdri-index.md)              | [Link](https://docs.coinglass.com/reference/cdri-index)              |

## Indic - Spots

| Name                       | github                                                   | docs                                                                    |
| -------------------------- | -------------------------------------------------------- | ----------------------------------------------------------------------- |
| Coinbase Premium Index     | [Link](./rest/Indic/Spots/coinbase-premium-index.md)     | [Link](https://docs.coinglass.com/reference/coinbase-premium-index)     |
| Bitfinex Margin Long/Short | [Link](./rest/Indic/Spots/bitfinex-margin-long-short.md) | [Link](https://docs.coinglass.com/reference/bitfinex-margin-long-short) |
| Borrow Interest Rate       | [Link](./rest/Indic/Spots/borrow-interest-rate.md)       | [Link](https://docs.coinglass.com/reference/borrow-interest-rate)       |

## Indic - Other

| Name                                     | github                                                                 | docs                                                                                  |
| ---------------------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| AHR999                                   | [Link](./rest/Indic/Other/ahr999.md)                                   | [Link](https://docs.coinglass.com/reference/ahr999)                                   |
| Bull Market Peak Indicators              | [Link](./rest/Indic/Other/bull-market-peak-indicator.md)               | [Link](https://docs.coinglass.com/reference/bull-market-peak-indicator)               |
| Puell-Multiple                           | [Link](./rest/Indic/Other/puell-multiple.md)                           | [Link](https://docs.coinglass.com/reference/puell-multiple)                           |
| Stock-to-Flow Model                      | [Link](./rest/Indic/Other/stock-flow.md)                               | [Link](https://docs.coinglass.com/reference/stock-flow)                               |
| Pi Cycle Top Indicator                   | [Link](./rest/Indic/Other/pi.md)                                       | [Link](https://docs.coinglass.com/reference/pi)                                       |
| Golden-Ratio-Multiplier                  | [Link](./rest/Indic/Other/golden-ratio-multiplier.md)                  | [Link](https://docs.coinglass.com/reference/golden-ratio-multiplier)                  |
| Bitcoin Profitable Days                  | [Link](./rest/Indic/Other/bitcoin-profitable-days.md)                  | [Link](https://docs.coinglass.com/reference/bitcoin-profitable-days)                  |
| Bitcoin-Rainbow-Chart                    | [Link](./rest/Indic/Other/bitcoin-rainbow-chart.md)                    | [Link](https://docs.coinglass.com/reference/bitcoin-rainbow-chart)                    |
| Crypto Fear & Greed Index                | [Link](./rest/Indic/Other/cryptofear-greedindex.md)                    | [Link](https://docs.coinglass.com/reference/cryptofear-greedindex)                    |
| StableCoin MarketCap History             | [Link](./rest/Indic/Other/stablecoin-marketcap-history.md)             | [Link](https://docs.coinglass.com/reference/stablecoin-marketcap-history)             |
| Bitcoin Bubble Index                     | [Link](./rest/Indic/Other/bitcoin-bubble-index.md)                     | [Link](https://docs.coinglass.com/reference/bitcoin-bubble-index)                     |
| Tow Year Ma Multiplier                   | [Link](./rest/Indic/Other/tow-year-ma-multiplier.md)                   | [Link](https://docs.coinglass.com/reference/tow-year-ma-multiplier)                   |
| 200-Week Moving Avg Heatmap              | [Link](./rest/Indic/Other/tow-hundred-week-moving-avg-heatmap.md)      | [Link](https://docs.coinglass.com/reference/tow-hundred-week-moving-avg-heatmap)      |
| Altcoin Season Index                     | [Link](./rest/Indic/Other/altcoin-season-index.md)                     | [Link](https://docs.coinglass.com/reference/altcoin-season-index)                     |
| Bitcoin Short Term Holder SOPR           | [Link](./rest/Indic/Other/bitcoin-short-term-holder-sopr.md)           | [Link](https://docs.coinglass.com/reference/bitcoin-short-term-holder-sopr)           |
| Bitcoin Long Term Holder SOPR            | [Link](./rest/Indic/Other/bitcoin-long-term-holder-sopr.md)            | [Link](https://docs.coinglass.com/reference/bitcoin-long-term-holder-sopr)            |
| Bitcoin Short Term Holder Realized Price | [Link](./rest/Indic/Other/bitcoin-short-term-holder-realized-price.md) | [Link](https://docs.coinglass.com/reference/bitcoin-short-term-holder-realized-price) |
| Bitcoin Long Term Holder Realized Price  | [Link](./rest/Indic/Other/bitcoin-long-term-holder-realized-price.md)  | [Link](https://docs.coinglass.com/reference/bitcoin-long-term-holder-realized-price)  |
| Bitcoin Short Term Holder Supply         | [Link](./rest/Indic/Other/bitcoin-short-term-holder-supply.md)         | [Link](https://docs.coinglass.com/reference/bitcoin-short-term-holder-supply)         |
| Bitcoin Long Term Holder Supply          | [Link](./rest/Indic/Other/bitcoin-long-term-holder-supply.md)          | [Link](https://docs.coinglass.com/reference/bitcoin-long-term-holder-supply)          |
| Bitcoin RHODL Ratio                      | [Link](./rest/Indic/Other/bitcoin-rhodl-ratio.md)                      | [Link](https://docs.coinglass.com/reference/bitcoin-rhodl-ratio)                      |
| Bitcoin Reserve Risk                     | [Link](./rest/Indic/Other/bitcoin-reserve-risk.md)                     | [Link](https://docs.coinglass.com/reference/bitcoin-reserve-risk)                     |
| Bitcoin Active Addresses                 | [Link](./rest/Indic/Other/bitcoin-active-addresses.md)                 | [Link](https://docs.coinglass.com/reference/bitcoin-active-addresses)                 |
| Bitcoin New Addresses                    | [Link](./rest/Indic/Other/bitcoin-new-addresses.md)                    | [Link](https://docs.coinglass.com/reference/bitcoin-new-addresses)                    |
| Bitcoin Net Unrealized PNL               | [Link](./rest/Indic/Other/bitcoin-net-unrealized-profitloss-nupl.md)   | [Link](https://docs.coinglass.com/reference/bitcoin-net-unrealized-profitloss-nupl)   |
| Bitcoin Correlations                     | [Link](./rest/Indic/Other/btc-correlations-gld-iwm-qqq-spy-tlt.md)     | [Link](https://docs.coinglass.com/reference/btc-correlations-gld-iwm-qqq-spy-tlt)     |
| Bitcoin Macro Oscillator (BMO)           | [Link](./rest/Indic/Other/bitcoin-macro-oscillator-bmo.md)             | [Link](https://docs.coinglass.com/reference/bitcoin-macro-oscillator-bmo)             |
| Options/Futures OI Ratio                 | [Link](./rest/Indic/Other/optionsfutures-oi-ratio.md)                  | [Link](https://docs.coinglass.com/reference/optionsfutures-oi-ratio)                  |
| Bitcoin vs Global M2 Supply & Growth     | [Link](./rest/Indic/Other/bitcoin-vs-global-m2-supply-growth.md)       | [Link](https://docs.coinglass.com/reference/bitcoin-vs-global-m2-supply-growth)       |
| Bitcoin vs US M2 Supply & Growth         | [Link](./rest/Indic/Other/bitcoin-vs-us-m2-supply-growth.md)           | [Link](https://docs.coinglass.com/reference/bitcoin-vs-us-m2-supply-growth)           |
| Bitcoin Dominance                        | [Link](./rest/Indic/Other/bitcoin-dominance.md)                        | [Link](https://docs.coinglass.com/reference/bitcoin-dominance)                        |
| Exchanges Assets Transparency            | [Link](./rest/Indic/Other/exchanges-assets-transparency.md)            | [Link](https://docs.coinglass.com/reference/exchanges-assets-transparency)            |
| Futures vs Spot Volume Ratio             | [Link](./rest/Indic/Other/futures-spot-volume-ratio.md)                | [Link](https://docs.coinglass.com/reference/futures-spot-volume-ratio)                |

## Other - Financial Calendar

| Name          | github                                                   | docs                                                       |
| ------------- | -------------------------------------------------------- | ---------------------------------------------------------- |
| Economic Data | [Link](./rest/Other/Financial-Calendar/economic-data.md) | [Link](https://docs.coinglass.com/reference/economic-data) |

## Other - News

| Name | github                                    | docs                                                      |
| ---- | ----------------------------------------- | --------------------------------------------------------- |
| News | [Link](./rest/Other/News/article-list.md) | [Link](https://docs.coinglass.com/reference/article-list) |


### Change log

Please refer to [CHANGE LOG](https://docs.coinglass.com/reference/change-log) for latest changes on our APIs and WebSocket.

### Contact Us

* [CoinGlass API Support](mailto:contact@coinglass.com)
  * For any questions regarding sudden drop in performance with the API and/or WebSockets.
  * For any general questions about the API not covered in the documentation.
* [CoinGlass API Support](mailto:contact@coinglass.com)
  * For any questions/help regarding code implementation with API and/or WebSockets.
