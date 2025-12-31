# ETF - 灰度基金 - 灰度持仓列表


```
GET /api/grayscale/holdings-list
```


该接口提供由 Grayscale Investments（灰度投资）管理的资产持仓列表

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
      "symbol": "ETH",                                  // 币种代码，例如 ETH 代表以太坊
      "primary_market_price": 29.89,                    // 一级市场价格
      "secondary_market_price": 29.71,                  // 二级市场价格
      "premium_rate": -0.6,                             // 溢价率（单位：%）
      "holdings_amount": 2630007.61026,                 // 当前持仓数量（单位：币）
      "holdings_usd": 4290752215.8347797,               // 当前持仓总市值（单位：USD）
      "holdings_amount_change_30d": 0,                  // 最近30天持仓数量变化（单位：币）
      "holdings_amount_change_7d": 0,                   // 最近7天持仓数量变化（单位：币）
      "holdings_amount_change1d": 0,                    // 最近1天持仓数量变化（单位：币）
      "close_time": 1721422800000,                      // 收盘时间（时间戳，单位：毫秒）
      "update_time": 1745203812007                      // 更新时间（时间戳，单位：毫秒）
    },
    {
      "symbol": "ETC",                                  // 币种代码，例如 ETC 代表以太经典
      "primary_market_price": 11.99,                    // 一级市场价格
      "secondary_market_price": 6.63,                   // 二级市场价格
      "premium_rate": -44.7,                            // 溢价率，ETC 当前处于较大折价状态
      "holdings_amount": 11181376.733556,               // 持仓数量（单位：币）
      "holdings_usd": 181440200.2554132,                // 持仓总市值（单位：USD）
      "holdings_amount_change_30d": -20697.669828,      // 最近30天持仓数量变化（减少）
      "holdings_amount_change_7d": -4596.123672,        // 最近7天持仓数量变化（减少）
      "holdings_amount_change1d": 0,                    // 最近1天持仓数量变化
      "close_time": 1744923600000,                      // 收盘时间
      "update_time": 1745203812168                      // 更新时间
    }
  ]
}

```

