# ETF - 比特币 ETF - 香港ETF流入流出历史


```
GET /api/hk-etf/bitcoin/flow-history
```


该接口提供香港市场中比特币ETF的资金流入流出历史数据。

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
      "timestamp": 1714435200000,                     // 日期（时间戳，单位毫秒）
      "flow_usd": 247866000,                          // 总资金流入（USD）
      "price_usd": 63842.4,                           // 当日BTC价格（USD）
      "etf_flows": [                                  // ETF资金流明细
        {
          "etf_ticker": "CHINAAMC",                   // ETF代码
          "flow_usd": 123610690                       // 该ETF资金流入（USD）
        },
        {
          "etf_ticker": "HARVEST",                    // ETF代码
          "flow_usd": 63138000                        // 该ETF资金流入（USD）
        },
        {
          "etf_ticker": "BOSERA&HASHKEY",             // ETF代码
          "flow_usd": 61117310                        // 该ETF资金流入（USD）
        }
      ]
    },
    {
      "timestamp": 1714608000000,                     // 日期（时间戳，单位毫秒）
      "flow_usd": 10095060,                           // 总资金流入（USD）
      "price_usd": 58307.7,                           // 当日BTC价格（USD）
      "etf_flows": [
        {
          "etf_ticker": "CHINAAMC",                   // ETF代码
          "flow_usd": 3053490                         // 该ETF资金流入（USD）
        },
        {
          "etf_ticker": "HARVEST",                    // ETF代码
          "flow_usd": 5022000                         // 该ETF资金流入（USD）
        },
        {
          "etf_ticker": "BOSERA&HASHKEY",             // ETF代码
          "flow_usd": 2019570                         // 该ETF资金流入（USD）
        }
      ]
    }
  ]
}

```

