# 關於本中文繁體翻譯版
* 中文繁體文檔由英文文檔翻譯而來，當中文繁體文檔內容與英文文檔衝突時，以英文文檔爲準。

## CoinGlass API文檔

* 所有於本文檔內給出定義的包括但不限於接口，WebSocket，參數，響應等，可認爲是CoinGlass官方提供的內容。
* 而所有未於本文檔內給出的內容，CoinGlass均不承諾提供任何支持。

文檔名 | 描述
------------ | ------------
[introduction_ZHTW.md](./introduction_ZHTW.md)    | CoinGlass API 介紹
[authentication_ZHTW.md](./authentication_ZHTW.md)    | CoinGlass API 身份驗証
[errors-rate-limits_ZHTW.md](./errors-rate-limits_ZHTW.md)    | 錯誤碼與頻率限製
[rest-api_ZHTW.md](./rest-api_ZHTW.md)                      | CoinGlass REST API 
[web-socket-api_ZHTW.md](./web-socket-api_ZHTW.md)          | CoinGlass  WebSocket API



# CoinGlass API 接口總覽

## 合約數據 - 交易市場

| 名稱         | github連結                                                           | 文件連結                                                                           |
| ---------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| 支持的幣種      | [Link](./rest_ZHTW/futu/trading-market/coins.md)                   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/coins)                   |
| 支持的交易所     | [Link](./rest_ZHTW/futu/trading-market/support-exchanges.md)       | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/support-exchanges)       |
| 支持的交易所和交易對 | [Link](./rest_ZHTW/futu/trading-market/instruments.md)             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/instruments)             |
| 幣種市場列表     | [Link](./rest_ZHTW/futu/trading-market/coins-markets.md)           | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/coins-markets)           |
| 交易對市場列表    | [Link](./rest_ZHTW/futu/trading-market/pairs-markets.md)           | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/pairs-markets)           |
| 幣種漲跌幅      | [Link](./rest_ZHTW/futu/trading-market/coins-price-change.md)      | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/coins-price-change)      |
| 交易對 K 線歷史  | [Link](./rest_ZHTW/futu/trading-market/price-ohlc-history.md)      | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/price-ohlc-history)      |
| 下架的交易所和交易對 | [Link](./rest_ZHTW/futu/trading-market/delisted-exchange-pairs.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/delisted-exchange-pairs) |
| 交易所列表      | [Link](./rest_ZHTW/futu/trading-market/exchange-list.md)           | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/exchange-list)           |

## 合約數據 - 持倉

| 名稱              | github連結                                                                               | 文件連結                                                                                                |
| --------------- | -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| 持倉歷史（K 線）       | [Link](./rest_ZHTW/futu/open-interest/oi-ohlc-histroy.md)                              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/oi-ohlc-histroy)                              |
| 聚合持倉歷史（K 線）     | [Link](./rest_ZHTW/futu/open-interest/oi-ohlc-aggregated-history.md)                   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/oi-ohlc-aggregated-history)                   |
| 聚合穩定幣保證金持倉（K 線） | [Link](./rest_ZHTW/futu/open-interest/oi-ohlc-aggregated-stablecoin-margin-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/oi-ohlc-aggregated-stablecoin-margin-history) |
| 聚合幣本位保證金持倉（K 線） | [Link](./rest_ZHTW/futu/open-interest/oi-ohlc-aggregated-coin-margin-history.md)       | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/oi-ohlc-aggregated-coin-margin-history)       |
| 幣種交易所持倉         | [Link](./rest_ZHTW/futu/open-interest/oi-exchange-list.md)                             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/oi-exchange-list)                             |
| 幣種交易所持倉歷史       | [Link](./rest_ZHTW/futu/open-interest/oi-exchange-history-chart.md)                    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/oi-exchange-history-chart)                    |

## 合約數據 - 資金費率

