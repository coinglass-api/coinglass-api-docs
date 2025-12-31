# ETF - 比特币 ETF - 比特币ETF历史


```
GET /api/etf/bitcoin/history
```


该接口提供比特币ETF的历史数据，涵盖每个ETF代码的关键指标信息，包括市场价格、净资产价值（NAV）、溢价/折扣百分比、流通股数以及总净资产等。

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
      "assets_date": 1706486400000,           // 净资产对应日期（时间戳，毫秒）
      "btc_holdings": 496573.8166,            // BTC 持仓数量
      "market_date": 1706486400000,           // 市场价格对应日期（时间戳，毫秒）
      "market_price": 38.51,                  // 市场价格（USD）
      "name": "Grayscale Bitcoin Trust",      // ETF 名称
      "nav": 38.57,                           // 单位净值（Net Asset Value，USD）
      "net_assets": 21431132778.35,           // 总净资产（USD）
      "premium_discount": -0.16,              // 溢价/折扣百分比（负值为折扣）
      "shares_outstanding": 555700100,        // 已发行份额
      "ticker": "GBTC"                        // ETF 代码
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                          |
| ------ | ------ | --- | --------------------------- |
| ticker | string | YES | ETF 股票代码 (例如., GBTC, IBIT). |

