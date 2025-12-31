# 指標 - 合約指標 - 幣種RSI 列表


```
GET /api/futures/rsi/list
```


該接口提供多種加密貨幣在不同時間週期下的相對強弱指數（RSI）數值。

***快取 / 更新頻率:*** 每 10 秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "BTC",                                  // 幣種符號，例如 BTC 表示比特幣
      "rsi_15m": 54.71,                                 // 15分鐘相對強弱指數（RSI）
      "price_change_percent_15m": 0.04,                 // 15分鐘內價格漲跌幅（單位：%）
      "rsi_1h": 71.91,                                  // 1小時相對強弱指數（RSI）
      "price_change_percent_1h": -0.23,                 // 1小時內價格漲跌幅（單位：%）
      "rsi_4h": 72.12,                                  // 4小時相對強弱指數（RSI）
      "price_change_percent_4h": -0.09,                 // 4小時內價格漲跌幅（單位：%）
      "rsi_12h": 62.33,                                 // 12小時相對強弱指數（RSI）
      "price_change_percent_12h": 2.72,                 // 12小時內價格漲跌幅（單位：%）
      "rsi_24h": 57.88,                                 // 24小時相對強弱指數（RSI）
      "price_change_percent_24h": 3.4,                  // 24小時內價格漲跌幅（單位：%）
      "rsi_1w": 52.04,                                  // 1週相對強弱指數（RSI）
      "price_change_percent_1w": 2.6,                   // 1週內價格漲跌幅（單位：%）
      "current_price": 87348.6                          // 當前價格（單位：USD）
    },
    {
      "symbol": "ETH",                                  // 幣種符號，例如 ETH 表示以太坊
      "rsi_15m": 54.35,                                 // 15分鐘相對強弱指數（RSI）
      "price_change_percent_15m": -0.13,                // 15分鐘內價格漲跌幅
      "rsi_1h": 67.93,                                  // 1小時相對強弱指數（RSI）
      "price_change_percent_1h": -0.26,                 // 1小時內價格漲跌幅
      "rsi_4h": 63.6,                                   // 4小時相對強弱指數（RSI）
      "price_change_percent_4h": 0.2,                   // 4小時內價格漲跌幅
      "rsi_12h": 52.09,                                 // 12小時相對強弱指數（RSI）
      "price_change_percent_12h": 3.41,                 // 12小時內價格漲跌幅
      "rsi_24h": 45.03,                                 // 24小時相對強弱指數（RSI）
      "price_change_percent_24h": 3.27,                 // 24小時內價格漲跌幅
      "rsi_1w": 33.31,                                  // 1週相對強弱指數（RSI）
      "price_change_percent_1w": 3.45,                  // 1週內價格漲跌幅
      "current_price": 1641.36                          // 當前價格（單位：USD）
    }
  ]
}

```

