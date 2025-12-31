# ETF - 比特幣 ETF - 比特幣 ETF 歷史


```
GET /api/etf/bitcoin/history
```


該接口提供比特幣 ETF 的歷史數據，涵蓋每個 ETF 代碼的關鍵指標數據，包括市場價格、淨資產價值（NAV）、溢價／折扣百分比、流通股數以及總淨資產等。

***快取 / 更新頻率:*** 每 1天更新一次

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
      "assets_date": 1706486400000,           // 淨資產對應日期（時間戳，毫秒）
      "btc_holdings": 496573.8166,            // BTC 持倉數量
      "market_date": 1706486400000,           // 市場價格對應日期（時間戳，毫秒）
      "market_price": 38.51,                  // 市場價格（USD）
      "name": "Grayscale Bitcoin Trust",      // ETF 名稱
      "nav": 38.57,                           // 單位淨值（Net Asset Value，USD）
      "net_assets": 21431132778.35,           // 總淨資產（USD）
      "premium_discount": -0.16,              // 溢價/折扣百分比（負值為折扣）
      "shares_outstanding": 555700100,        // 已發行份額
      "ticker": "GBTC"                        // ETF 代碼
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                    |
| ------ | ------ | --- | --------------------- |
| ticker | string | YES | ETF 代碼（例如：GBTC、IBIT）。 |

