# ETF - 索拉納 ETF - 索拉納 ETF 流入流出歷史


```
GET /api/etf/solana/flow-history
```


該接口提供交易所交易基金（ETF）的索拉納流入流出歷史數據。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    {
      "timestamp": 1762473600000,
      "flow_usd": 12700000,
      "price_usd": 155.2,
      "etf_flows": [
        {
          "etf_ticker": "BSOL",
          "flow_usd": 11700000
        },
        {
          "etf_ticker": "VSOL"
        },
        {
          "etf_ticker": "FSOL"
        },
        {
          "etf_ticker": "TSOL"
        },
        {
          "etf_ticker": "GSOL",
          "flow_usd": 1000000
        }
      ]
    },
  ]
}

```

