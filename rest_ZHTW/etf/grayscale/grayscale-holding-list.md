# ETF - 灰度基金 - 灰度持倉列表


```
GET /api/grayscale/holdings-list
```


該接口提供由 Grayscale Investments（灰度投資）管理的資產持倉列表。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "ETH",                                  // 幣種代碼，例如 ETH 代表以太坊
      "primary_market_price": 29.89,                    // 一級市場價格
      "secondary_market_price": 29.71,                  // 二級市場價格
      "premium_rate": -0.6,                             // 溢價率（單位：%）
      "holdings_amount": 2630007.61026,                 // 當前持倉數量（單位：幣）
      "holdings_usd": 4290752215.8347797,               // 當前持倉總市值（單位：USD）
      "holdings_amount_change_30d": 0,                  // 最近30天持倉數量變化（單位：幣）
      "holdings_amount_change_7d": 0,                   // 最近7天持倉數量變化（單位：幣）
      "holdings_amount_change1d": 0,                    // 最近1天持倉數量變化（單位：幣）
      "close_time": 1721422800000,                      // 收盤時間（時間戳，單位：毫秒）
      "update_time": 1745203812007                      // 更新時間（時間戳，單位：毫秒）
    },
    {
      "symbol": "ETC",                                  // 幣種代碼，例如 ETC 代表以太經典
      "primary_market_price": 11.99,                    // 一級市場價格
      "secondary_market_price": 6.63,                   // 二級市場價格
      "premium_rate": -44.7,                            // 溢價率，ETC 當前處於較大折價狀態
      "holdings_amount": 11181376.733556,               // 持倉數量（單位：幣）
      "holdings_usd": 181440200.2554132,                // 持倉總市值（單位：USD）
      "holdings_amount_change_30d": -20697.669828,      // 最近30天持倉數量變化（減少）
      "holdings_amount_change_7d": -4596.123672,        // 最近7天持倉數量變化（減少）
      "holdings_amount_change1d": 0,                    // 最近1天持倉數量變化
      "close_time": 1744923600000,                      // 收盤時間
      "update_time": 1745203812168                      // 更新時間
    }
  ]
}

```