| 名稱               | github連結                                                          | 文件連結                                                                            |
| ---------------- | ----------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| 資金費率歷史（K 線）      | [Link](./rest_ZHTW/futu/funding-rate/fr-ohlc-histroy.md)          | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/fr-ohlc-histroy)          |
| 持倉加權資金費率歷史（K 線）  | [Link](./rest_ZHTW/futu/funding-rate/oi-weight-ohlc-history.md)   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/oi-weight-ohlc-history)   |
| 成交量加權資金費率歷史（K 線） | [Link](./rest_ZHTW/futu/funding-rate/vol-weight-ohlc-history.md)  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/vol-weight-ohlc-history)  |
| 幣種資金費率－交易所列表     | [Link](./rest_ZHTW/futu/funding-rate/fr-exchange-list.md)         | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/fr-exchange-list)         |
| 累計資金費率－交易所列表     | [Link](./rest_ZHTW/futu/funding-rate/cumulative-exchange-list.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/cumulative-exchange-list) |
| 資金費率套利           | [Link](./rest_ZHTW/futu/funding-rate/fr-arbitrage.md)             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/fr-arbitrage)             |

## 合約數據 - 多空比

| 名稱         | github連結                                                                        | 文件連結                                                                                      |
| ---------- | ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 交易對多空比歷史   | [Link](./rest_ZHTW/futu/long-short-ratio/global-longshort-account-ratio.md)     | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/global-longshort-account-ratio)     |
| 大戶帳戶數多空比歷史 | [Link](./rest_ZHTW/futu/long-short-ratio/top-longshort-account-ratio.md)        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/top-longshort-account-ratio)        |
| 大戶持倉多空比歷史  | [Link](./rest_ZHTW/futu/long-short-ratio/top-longshort-position-ratio.md)       | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/top-longshort-position-ratio)       |
| 幣種主動買賣比    | [Link](./rest_ZHTW/futu/long-short-ratio/taker-buysell-volume-exchange-list.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/taker-buysell-volume-exchange-list) |
| 淨持倉        | [Link](./rest_ZHTW/futu/long-short-ratio/淨持倉.md)                                | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/淨持倉)                                |
| 淨持倉(v2)    | [Link](./rest_ZHTW/futu/long-short-ratio/淨持倉v2.md)                              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/淨持倉v2)                              |

## 合約數據 - 爆倉與清算

| 名稱            | github連結                                                                      | 文件連結                                                                                         |
| ------------- | ----------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| 交易對爆倉歷史       | [Link](./rest_ZHTW/futu/liquidation/liquidation-history.md)                   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-history)                   |
| 幣種爆倉歷史        | [Link](./rest_ZHTW/futu/liquidation/aggregated-liquidation-history.md)        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/aggregated-liquidation-history)        |
| 交易所幣種爆倉列表     | [Link](./rest_ZHTW/futu/liquidation/liquidation-coin-list.md)                 | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-coin-list)                 |
| 幣種交易所爆倉列表     | [Link](./rest_ZHTW/futu/liquidation/liquidation-exchange-list.md)             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-exchange-list)             |
| 爆倉訂單          | [Link](./rest_ZHTW/futu/liquidation/liquidation-order.md)                     | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-order)                     |
| 交易對清算熱力圖（模型1） | [Link](./rest_ZHTW/futu/liquidation/liquidation-heatmap.md)                   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-heatmap)                   |
| 交易對清算熱力圖（模型2） | [Link](./rest_ZHTW/futu/liquidation/liquidation-heatmap-model2.md)            | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-heatmap-model2)            |
| 交易對清算熱力圖（模型3） | [Link](./rest_ZHTW/futu/liquidation/liquidation-heatmap-model3.md)            | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-heatmap-model3)            |
| 幣種清算熱力圖（模型1）  | [Link](./rest_ZHTW/futu/liquidation/liquidation-aggregate-heatmap.md)         | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-aggregate-heatmap)         |
| 幣種清算熱力圖（模型2）  | [Link](./rest_ZHTW/futu/liquidation/liquidation-aggregate-heatmap-model2.md)  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-aggregate-heatmap-model2)  |
| 幣種清算熱力圖（模型3）  | [Link](./rest_ZHTW/futu/liquidation/liquidation-aggregated-heatmap-model3.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-aggregated-heatmap-model3) |
| 交易對清算地圖       | [Link](./rest_ZHTW/futu/liquidation/liquidation-map.md)                       | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-map)                       |
| 幣種清算地圖        | [Link](./rest_ZHTW/futu/liquidation/liquidation-aggregated-map.md)            | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-aggregated-map)            |
| 清算最大痛點        | [Link](./rest_ZHTW/futu/liquidation/liquidation-max-pain.md)                  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/liquidation-max-pain)                  |

