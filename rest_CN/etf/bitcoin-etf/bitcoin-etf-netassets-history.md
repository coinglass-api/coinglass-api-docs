# ETF - 比特币 ETF - ETF净资产历史


```
GET /api/etf/bitcoin/net-assets/history
```


该接口提供比特币交易所交易基金（ETF）的历史净资产数据。

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
      "net_assets_usd": 51671409241.39,         // 净资产总额（USD）
      "change_usd": 655300000,                  // 当日资金变化（USD）
      "timestamp": 1704931200000,               // 日期（时间戳，单位毫秒）
      "price_usd": 46337.8                      // 当日BTC价格（USD）
    },
    {
      "net_assets_usd": 51874409241.39,         // 净资产总额（USD）
      "change_usd": 203000000,                  // 当日资金变化（USD）
      "timestamp": 1705017600000,               // 日期（时间戳，单位毫秒）
      "price_usd": 42788.9                      // 当日BTC价格（USD）
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填 | 描述                    |
| ------ | ------ | -- | --------------------- |
| ticker | string | NO | ETF 代码（例如：GBTC、IBIT）。 |

