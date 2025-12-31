# ETF - XRP ETF - XRP ETF流入流出历史


```
GET /api/etf/xrp//flow-history
```


该接口提供交易所交易基金（ETF）的XRP流入流出历史数据。

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