## 合約數據 - 訂單薄

| 名稱              | github連結                                                                    | 文件連結                                                                                        |
| --------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| 交易對掛單深度歷史（±範圍）  | [Link](./rest_ZHTW/futu/order-book/futures-orderbook-history.md)            | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-orderbook-history)            |
| 幣種聚合掛單深度歷史（±範圍） | [Link](./rest_ZHTW/futu/order-book/futures-aggregated-orderbook-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-aggregated-orderbook-history) |
| 訂單薄歷史（熱力圖）      | [Link](./rest_ZHTW/futu/order-book/orderbook-heatmap.md)                    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/orderbook-heatmap)                    |
| 大額訂單薄           | [Link](./rest_ZHTW/futu/order-book/large-orderbook.md)                      | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/large-orderbook)                      |
| 大額訂單薄歷史         | [Link](./rest_ZHTW/futu/order-book/large-orderbook-history.md)              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/large-orderbook-history)              |

## 合約數據 - Hyperliquid 倉位

| 名稱                | github連結                                                               | 文件連結                                                                              |
| ----------------- | ---------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Hyperliquid 鯨魚提醒  | [Link](./rest_ZHTW/futu/whale-positions/hyperliquid-whale-alert.md)    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/hyperliquid-whale-alert)    |
| Hyperliquid 鯨魚持倉  | [Link](./rest_ZHTW/futu/whale-positions/hyperliquid-whale-position.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/hyperliquid-whale-position) |
| Hyperliquid 倉位    | [Link](./rest_ZHTW/futu/whale-positions/hyperliquid-position.md)       | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/hyperliquid-position)       |
| Hyperliquid 使用者倉位 | [Link](./rest_ZHTW/futu/whale-positions/hyperliquid-user-position.md)  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/hyperliquid-user-position)  |

## 合約數據 - 主動買賣

| 名稱             | github連結                                                                            | 文件連結                                                                                           |
| -------------- | ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| 交易對主動買賣歷史      | [Link](./rest_ZHTW/futu/trading-history/taker-buysell-volume.md)                    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/taker-buysell-volume)                    |
| 幣種主動買賣歷史       | [Link](./rest_ZHTW/futu/trading-history/aggregated-taker-buysell-volume-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/aggregated-taker-buysell-volume-history) |
| 足跡圖歷史(90天)     | [Link](./rest_ZHTW/futu/trading-history/futures-footprint-history.md)               | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-footprint-history)               |
| 累計成交量差值（CVD）   | [Link](./rest_ZHTW/futu/trading-history/futures-cvd-history.md)                     | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-cvd-history)                     |
| 聚合累計成交量差值（CVD） | [Link](./rest_ZHTW/futu/trading-history/futures-aggregated-cvd-history.md)          | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-aggregated-cvd-history)          |

## 現貨 - 交易市場

| 名稱           | github連結                                                                   | 文件連結                                                                                |
| ------------ | -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 支持的幣種        | [Link](./rest_ZHTW/spots/trading-market-1/spot-supported-coins.md)         | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-supported-coins)         |
| 支持的交易所和交易對   | [Link](./rest_ZHTW/spots/trading-market-1/spot-suported-exchange-pairs.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-suported-exchange-pairs) |
| 幣種市場列表       | [Link](./rest_ZHTW/spots/trading-market-1/spot-coins-markets.md)           | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-coins-markets)           |
| 交易對市場列表      | [Link](./rest_ZHTW/spots/trading-market-1/spot-pairs-markets.md)           | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-pairs-markets)           |
| 交易對價格歷史（K 線） | [Link](./rest_ZHTW/spots/trading-market-1/price-history-1.md)              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/price-history-1)              |

## 現貨 - 訂單簿

