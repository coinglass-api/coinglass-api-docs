# ETF - 索拉纳 ETF - 索拉纳ETF流入流出历史


```
GET /api/etf/solana//flow-history
```


该接口提供交易所交易基金（ETF）的索拉纳流入流出历史数据。

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

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

