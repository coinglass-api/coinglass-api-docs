# ETF - 比特幣 ETF - ETF 溢價／折價歷史


```
GET /api/etf/bitcoin/premium-discount/history
```


該接口提供比特幣 ETF 的溢價或折扣率的歷史數據，包括各 ETF 代碼的淨資產價值（NAV）、市場價格，以及對應的溢價／折扣百分比。

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
      "timestamp": 1706227200000,                 // 日期（時間戳，單位為毫秒）
      "list": [
        {
          "ticker": "GBTC",                       // ETF代碼
          "nav_usd": 37.51,                        // 淨資產價值（USD）
          "market_price_usd": 37.51,               // 市場價格（USD）
          "premium_discount_details": 0            // 溢價/折扣百分比
        },
        {
          "ticker": "IBIT",                       // ETF代碼
          "nav_usd": 23.94,                        // 淨資產價值（USD）
          "market_price_usd": 23.99,               // 市場價格（USD）
          "premium_discount_details": 0.22         // 溢價/折扣百分比
        },
        {
          "ticker": "FBTC",                       // ETF代碼
          "nav_usd": 36.720807,                    // 淨資產價值（USD）
          "market_price_usd": 36.75,               // 市場價格（USD）
          "premium_discount_details": 0.0795       // 溢價/折扣百分比
        }
      ]
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填 | 描述                    |
| ------ | ------ | -- | --------------------- |
| ticker | string | NO | ETF 代碼（例如：GBTC、IBIT）。 |