| 名稱              | github連結                                                            | 文件連結                                                                             |
| --------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| 交易對掛單深度歷史（±範圍）  | [Link](./rest_ZHTW/spots/order-book-1/spot-orderbook-history.md)    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-orderbook-history)    |
| 幣種聚合掛單深度歷史（±範圍） | [Link](./rest_ZHTW/spots/order-book-1/spot-aggregated-history.md)   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-aggregated-history)   |
| 訂單簿歷史（熱力圖）      | [Link](./rest_ZHTW/spots/order-book-1/orderbook-history-1.md)       | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/orderbook-history-1)       |
| 大額訂單簿           | [Link](./rest_ZHTW/spots/order-book-1/large-limit-order-1.md)       | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/large-limit-order-1)       |
| 大額訂單簿歷史         | [Link](./rest_ZHTW/spots/order-book-1/large-orderbook-history-1.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/large-orderbook-history-1) |

## 現貨 - 主動買賣

| 名稱             | github連結                                                                         | 文件連結                                                                                         |
| -------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| 交易對主動買賣歷史      | [Link](./rest_ZHTW/spots/taker-buysell/spot-taker-buysell-ratio-history.md)      | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-taker-buysell-ratio-history)      |
| 幣種主動買賣歷史       | [Link](./rest_ZHTW/spots/taker-buysell/spot-aggregated-taker-buysell-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-aggregated-taker-buysell-history) |
| 足跡圖歷史(90天)     | [Link](./rest_ZHTW/spots/taker-buysell/spot-footprint.md)                        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-footprint)                        |
| 累計成交量差值（CVD）   | [Link](./rest_ZHTW/spots/taker-buysell/spot-cvd-history.md)                      | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-cvd-history)                      |
| 聚合累計成交量差值（CVD） | [Link](./rest_ZHTW/spots/taker-buysell/spot-aggregated-cvd-history.md)           | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/spot-aggregated-cvd-history)           |

## 期權

| 名稱       | github連結                                                      | 文件連結                                                                                  |
| -------- | ------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| 期權最大痛點   | [Link](./rest_ZHTW/options/option-max-pain.md)                | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/option-max-pain)                |
| 期權相關     | [Link](./rest_ZHTW/options/info.md)                           | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/info)                           |
| 交易所持倉歷史  | [Link](./rest_ZHTW/options/exchange-open-interest-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/exchange-open-interest-history) |
| 交易所成交量歷史 | [Link](./rest_ZHTW/options/exchange-volume-history.md)        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/exchange-volume-history)        |

## 鏈上 - 交易所數據

| 名稱       | github連結                                                             | 文件連結                                                                          |
| -------- | -------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| 交易所資產透明度 | [Link](./rest_ZHTW/on-chain/exchange-data/exchange-assets.md)        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/exchange-assets)        |
| 交易所餘額列表  | [Link](./rest_ZHTW/on-chain/exchange-data/exchange-balance-list.md)  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/exchange-balance-list)  |
| 交易所餘額圖表  | [Link](./rest_ZHTW/on-chain/exchange-data/exchange-balance-chart.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/exchange-balance-chart) |

## 鏈上 -  鏈上轉帳

| 名稱              | github連結                                                                | 文件連結                                                                              |
| --------------- | ----------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| 交易所鏈上轉帳（ERC-20） | [Link](./rest_ZHTW/on-chain/transactions/exchange-onchain-transfers.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/exchange-onchain-transfers) |
| 大額轉賬            | [Link](./rest_ZHTW/on-chain/transactions/whale-transfer.md)             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/whale-transfer)             |

## 鏈上 - 代幣

| 名稱     | github連結                                            | 文件連結                                                                    |
| ------ | --------------------------------------------------- | ----------------------------------------------------------------------- |
| 代幣解鎖列表 | [Link](./rest_ZHTW/on-chain/代幣/coin-unlock-list.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/coin-unlock-list) |
| 代幣解鎖詳情 | [Link](./rest_ZHTW/on-chain/代幣/coin-vesting.md)     | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/coin-vesting)     |

## ETF - 比特幣 ETF

