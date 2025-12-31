# 关于本中文翻译版
* 中文文档由英文文档翻译而来，当中文文档内容与英文文档冲突时，以英文文档为准。

## CoinGlass API文档

* 所有于本文档内给出定义的包括但不限于接口，WebSocket，参数，响应等，可认为是CoinGlass官方提供的内容。
* 而所有未于本文档内给出的内容，CoinGlass均不承诺提供任何支持。

文档名 | 描述
------------ | ------------
[introduction_CN.md](./introduction_CN.md)    | CoinGlass API 介绍
[authentication_CN.md](./authentication_CN.md)    | CoinGlass API 身份验证
[errors-rate-limits_CN.md](./errors-rate-limits_CN.md)    | 错误码与频率限制
[rest-api_CN.md](./rest-api_CN.md)                      | CoinGlass REST API 
[web-socket-api_CN.md](./web-socket-api_CN.md)          | CoinGlass  WebSocket API




# CoinGlass API 接口总览

## 合约 - 交易市场

| 名称         | github链接                                                         | 文档链接                                                                         |
| ---------- | ---------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| 支持的币种      | [Link](./rest_CN/futu/trading-market/coins.md)                   | [Link](https://docs.coinglass.com/v4.0-zh/reference/coins)                   |
| 支持的交易所     | [Link](./rest_CN/futu/trading-market/supported-exchanges.md)     | [Link](https://docs.coinglass.com/v4.0-zh/reference/supported-exchanges)     |
| 支持的交易所和交易对 | [Link](./rest_CN/futu/trading-market/instruments.md)             | [Link](https://docs.coinglass.com/v4.0-zh/reference/instruments)             |
| 币种市场列表     | [Link](./rest_CN/futu/trading-market/coins-markets.md)           | [Link](https://docs.coinglass.com/v4.0-zh/reference/coins-markets)           |
| 交易对市场列表    | [Link](./rest_CN/futu/trading-market/pairs-markets.md)           | [Link](https://docs.coinglass.com/v4.0-zh/reference/pairs-markets)           |
| 币种涨跌幅      | [Link](./rest_CN/futu/trading-market/coins-price-change.md)      | [Link](https://docs.coinglass.com/v4.0-zh/reference/coins-price-change)      |
| 交易对K线历史    | [Link](./rest_CN/futu/trading-market/price-ohlc-history.md)      | [Link](https://docs.coinglass.com/v4.0-zh/reference/price-ohlc-history)      |
| 下架的交易所和交易对 | [Link](./rest_CN/futu/trading-market/delisted-exchange-pairs.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/delisted-exchange-pairs) |
| 交易所列表      | [Link](./rest_CN/futu/trading-market/exchange-rank.md)           | [Link](https://docs.coinglass.com/v4.0-zh/reference/exchange-rank)           |

## 合约 - 持仓

| 名称             | github链接                                                                             | 文档链接                                                                                              |
| -------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------- |
| 持仓历史(K线)       | [Link](./rest_CN/futu/open-interest/oi-ohlc-histroy.md)                              | [Link](https://docs.coinglass.com/v4.0-zh/reference/oi-ohlc-histroy)                              |
| 聚合持仓历史(K线)     | [Link](./rest_CN/futu/open-interest/oi-ohlc-aggregated-history.md)                   | [Link](https://docs.coinglass.com/v4.0-zh/reference/oi-ohlc-aggregated-history)                   |
| 聚合稳定币保证金持仓(K线) | [Link](./rest_CN/futu/open-interest/oi-ohlc-aggregated-stablecoin-margin-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/oi-ohlc-aggregated-stablecoin-margin-history) |
| 聚合币本位保证金持仓(K线) | [Link](./rest_CN/futu/open-interest/oi-ohlc-aggregated-coin-margin-history.md)       | [Link](https://docs.coinglass.com/v4.0-zh/reference/oi-ohlc-aggregated-coin-margin-history)       |
| 币种交易所持仓        | [Link](./rest_CN/futu/open-interest/oi-exchange-list.md)                             | [Link](https://docs.coinglass.com/v4.0-zh/reference/oi-exchange-list)                             |
| 币种交易所持仓历史      | [Link](./rest_CN/futu/open-interest/oi-exchange-history-chart.md)                    | [Link](https://docs.coinglass.com/v4.0-zh/reference/oi-exchange-history-chart)                    |

## 合约 - 资金费率

| 名称              | github链接                                                        | 文档链接                                                                          |
| --------------- | --------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| 资金费率历史(K线)      | [Link](./rest_CN/futu/funding-rate/fr-ohlc-histroy.md)          | [Link](https://docs.coinglass.com/v4.0-zh/reference/fr-ohlc-histroy)          |
| 持仓加权资金费率历史(K线)  | [Link](./rest_CN/futu/funding-rate/oi-weight-ohlc-history.md)   | [Link](https://docs.coinglass.com/v4.0-zh/reference/oi-weight-ohlc-history)   |
| 成交量加权资金费率历史(K线) | [Link](./rest_CN/futu/funding-rate/vol-weight-ohlc-history.md)  | [Link](https://docs.coinglass.com/v4.0-zh/reference/vol-weight-ohlc-history)  |
| 币种资金费率-交易所列表    | [Link](./rest_CN/futu/funding-rate/fr-exchange-list.md)         | [Link](https://docs.coinglass.com/v4.0-zh/reference/fr-exchange-list)         |
| 累计资金费率-交易所列表    | [Link](./rest_CN/futu/funding-rate/cumulative-exchange-list.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/cumulative-exchange-list) |
| 资金费率套利          | [Link](./rest_CN/futu/funding-rate/fr-arbitrage.md)             | [Link](https://docs.coinglass.com/v4.0-zh/reference/fr-arbitrage)             |

## 合约 - 多空比

| 名称         | github链接                                                                      | 文档链接                                                                                    |
| ---------- | ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| 交易对账户多空比历史 | [Link](./rest_CN/futu/long-short-ratio/global-longshort-account-ratio.md)     | [Link](https://docs.coinglass.com/v4.0-zh/reference/global-longshort-account-ratio)     |
| 大户账户数多空比历史 | [Link](./rest_CN/futu/long-short-ratio/top-longshort-account-ratio.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/top-longshort-account-ratio)        |
| 大户持仓多空比历史  | [Link](./rest_CN/futu/long-short-ratio/top-longshort-position-ratio.md)       | [Link](https://docs.coinglass.com/v4.0-zh/reference/top-longshort-position-ratio)       |
| 币种主动买卖比    | [Link](./rest_CN/futu/long-short-ratio/taker-buysell-volume-exchange-list.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/taker-buysell-volume-exchange-list) |
| 净持仓        | [Link](./rest_CN/futu/long-short-ratio/net-position.md)                                | [Link](https://docs.coinglass.com/v4.0-zh/reference/net-position)                                |
| 净持仓(v2)    | [Link](./rest_CN/futu/long-short-ratio/net-position-v2.md)                              | [Link](https://docs.coinglass.com/v4.0-zh/reference/net-position-v2)                              |

## 合约 - 爆仓与清算

| 名称            | github链接                                                                    | 文档链接                                                                                       |
| ------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| 交易对爆仓历史       | [Link](./rest_CN/futu/liquidation/liquidation-history.md)                   | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-history)                   |
| 币种爆仓历史        | [Link](./rest_CN/futu/liquidation/aggregated-liquidation-history.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/aggregated-liquidation-history)        |
| 交易所币种爆仓列表     | [Link](./rest_CN/futu/liquidation/liquidation-coin-list.md)                 | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-coin-list)                 |
| 币种交易所爆仓列表     | [Link](./rest_CN/futu/liquidation/liquidation-exchange-list.md)             | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-exchange-list)             |
| 爆仓订单          | [Link](./rest_CN/futu/liquidation/liquidation-order.md)                     | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-order)                     |
| 交易对清算热力图(模型1) | [Link](./rest_CN/futu/liquidation/liquidation-heatmap.md)                   | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-heatmap)                   |
| 交易对清算热力图(模型2) | [Link](./rest_CN/futu/liquidation/liquidation-heatmap-model2.md)            | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-heatmap-model2)            |
| 交易对清算热力图(模型3) | [Link](./rest_CN/futu/liquidation/liquidation-heatmap-model3.md)            | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-heatmap-model3)            |
| 币种清算热力图(模型1)  | [Link](./rest_CN/futu/liquidation/liquidation-aggregate-heatmap.md)         | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-aggregate-heatmap)         |
| 币种清算热力图(模型2)  | [Link](./rest_CN/futu/liquidation/liquidation-aggregate-heatmap-model2.md)  | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-aggregate-heatmap-model2)  |
| 币种清算热力图(模型3)  | [Link](./rest_CN/futu/liquidation/liquidation-aggregated-heatmap-model3.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-aggregated-heatmap-model3) |
| 交易对清算地图       | [Link](./rest_CN/futu/liquidation/liquidation-map.md)                       | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-map)                       |
| 币种清算地图        | [Link](./rest_CN/futu/liquidation/liquidation-aggregated-map.md)            | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-aggregated-map)            |
| 清算最大痛点        | [Link](./rest_CN/futu/liquidation/liquidation-max-pain.md)                  | [Link](https://docs.coinglass.com/v4.0-zh/reference/liquidation-max-pain)                  |

## 合约 - 订单薄

| 名称              | github链接                                                                  | 文档链接                                                                                      |
| --------------- | ------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 交易对挂单深度历史(±范围)  | [Link](./rest_CN/futu/order-book/futures-orderbook-history.md)            | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-orderbook-history)            |
| 币种聚合挂单深度历史(±范围) | [Link](./rest_CN/futu/order-book/futures-aggregated-orderbook-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-aggregated-orderbook-history) |
| 订单薄历史(热力图)      | [Link](./rest_CN/futu/order-book/orderbook-heatmap.md)                    | [Link](https://docs.coinglass.com/v4.0-zh/reference/orderbook-heatmap)                    |
| 大额订单薄           | [Link](./rest_CN/futu/order-book/large-orderbook.md)                      | [Link](https://docs.coinglass.com/v4.0-zh/reference/large-orderbook)                      |
| 大额订单薄历史         | [Link](./rest_CN/futu/order-book/large-orderbook-history.md)              | [Link](https://docs.coinglass.com/v4.0-zh/reference/large-orderbook-history)              |

## 合约 - Hyperliquid 仓位

| 名称               | github链接                                                             | 文档链接                                                                            |
| ---------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Hyperliquid 鲸鱼提醒 | [Link](./rest_CN/futu/whale-positions/hyperliquid-whale-alert.md)    | [Link](https://docs.coinglass.com/v4.0-zh/reference/hyperliquid-whale-alert)    |
| Hyperliquid 鲸鱼持仓 | [Link](./rest_CN/futu/whale-positions/hyperliquid-whale-position.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/hyperliquid-whale-position) |
| Hyperliquid 仓位   | [Link](./rest_CN/futu/whale-positions/hyperliquid-position.md)       | [Link](https://docs.coinglass.com/v4.0-zh/reference/hyperliquid-position)       |
| Hyperliquid 用户仓位 | [Link](./rest_CN/futu/whale-positions/hyperliquid-user-position.md)  | [Link](https://docs.coinglass.com/v4.0-zh/reference/hyperliquid-user-position)  |

## 合约 - 主动买卖

| 名称             | github链接                                                                          | 文档链接                                                                                         |
| -------------- | --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| 交易对主动买卖历史      | [Link](./rest_CN/futu/trading-history/taker-buysell-volume.md)                    | [Link](https://docs.coinglass.com/v4.0-zh/reference/taker-buysell-volume)                    |
| 币种主动买卖历史       | [Link](./rest_CN/futu/trading-history/aggregated-taker-buysell-volume-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/aggregated-taker-buysell-volume-history) |
| 足迹图历史(90天)     | [Link](./rest_CN/futu/trading-history/futures-footprint-history.md)               | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-footprint-history)               |
| 累计成交量差值（CVD）   | [Link](./rest_CN/futu/trading-history/futures-cvd-history.md)                     | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-cvd-history)                     |
| 聚合累计成交量差值（CVD） | [Link](./rest_CN/futu/trading-history/futures-aggregated-cvd-history.md)          | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-aggregated-cvd-history)          |

## 现货 - 交易市场

| 名称          | github链接                                                                 | 文档链接                                                                              |
| ----------- | ------------------------------------------------------------------------ | --------------------------------------------------------------------------------- |
| 支持的币种       | [Link](./rest_CN/spots/trading-market-1/spot-supported-coins.md)         | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-supported-coins)         |
| 支持的交易所和交易对  | [Link](./rest_CN/spots/trading-market-1/spot-suported-exchange-pairs.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-suported-exchange-pairs) |
| 币种市场列表      | [Link](./rest_CN/spots/trading-market-1/spot-coins-markets.md)           | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-coins-markets)           |
| 交易对市场列表     | [Link](./rest_CN/spots/trading-market-1/spot-pairs-markets.md)           | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-pairs-markets)           |
| 交易对价格历史(K线) | [Link](./rest_CN/spots/trading-market-1/price-history-1.md)              | [Link](https://docs.coinglass.com/v4.0-zh/reference/price-history-1)              |

## 现货 - 订单薄

| 名称              | github链接                                                          | 文档链接                                                                           |
| --------------- | ----------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| 交易对挂单深度历史(±范围)  | [Link](./rest_CN/spots/order-book-1/spot-orderbook-history.md)    | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-orderbook-history)    |
| 币种聚合挂单深度历史(±范围) | [Link](./rest_CN/spots/order-book-1/spot-aggregated-history.md)   | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-aggregated-history)   |
| 订单薄历史(热力图)      | [Link](./rest_CN/spots/order-book-1/orderbook-history-1.md)       | [Link](https://docs.coinglass.com/v4.0-zh/reference/orderbook-history-1)       |
| 大额订单薄           | [Link](./rest_CN/spots/order-book-1/large-limit-order-1.md)       | [Link](https://docs.coinglass.com/v4.0-zh/reference/large-limit-order-1)       |
| 大额订单薄历史         | [Link](./rest_CN/spots/order-book-1/large-orderbook-history-1.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/large-orderbook-history-1) |

## 现货 - 主动买卖

| 名称             | github链接                                                                       | 文档链接                                                                                       |
| -------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| 交易对主动买卖历史      | [Link](./rest_CN/spots/taker-buysell/spot-taker-buysell-ratio-history.md)      | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-taker-buysell-ratio-history)      |
| 币种主动买卖历史       | [Link](./rest_CN/spots/taker-buysell/spot-aggregated-taker-buysell-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-aggregated-taker-buysell-history) |
| 足迹图历史          | [Link](./rest_CN/spots/taker-buysell/足迹图历史-1.md)                               | [Link](https://docs.coinglass.com/v4.0-zh/reference/足迹图历史-1)                               |
| 累计成交量差值（CVD）   | [Link](./rest_CN/spots/taker-buysell/spot-cvd-history.md)                      | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-cvd-history)                      |
| 聚合累计成交量差值（CVD） | [Link](./rest_CN/spots/taker-buysell/spot-aggregated-cvd-history.md)           | [Link](https://docs.coinglass.com/v4.0-zh/reference/spot-aggregated-cvd-history)           |

## 期权

| 名称       | github链接                                                    | 文档链接                                                                                |
| -------- | ----------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 期权最大痛点   | [Link](./rest_CN/options/option-max-pain.md)                | [Link](https://docs.coinglass.com/v4.0-zh/reference/option-max-pain)                |
| 期权相关数据   | [Link](./rest_CN/options/info.md)                           | [Link](https://docs.coinglass.com/v4.0-zh/reference/info)                           |
| 交易所持仓历史  | [Link](./rest_CN/options/exchange-open-interest-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/exchange-open-interest-history) |
| 交易所成交量历史 | [Link](./rest_CN/options/exchange-volume-history.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/exchange-volume-history)        |

## 链上 - 交易所数据

| 名称       | github链接                                                           | 文档链接                                                                        |
| -------- | ------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| 交易所资产透明度 | [Link](./rest_CN/on-chain/exchange-data/exchange-assets.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/exchange-assets)        |
| 交易所余额列表  | [Link](./rest_CN/on-chain/exchange-data/exchange-balance-list.md)  | [Link](https://docs.coinglass.com/v4.0-zh/reference/exchange-balance-list)  |
| 交易所余额图表  | [Link](./rest_CN/on-chain/exchange-data/exchange-balance-chart.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/exchange-balance-chart) |

## 链上 - 链上转账

| 名称              | github链接                                                              | 文档链接                                                                            |
| --------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| 交易所链上转账（ERC-20） | [Link](./rest_CN/on-chain/transactions/exchange-onchain-transfers.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/exchange-onchain-transfers) |
| 大额转账            | [Link](./rest_CN/on-chain/transactions/whale-transfer.md)             | [Link](https://docs.coinglass.com/v4.0-zh/reference/whale-transfer)             |

## 链上 - 代币

| 名称     | github链接                                             | 文档链接                                                                  |
| ------ | ---------------------------------------------------- | --------------------------------------------------------------------- |
| 代币解锁列表 | [Link](./rest_CN/on-chain/token/coin-unlock-list.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/coin-unlock-list) |
| 代币解锁详情 | [Link](./rest_CN/on-chain/token/coin-vesting.md)     | [Link](https://docs.coinglass.com/v4.0-zh/reference/coin-vesting)     |

## ETF - 比特币 ETF

| 名称          | github链接                                                                  | 文档链接                                                                                      |
| ----------- | ------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 比特币ETF列表    | [Link](./rest_CN/etf/bitcoin-etf/bitcoin-etfs.md)                         | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-etfs)                         |
| 香港ETF流入流出历史 | [Link](./rest_CN/etf/bitcoin-etf/hong-kong-bitcoin-etf-flow-history.md)   | [Link](https://docs.coinglass.com/v4.0-zh/reference/hong-kong-bitcoin-etf-flow-history)   |
| ETF净资产历史    | [Link](./rest_CN/etf/bitcoin-etf/bitcoin-etf-netassets-history.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-etf-netassets-history)        |
| ETF流入流出历史   | [Link](./rest_CN/etf/bitcoin-etf/etf-flows-history.md)                    | [Link](https://docs.coinglass.com/v4.0-zh/reference/etf-flows-history)                    |
| ETF溢价/折扣历史  | [Link](./rest_CN/etf/bitcoin-etf/bitcoin-etf-premium-discount-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-etf-premium-discount-history) |
| 比特币ETF历史    | [Link](./rest_CN/etf/bitcoin-etf/etf-history.md)                          | [Link](https://docs.coinglass.com/v4.0-zh/reference/etf-history)                          |
| ETF价格历史     | [Link](./rest_CN/etf/bitcoin-etf/etf-price-ohlc-history.md)               | [Link](https://docs.coinglass.com/v4.0-zh/reference/etf-price-ohlc-history)               |
| 比特币ETF详情    | [Link](./rest_CN/etf/bitcoin-etf/etf-detail.md)                           | [Link](https://docs.coinglass.com/v4.0-zh/reference/etf-detail)                           |
| ETF资产管理规模   | [Link](./rest_CN/etf/bitcoin-etf/etf-spot-net-inflow.md)                  | [Link](https://docs.coinglass.com/v4.0-zh/reference/etf-spot-net-inflow)                  |

## ETF - 以太坊 ETF

| 名称           | github链接                                                        | 文档链接                                                                                |
| ------------ | --------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 以太坊ETF净资产历史  | [Link](./rest_CN/etf/eth-etf/ethereum-etf-netassets-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/ethereum-etf-netassets-history) |
| 以太坊ETF列表     | [Link](./rest_CN/etf/eth-etf/ethereum-etf-list.md)              | [Link](https://docs.coinglass.com/v4.0-zh/reference/ethereum-etf-list)              |
| 以太坊ETF流入流出历史 | [Link](./rest_CN/etf/eth-etf/ethereum-etf-flows-history.md)     | [Link](https://docs.coinglass.com/v4.0-zh/reference/ethereum-etf-flows-history)     |

## ETF - 灰度基金

| 名称     | github链接                                                     | 文档链接                                                                           |
| ------ | ------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| 灰度持仓列表 | [Link](./rest_CN/etf/grayscale/grayscale-holding-list.md)    | [Link](https://docs.coinglass.com/v4.0-zh/reference/grayscale-holding-list)    |
| 灰度溢价历史 | [Link](./rest_CN/etf/grayscale/grayscale-premium-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/grayscale-premium-history) |

## ETF - 索拉纳 ETF

| 名称           | github链接                                                  | 文档链接                                                                          |
| ------------ | --------------------------------------------------------- | ----------------------------------------------------------------------------- |
| 索拉纳ETF流入流出历史 | [Link](./rest_CN/etf/索拉纳-etf/solana-etf-flows-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/solana-etf-flows-history) |

## ETF - XRP ETF

| 名称            | github链接                                                       | 文档链接                                                                       |
| ------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------- |
| XRP ETF流入流出历史 | [Link](./rest_CN/etf/copy-of-索拉纳-etf/xrp-etf-flows-history.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/xrp-etf-flows-history) |

## 指标 - 合约指标

| 名称                | github链接                                                     | 文档链接                                                                         |
| ----------------- | ------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| 币种RSI列表           | [Link](./rest_CN/indic/futures-1/futures-rsi-list.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-rsi-list)        |
| 交易对RSI            | [Link](./rest_CN/indic/futures-1/futures-indicators-rsi.md)  | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-indicators-rsi)  |
| 移动平均线 (MA)        | [Link](./rest_CN/indic/futures-1/futures-indicators-ma.md)   | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-indicators-ma)   |
| 指数移动平均线 (EMA)     | [Link](./rest_CN/indic/futures-1/futures-indicators-ema.md)  | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-indicators-ema)  |
| 布林带指标 (BOLL)      | [Link](./rest_CN/indic/futures-1/futures-indicators-boll.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-indicators-boll) |
| 移动平均收敛发散指标 (MACD) | [Link](./rest_CN/indic/futures-1/futures-indicators-macd.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/futures-indicators-macd) |
| 合约基差              | [Link](./rest_CN/indic/futures-1/basis.md)                   | [Link](https://docs.coinglass.com/v4.0-zh/reference/basis)                   |
| 鲸鱼指数              | [Link](./rest_CN/indic/futures-1/whale-index.md)                    | [Link](https://docs.coinglass.com/v4.0-zh/reference/whale-index)                    |
| CGDI 指数           | [Link](./rest_CN/indic/futures-1/cgdi-index.md)                 | [Link](https://docs.coinglass.com/v4.0-zh/reference/cgdi-index)                 |
| CDRI 指数           | [Link](./rest_CN/indic/futures-1/cdri-index.md)              | [Link](https://docs.coinglass.com/v4.0-zh/reference/cdri-index)              |

## 指标 - 现货

| 名称             | github链接                                                      | 文档链接                                                                            |
| -------------- | ------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Coinbase溢价指数   | [Link](./rest_CN/indic/spots-1/coinbase-premium-index.md)     | [Link](https://docs.coinglass.com/v4.0-zh/reference/coinbase-premium-index)     |
| Bitfinex杠杆多空仓位 | [Link](./rest_CN/indic/spots-1/bitfinex-margin-long-short.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitfinex-margin-long-short) |
| 借贷利率           | [Link](./rest_CN/indic/spots-1/borrow-interest-rate.md)       | [Link](https://docs.coinglass.com/v4.0-zh/reference/borrow-interest-rate)       |

## 指标 - 其他指标

| 名称                  | github链接                                                             | 文档链接                                                                                     |
| ------------------- | -------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| 比特币Ahr999指标         | [Link](./rest_CN/indic/other/ahr999.md)                              | [Link](https://docs.coinglass.com/v4.0-zh/reference/ahr999)                              |
| 普尔倍数                | [Link](./rest_CN/indic/other/puell-multiple.md)                      | [Link](https://docs.coinglass.com/v4.0-zh/reference/puell-multiple)                      |
| 比特币流通量与年产量          | [Link](./rest_CN/indic/other/stock-flow.md)                          | [Link](https://docs.coinglass.com/v4.0-zh/reference/stock-flow)                          |
| Pi循环顶部指示器           | [Link](./rest_CN/indic/other/pi.md)                                  | [Link](https://docs.coinglass.com/v4.0-zh/reference/pi)                                  |
| 比特币黄金比例乘数           | [Link](./rest_CN/indic/other/golden-ratio-multiplier.md)             | [Link](https://docs.coinglass.com/v4.0-zh/reference/golden-ratio-multiplier)             |
| 比特币盈利日期             | [Link](./rest_CN/indic/other/bitcoin-profitable-days.md)             | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-profitable-days)             |
| 比特币彩虹图              | [Link](./rest_CN/indic/other/bitcoin-rainbow-chart.md)               | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-rainbow-chart)               |
| 恐惧与贪婪指数             | [Link](./rest_CN/indic/other/cryptofear-greedindex.md)               | [Link](https://docs.coinglass.com/v4.0-zh/reference/cryptofear-greedindex)               |
| 稳定币市值历史             | [Link](./rest_CN/indic/other/stablecoin-marketcap-history.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/stablecoin-marketcap-history)        |
| 比特币泡沫指数             | [Link](./rest_CN/indic/other/bitcoin-bubble-index.md)                | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-bubble-index)                |
| 牛市逃顶信号清单            | [Link](./rest_CN/indic/other/bull-market-peak-indicator.md)          | [Link](https://docs.coinglass.com/v4.0-zh/reference/bull-market-peak-indicator)          |
| 两年MA乘数指标            | [Link](./rest_CN/indic/other/tow-year-ma-multiplier.md)              | [Link](https://docs.coinglass.com/v4.0-zh/reference/tow-year-ma-multiplier)              |
| 200周移动平均热力图         | [Link](./rest_CN/indic/other/tow-hundred-week-moving-avg-heatmap.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/tow-hundred-week-moving-avg-heatmap) |
| 山寨币季节指数             | [Link](./rest_CN/indic/other/altcoin-season.md)                      | [Link](https://docs.coinglass.com/v4.0-zh/reference/altcoin-season)                      |
| 比特币短期持有者已实现利润率      | [Link](./rest_CN/indic/other/bitcoin-sth-sopr.md)                    | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-sth-sopr)                    |
| 比特币长期持有者已实现利润率      | [Link](./rest_CN/indic/other/bitcoin-lth-sopr.md)                    | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-lth-sopr)                    |
| 比特币短期持有者平均持仓成本      | [Link](./rest_CN/indic/other/bitcoin-sth-realized-price.md)          | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-sth-realized-price)          |
| 比特币长期持有者平均持仓成本      | [Link](./rest_CN/indic/other/bitcoin-lth-realized-price.md)          | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-lth-realized-price)          |
| 短期持有者持有比特币数量        | [Link](./rest_CN/indic/other/bitcoin-short-term-holder-supply.md)    | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-short-term-holder-supply)    |
| 长期持有者持有比特币数量        | [Link](./rest_CN/indic/other/bitcoin-long-term-holder-supply.md)     | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-long-term-holder-supply)     |
| 比特币 RHODL 比值        | [Link](./rest_CN/indic/other/bitcoin-rhodl-ratio.md)                 | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-rhodl-ratio)                 |
| 比特币新地址              | [Link](./rest_CN/indic/other/bitcoin-new-addresses.md)               | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-new-addresses)               |
| 比特币活跃地址             | [Link](./rest_CN/indic/other/bitcoin-active-addresses.md)            | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-active-addresses)            |
| 比特币储备风险             | [Link](./rest_CN/indic/other/bitcoin-reserve-risk.md)                | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-reserve-risk)                |
| 比特币未实现净盈亏 (NUPL)    | [Link](./rest_CN/indic/other/bitcoin-net-unrealized-profit-loss.md)  | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-net-unrealized-profit-loss)  |
| 比特币相关性              | [Link](./rest_CN/indic/other/bitcoin-correlation.md)                 | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-correlation)                 |
| 比特币宏观震荡指标(BMO)      | [Link](./rest_CN/indic/other/bitcoin-macro-oscillator.md)            | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-macro-oscillator)            |
| 期权持仓 vs 合约持仓        | [Link](./rest_CN/indic/other/option-vs-futures-oi-ratio.md)          | [Link](https://docs.coinglass.com/v4.0-zh/reference/option-vs-futures-oi-ratio)          |
| 比特币 vs 全球 M2 货币供应增长 | [Link](./rest_CN/indic/other/bitcoin-vs-global-m2-growth.md)         | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-vs-global-m2-growth)         |
| 比特币 vs 美国 M2 货币供应增长 | [Link](./rest_CN/indic/other/bitcoin-vs-us-m2-growth.md)             | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-vs-us-m2-growth)             |
| 比特币市值占比             | [Link](./rest_CN/indic/other/bitcoin-dominance.md)                   | [Link](https://docs.coinglass.com/v4.0-zh/reference/bitcoin-dominance)                   |
| 交易所资产透明度证明          | [Link](./rest_CN/indic/other/exchange_assets_transparency.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/exchange_assets_transparency)        |

## 其他 - 财经日历

| 名称   | github链接                                             | 文档链接                                                                         |
| ---- | ---------------------------------------------------- | ---------------------------------------------------------------------------- |
| 经济数据 | [Link](./rest_CN/other/financial-calender/economic-data.md)           | [Link](https://docs.coinglass.com/v4.0-zh/reference/economic-data)           |
| 财经事件 | [Link](./rest_CN/other/financial-calender/financial-events.md)        | [Link](https://docs.coinglass.com/v4.0-zh/reference/financial-events)        |
| 央行动态 | [Link](./rest_CN/other/financial-calender/central-bank-activities.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/central-bank-activities) |

## 其他 - 新闻、快讯

| 名称 | github链接                                  | 文档链接                                                                |
| -- | ----------------------------------------- | ------------------------------------------------------------------- |
| 新闻 | [Link](./rest_CN/other/news-newsflash/article-list.md)   | [Link](https://docs.coinglass.com/v4.0-zh/reference/article-list)   |
| 快讯 | [Link](./rest_CN/other/news-newsflash/newsflash-list.md) | [Link](https://docs.coinglass.com/v4.0-zh/reference/newsflash-list) |



### 更新日志

关于 API 和WebSocket方面的最新变动，请参考 [更新日志](https://docs.coinglass.com/v4.0-zh/reference/change-log)。

### 联系我们

* [CoinGlass API 支持](mailto:contact@coinglass.com)
  * 适合咨询关于 API 或者 Websocket 性能方面的疑问和困扰。
  * 可以咨询在文档上面没有的 API 问题。
* [CoinGlass API 支持](mailto:contact@coinglass.com)
  * 可以提问或者咨询关于 API 或者 Websocket 代码方面问题。
