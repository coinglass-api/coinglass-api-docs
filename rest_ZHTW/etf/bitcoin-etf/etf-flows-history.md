# ETF - 比特幣 ETF - ETF 流入流出歷史


```
GET /api/etf/bitcoin/flow-history
```


該接口提供比特幣 ETF 的歷史資金流入流出數據，包括每日的淨流入和淨流出（以美元計）、收盤價格，以及按 ETF 代碼劃分的資金流明細。

***快取 / 更新頻率:*** 每 1小時更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "timestamp": 1704931200000,                   // 日期（時間戳，單位毫秒）
      "flow_usd": 655300000,                         // 當日總資金流入（USD）
      "price_usd": 46663,                            // 當日BTC現價（USD）
      "etf_flows": [                                 // 各ETF的資金流入詳情
        {
          "etf_ticker": "GBTC",                      // ETF代碼
          "flow_usd": -95100000                      // 資金流出（USD）
        },
        {
          "etf_ticker": "IBIT",                      // ETF代碼
          "flow_usd": 111700000                      // 資金流入（USD）
        },
        {
          "etf_ticker": "FBTC",                      // ETF代碼
          "flow_usd": 227000000                      // 資金流入（USD）
        }
      ]
    }
  ]
}

```