| 名稱            | github連結                                                                    | 文件連結                                                                                        |
| ------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| 比特幣 ETF 列表    | [Link](./rest_ZHTW/etf/bitcoin-etf/bitcoin-etfs.md)                         | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-etfs)                         |
| 香港 ETF 流入流出歷史 | [Link](./rest_ZHTW/etf/bitcoin-etf/hong-kong-bitcoin-etf-flow-history.md)   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/hong-kong-bitcoin-etf-flow-history)   |
| ETF 淨資產歷史     | [Link](./rest_ZHTW/etf/bitcoin-etf/bitcoin-etf-netassets-history.md)        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-etf-netassets-history)        |
| ETF 流入流出歷史    | [Link](./rest_ZHTW/etf/bitcoin-etf/etf-flows-history.md)                    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/etf-flows-history)                    |
| ETF 溢價／折價歷史   | [Link](./rest_ZHTW/etf/bitcoin-etf/bitcoin-etf-premium-discount-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-etf-premium-discount-history) |
| 比特幣 ETF 歷史    | [Link](./rest_ZHTW/etf/bitcoin-etf/etf-history.md)                          | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/etf-history)                          |
| ETF 價格歷史      | [Link](./rest_ZHTW/etf/bitcoin-etf/etf-price-ohlc-history.md)               | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/etf-price-ohlc-history)               |
| 比特幣 ETF 詳情    | [Link](./rest_ZHTW/etf/bitcoin-etf/etf-detail.md)                           | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/etf-detail)                           |
| ETF 資產管理規模    | [Link](./rest_ZHTW/etf/bitcoin-etf/etf-spot-net-inflow.md)                  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/etf-spot-net-inflow)                  |

## ETF - 以太坊 ETF

| 名稱             | github連結                                                          | 文件連結                                                                                  |
| -------------- | ----------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| 以太坊 ETF 淨資產歷史  | [Link](./rest_ZHTW/etf/eth-etf/ethereum-etf-netassets-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/ethereum-etf-netassets-history) |
| 以太坊 ETF 列表     | [Link](./rest_ZHTW/etf/eth-etf/ethereum-etf-list.md)              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/ethereum-etf-list)              |
| 以太坊 ETF 流入流出歷史 | [Link](./rest_ZHTW/etf/eth-etf/ethereum-etf-flows-history.md)     | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/ethereum-etf-flows-history)     |

## ETF - 灰度基金

| 名稱     | github連結                                                       | 文件連結                                                                             |
| ------ | -------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| 灰度持倉列表 | [Link](./rest_ZHTW/etf/grayscale/grayscale-holding-list.md)    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/grayscale-holding-list)    |
| 灰度溢價歷史 | [Link](./rest_ZHTW/etf/grayscale/grayscale-premium-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/grayscale-premium-history) |

## ETF - 索拉納 ETF

| 名稱             | github連結                                                    | 文件連結                                                                            |
| -------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------------- |
| 索拉納 ETF 流入流出歷史 | [Link](./rest_ZHTW/etf/索拉納-etf/solana-etf-flows-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/solana-etf-flows-history) |

## ETF - XRP ETF

| 名稱             | github連結                                                         | 文件連結                                                                         |
| -------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| XRP ETF 流入流出歷史 | [Link](./rest_ZHTW/etf/copy-of-索拉納-etf/xrp-etf-flows-history.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/xrp-etf-flows-history) |

## 指標 - 合約指標

