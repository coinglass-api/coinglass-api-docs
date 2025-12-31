# ETF - XRP ETF - XRP ETF 流入流出歷史


```
GET /api/etf/xrp/flow-history
```


該接口提供交易所交易基金（ETF）的XRP流入流出歷史數據。

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
      "timestamp": 1763078400000,
      "flow_usd": 243050000,
      "price_usd": 2.3212,
      "etf_flows": [
        {
          "etf_ticker": "XRPC",
          "flow_usd": 243050000
        },
        {
          "etf_ticker": "XRPZ"
        },
        {
          "etf_ticker": "XRP"
        },
        {
          "etf_ticker": "GXRP"
        }
      ]
    },
  ]
}

```

