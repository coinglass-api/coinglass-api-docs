# 指標 - 其他指標 - 200 週移動平均熱力圖


```
GET /api/index/200-week-moving-average-heatmap
```


該接口提供 200 週移動平均熱力圖數據。

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
      "timestamp": 1325203200000,          // 時間戳 (毫秒)
      "price": 4.31063509000584,           // 當前價格
      "moving_average_1440": 4.143619070636635, // 200 周移動平均線 (1440 表示周期)
      "moving_average_1440_ip": 0,         // 移動平均線位置 (IP 指標)
      "buy_quantity": 0,                   // 買單數量
      "sell_quantity": 0                   // 賣單數量
    }
  ]
}

```