| 名稱               | github連結                                                       | 文件連結                                                                           |
| ---------------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| 幣種RSI 列表         | [Link](./rest_ZHTW/indic/futures-1/futures-rsi-list.md)        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-rsi-list)        |
| 交易對RSI           | [Link](./rest_ZHTW/indic/futures-1/futures-indicators-rsi.md)  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-indicators-rsi)  |
| 移動平均線 (MA)       | [Link](./rest_ZHTW/indic/futures-1/futures-indicators-ma.md)   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-indicators-ma)   |
| 指數移動平均線（EMA）     | [Link](./rest_ZHTW/indic/futures-1/futures-indicators-ema.md)  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-indicators-ema)  |
| 布林帶指標（BOLL）      | [Link](./rest_ZHTW/indic/futures-1/futures-indicators-boll.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-indicators-boll) |
| 移動平均收斂發散指標（MACD） | [Link](./rest_ZHTW/indic/futures-1/futures-indicators-macd.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/futures-indicators-macd) |
| 合約基差             | [Link](./rest_ZHTW/indic/futures-1/basis.md)                   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/basis)                   |
| 鯨魚指數             | [Link](./rest_ZHTW/indic/futures-1/whale-index.md)             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/whale-index)             |
| CGDI 指數          | [Link](./rest_ZHTW/indic/futures-1/cgdi-index.md)              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/cgdi-index)              |
| CDRI 指數          | [Link](./rest_ZHTW/indic/futures-1/cdri-index.md)              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/cdri-index)              |

## 指標 - 現貨

| 名稱              | github連結                                                        | 文件連結                                                                              |
| --------------- | --------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Coinbase 溢價指數   | [Link](./rest_ZHTW/indic/spots-1/coinbase-premium-index.md)     | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/coinbase-premium-index)     |
| Bitfinex 槓桿多空倉位 | [Link](./rest_ZHTW/indic/spots-1/bitfinex-margin-long-short.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitfinex-margin-long-short) |
| 借貸利率            | [Link](./rest_ZHTW/indic/spots-1/borrow-interest-rate.md)       | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/borrow-interest-rate)       |

## 指標 - 其他指標

