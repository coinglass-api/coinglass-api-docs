# 合約數據 - 交易市場 - 幣種漲跌幅


```
GET /api/futures/coins-price-change
```


該接口提供幣種在多個時間週期內的漲跌幅和振幅數據

***快取 / 更新頻率:***  即時更新.

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
      "symbol": "BTC", // 幣種
      "current_price": 84518.4, // 當前價格

      "price_change_percent_5m": -0.04, // 5分鐘價格漲跌幅 (%)
      "price_change_percent_15m": -0.09, // 15分鐘價格漲跌幅 (%)
      "price_change_percent_30m": -0.11, // 30分鐘價格漲跌幅 (%)
      "price_change_percent_1h": -0.17, // 1小時價格漲跌幅 (%)
      "price_change_percent_4h": -0.54, // 4小時價格漲跌幅 (%)
      "price_change_percent_12h": -0.6, // 12小時價格漲跌幅 (%)
      "price_change_percent_24h": 0.24, // 24小時價格漲跌幅 (%)

      "price_amplitude_percent_5m": 0.07, // 5分鐘價格振幅 (%)
      "price_amplitude_percent_15m": 0.16, // 15分鐘價格振幅 (%)
      "price_amplitude_percent_30m": 0.18, // 30分鐘價格振幅 (%)
      "price_amplitude_percent_1h": 0.26, // 1小時價格振幅 (%)
      "price_amplitude_percent_4h": 0.63, // 4小時價格振幅 (%)
      "price_amplitude_percent_12h": 1.17, // 12小時價格振幅 (%)
      "price_amplitude_percent_24h": 2.06 // 24小時價格振幅 (%)
    },
    {
      "symbol": "ETH", // 幣種
      "current_price": 1573.45, // 當前價格

      "price_change_percent_5m": -0.04, // 5分鐘價格漲跌幅 (%)
      "price_change_percent_15m": -0.34, // 15分鐘價格漲跌幅 (%)
      "price_change_percent_30m": -0.38, // 30分鐘價格漲跌幅 (%)
      "price_change_percent_1h": -0.54, // 1小時價格漲跌幅 (%)
      "price_change_percent_4h": -0.77, // 4小時價格漲跌幅 (%)
      "price_change_percent_12h": -1.99, // 12小時價格漲跌幅 (%)
      "price_change_percent_24h": -1.41, // 24小時價格漲跌幅 (%)

      "price_amplitude_percent_5m": 0.13, // 5分鐘價格振幅 (%)
      "price_amplitude_percent_15m": 0.4, // 15分鐘價格振幅 (%)
      "price_amplitude_percent_30m": 0.47, // 30分鐘價格振幅 (%)
      "price_amplitude_percent_1h": 0.66, // 1小時價格振幅 (%)
      "price_amplitude_percent_4h": 0.9, // 4小時價格振幅 (%)
      "price_amplitude_percent_12h": 2.74, // 12小時價格振幅 (%)
      "price_amplitude_percent_24h": 3.47 // 24小時價格振幅 (%)
    }
  ]
}

```

