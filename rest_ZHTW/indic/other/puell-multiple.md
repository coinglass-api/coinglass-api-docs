# 指標 - 其他指標 - 普爾倍數


```
GET /api/index/puell-multiple
```


該接口提供 Puell Multiple 指標相關數據，包括在特定時間點的比特幣價格、買入／賣出數量，以及對應的普爾倍數數值。

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
      "timestamp": 1282003200000,           // 時間戳（毫秒）
      "price": 0.07,                         // 當日價格
      "puell_multiple": 1                   // Puell Multiple 指標數值
    },
    {
      "timestamp": 1282089600000,           // 時間戳（毫秒）
      "price": 0.068,                        // 當日價格
      "puell_multiple": 1.0007745933384973  // Puell Multiple 指標數值
    }
  ]
}

```

