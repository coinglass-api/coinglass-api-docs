# ETF - 比特币 ETF - ETF溢价/折扣历史


```
GET /api/etf/bitcoin/premium-discount/history
```


该接口提供比特币ETF的溢价或折扣率的历史数据，包括各ETF代码的净资产价值（NAV）、市场价格，以及对应的溢价/折扣百分比。

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
      "timestamp": 1706227200000,                 // 日期（时间戳，单位为毫秒）
      "list": [
        {
          "ticker": "GBTC",                       // ETF代码
          "nav_usd": 37.51,                        // 净资产价值（USD）
          "market_price_usd": 37.51,               // 市场价格（USD）
          "premium_discount_details": 0            // 溢价/折扣百分比
        },
        {
          "ticker": "IBIT",                       // ETF代码
          "nav_usd": 23.94,                        // 净资产价值（USD）
          "market_price_usd": 23.99,               // 市场价格（USD）
          "premium_discount_details": 0.22         // 溢价/折扣百分比
        },
        {
          "ticker": "FBTC",                       // ETF代码
          "nav_usd": 36.720807,                    // 净资产价值（USD）
          "market_price_usd": 36.75,               // 市场价格（USD）
          "premium_discount_details": 0.0795       // 溢价/折扣百分比
        }
      ]
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填 | 描述                       |
| ------ | ------ | -- | ------------------------ |
| ticker | string | NO | ETF 代码 (例如, GBTC, IBIT). |

