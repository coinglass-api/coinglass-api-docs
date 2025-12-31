# 指標 - 現貨 - Coinbase 溢價指數


```
GET /api/coinbase-premium-index
```


該接口提供 Coinbase 比特幣溢價指數，反映 Coinbase Pro 與 Binance 之間的比特幣價格差異。

***快取 / 更新頻率:*** 即時更新.

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
      "time": 1658880000,         // 時間戳（秒）
      "premium": 5.55,            // 溢價金額（USD）
      "premium_rate": 0.0261      // 溢價率（例如 0.0261 表示 2.61%）
    },
    {
      "time": 1658880000,         // 時間戳（秒）
      "premium": 5.55,            // 溢價金額（USD）
      "premium_rate": 0.0261      // 溢價率（例如 0.0261 表示 2.61%）
    }
  ]
}

```

 **Parameters:**
| 名称        | 类型      | 必填  | 描述                                                     |
| --------- | ------- | --- | ------------------------------------------------------ |
| interval  | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。 |
| limit     | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                         |
| startTime | integer | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                         |
| endTime   | integer | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                         |

