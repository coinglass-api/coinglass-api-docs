# 指標 - 其他指標 - 牛市逃頂指數


```
GET /api/bull-market-peak-indicator
```


該接口提供牛市逃頂指數數據。

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
      "indicator_name": "Bitcoin Ahr999 Index",  // 指標名稱
      "current_value": "0.78",                  // 當前值
      "target_value": "4",                      // 目標值
      "previous_value": "0.77",                 // 前一值
      "change_value": "0.0009811160359081",     // 變動值
      "comparison_type": ">=",                  // 比較類型
      "hit_status": false                       // 是否滿足目標條件
    },
    {
      "indicator_name": "Pi Cycle Top Indicator",  // 指標名稱
      "current_value": "85073.0",                  // 當前值
      "target_value": "154582",                    // 目標值
      "previous_value": "85127.0",                 // 前一值
      "change_value": "-54.0",                     // 變動值
      "comparison_type": ">=",                     // 比較類型
      "hit_status": false                          // 是否滿足目標條件
    }
  ]
}

```

