# 指標 - 其他指標 - 兩年 MA 乘數指標


```
GET /api/index/2-year-ma-multiplier
```


該接口提供兩年 MA 乘數指標數據。

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
      "timestamp": 1282003200000,               // 時間戳 (毫秒)
      "price": 0.07,                            // 當前價格
      "moving_average_730": 0.07,               // 2 年移動平均線 (730 表示周期)
      "moving_average_730_multiplier_5": 0.35000000000000003, // 2 年移動平均線的 5 倍 (Multiplier)
    }
  ]
}

```

