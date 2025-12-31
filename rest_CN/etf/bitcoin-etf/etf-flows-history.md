# ETF - 比特币 ETF - ETF流入流出历史


```
GET /api/etf/bitcoin/flow-history
```


该接口提供比特币ETF的历史资金流入流出数据，包括每日的净流入和净流出（以美元计）、收盘价格，以及按ETF代码划分的资金流明细。

***缓存/ 更新频率 :*** 1天一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "timestamp": 1704931200000,                   // 日期（时间戳，单位毫秒）
      "flow_usd": 655300000,                         // 当日总资金流入（USD）
      "price_usd": 46663,                            // 当日BTC现价（USD）
      "etf_flows": [                                 // 各ETF的资金流入详情
        {
          "etf_ticker": "GBTC",                      // ETF代码
          "flow_usd": -95100000                      // 资金流出（USD）
        },
        {
          "etf_ticker": "IBIT",                      // ETF代码
          "flow_usd": 111700000                      // 资金流入（USD）
        },
        {
          "etf_ticker": "FBTC",                      // ETF代码
          "flow_usd": 227000000                      // 资金流入（USD）
        }
      ]
    }
  ]
}

```