| 名稱                  | github連結                                                               | 文件連結                                                                                       |
| ------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| 比特幣 Ahr999 指標       | [Link](./rest_ZHTW/indic/other/ahr999.md)                              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/ahr999)                              |
| 普爾倍數                | [Link](./rest_ZHTW/indic/other/puell-multiple.md)                      | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/puell-multiple)                      |
| 比特幣流通量與年產量          | [Link](./rest_ZHTW/indic/other/stock-flow.md)                          | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/stock-flow)                          |
| Pi 循環頂部指標           | [Link](./rest_ZHTW/indic/other/pi.md)                                  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/pi)                                  |
| 比特幣黃金比例乘數           | [Link](./rest_ZHTW/indic/other/golden-ratio-multiplier.md)             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/golden-ratio-multiplier)             |
| 比特幣盈利日期             | [Link](./rest_ZHTW/indic/other/bitcoin-profitable-days.md)             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-profitable-days)             |
| 比特幣彩虹圖              | [Link](./rest_ZHTW/indic/other/bitcoin-rainbow-chart.md)               | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-rainbow-chart)               |
| 恐懼與貪婪指數             | [Link](./rest_ZHTW/indic/other/cryptofear-greedindex.md)               | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/cryptofear-greedindex)               |
| 穩定幣市值歷史             | [Link](./rest_ZHTW/indic/other/stablecoin-marketcap-history.md)        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/stablecoin-marketcap-history)        |
| 比特幣泡沫指數             | [Link](./rest_ZHTW/indic/other/bitcoin-bubble-index.md)                | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-bubble-index)                |
| 牛市逃頂指數              | [Link](./rest_ZHTW/indic/other/bull-market-peak-indicator.md)          | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bull-market-peak-indicator)          |
| 兩年 MA 乘數指標          | [Link](./rest_ZHTW/indic/other/tow-year-ma-multiplier.md)              | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/tow-year-ma-multiplier)              |
| 200 週移動平均熱力圖        | [Link](./rest_ZHTW/indic/other/tow-hundred-week-moving-avg-heatmap.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/tow-hundred-week-moving-avg-heatmap) |
| 比特幣短期持有者已實現利潤率      | [Link](./rest_ZHTW/indic/other/bitcoin-sth-sopr.md)                    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-sth-sopr)                    |
| 比特幣長期持有者已實現利潤率      | [Link](./rest_ZHTW/indic/other/bitcoin-lth-sopr.md)                    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-lth-sopr)                    |
| 比特幣短期持有者平均持倉成本      | [Link](./rest_ZHTW/indic/other/bitcoin-sth-realized-price.md)          | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-sth-realized-price)          |
| 比特幣長期持有者平均持倉成本      | [Link](./rest_ZHTW/indic/other/bitcoin-lth-realized-price.md)          | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-lth-realized-price)          |
| 短期持有者持有比特幣數量        | [Link](./rest_ZHTW/indic/other/bitcoin-short-term-holder-supply.md)    | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-short-term-holder-supply)    |
| 長期持有者持有比特幣數量        | [Link](./rest_ZHTW/indic/other/bitcoin-long-term-holder-supply.md)     | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-long-term-holder-supply)     |
| 比特幣 RHODL 比值        | [Link](./rest_ZHTW/indic/other/bitcoin-rhodl-ratio.md)                 | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-rhodl-ratio)                 |
| 比特幣新地址              | [Link](./rest_ZHTW/indic/other/bitcoin-new-addresses.md)               | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-new-addresses)               |
| 比特幣活躍地址             | [Link](./rest_ZHTW/indic/other/bitcoin-active-addresses.md)            | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-active-addresses)            |
| 比特幣儲備風險             | [Link](./rest_ZHTW/indic/other/bitcoin-reserve-risk.md)                | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-reserve-risk)                |
| 比特幣未實現淨盈虧 (NUPL)    | [Link](./rest_ZHTW/indic/other/bitcoin-net-unrealized-profit-loss.md)  | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-net-unrealized-profit-loss)  |
| 比特幣相關性              | [Link](./rest_ZHTW/indic/other/bitcoin-correlation.md)                 | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-correlation)                 |
| 比特幣宏觀震盪指標(BMO)      | [Link](./rest_ZHTW/indic/other/bitcoin-macro-oscillator.md)            | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-macro-oscillator)            |
| 期權持倉 VS 合約持倉        | [Link](./rest_ZHTW/indic/other/option-vs-futures-oi-ratio.md)          | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/option-vs-futures-oi-ratio)          |
| 山寨幣季節指數             | [Link](./rest_ZHTW/indic/other/altcoin-season.md)                      | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/altcoin-season)                      |
| 比特幣 vs 全球 M2 貨幣供應增長 | [Link](./rest_ZHTW/indic/other/bitcoin-vs-global-m2-growth.md)         | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-vs-global-m2-growth)         |
| 比特幣 vs 美國 M2 貨幣供應增長 | [Link](./rest_ZHTW/indic/other/bitcoin-vs-us-m2-growth.md)             | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-vs-us-m2-growth)             |
| 比特幣市值佔比             | [Link](./rest_ZHTW/indic/other/bitcoin-dominance.md)                   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/bitcoin-dominance)                   |
| 交易所資產透明度證明          | [Link](./rest_ZHTW/indic/other/exchange_assets_transparency.md)        | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/exchange_assets_transparency)        |

## 其他 - 財經日曆

| 名稱   | github連結                                     | 文件連結                                                                 |
| ---- | -------------------------------------------- | -------------------------------------------------------------------- |
| 經濟數據 | [Link](./rest_ZHTW/其他/財經日曆/economic-data.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/economic-data) |

## 其他 - 新聞、快訊

| 名稱 | github連結                                       | 文件連結                                                                  |
| -- | ---------------------------------------------- | --------------------------------------------------------------------- |
| 新聞 | [Link](./rest_ZHTW/其他/新聞-快訊/article-list.md)   | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/article-list)   |
| 快訊 | [Link](./rest_ZHTW/其他/新聞-快訊/newsflash-list.md) | [Link](https://docs.coinglass.com/v4.0-zhtw/reference/newsflash-list) |



### 更新日誌

關於 API 和WebSocket方麵的最新變動，請參考 [更新日誌](https://docs.coinglass.com/v4.0-zhtw/reference/change-log)。

### 聯繫我們

* [CoinGlass API 支持](mailto:contact@coinglass.com)
  * 適合諮詢關於 API 或者 Websocket 性能方麵的疑問和睏擾。
  * 可以諮詢在文檔上麵沒有的 API 問題。
* [CoinGlass API 支持](mailto:contact@coinglass.com)
  * 可以提問或者諮詢關於 API 或者 Websocket 代碼方麵問題。
