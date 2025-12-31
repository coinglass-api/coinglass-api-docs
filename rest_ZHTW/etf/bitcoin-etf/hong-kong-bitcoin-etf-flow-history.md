# ETF - 比特幣 ETF - 香港 ETF 流入流出歷史


```
GET /api/hk-etf/bitcoin/flow-history
```


該接口提供香港市場中比特幣 ETF 的資金流入流出歷史數據。

***快取 / 更新頻率:*** 每 1天更新一次

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
      "timestamp": 1714435200000,                     // 日期（時間戳，單位毫秒）
      "flow_usd": 247866000,                          // 總資金流入（USD）
      "price_usd": 63842.4,                           // 當日BTC價格（USD）
      "etf_flows": [                                  // ETF資金流明細
        {
          "etf_ticker": "CHINAAMC",                   // ETF代碼
          "flow_usd": 123610690                       // 該ETF資金流入（USD）
        },
        {
          "etf_ticker": "HARVEST",                    // ETF代碼
          "flow_usd": 63138000                        // 該ETF資金流入（USD）
        },
        {
          "etf_ticker": "BOSERA&HASHKEY",             // ETF代碼
          "flow_usd": 61117310                        // 該ETF資金流入（USD）
        }
      ]
    },
    {
      "timestamp": 1714608000000,                     // 日期（時間戳，單位毫秒）
      "flow_usd": 10095060,                           // 總資金流入（USD）
      "price_usd": 58307.7,                           // 當日BTC價格（USD）
      "etf_flows": [
        {
          "etf_ticker": "CHINAAMC",                   // ETF代碼
          "flow_usd": 3053490                         // 該ETF資金流入（USD）
        },
        {
          "etf_ticker": "HARVEST",                    // ETF代碼
          "flow_usd": 5022000                         // 該ETF資金流入（USD）
        },
        {
          "etf_ticker": "BOSERA&HASHKEY",             // ETF代碼
          "flow_usd": 2019570                         // 該ETF資金流入（USD）
        }
      ]
    }
  ]
}

```

