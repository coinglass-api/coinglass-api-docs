# 指標 - 其他指標 - 比特幣黃金比例乘數


```
GET /api/index/golden-ratio-multiplier
```


該接口提供比特幣黃金比例乘數（Golden Ratio Multiplier）的相關數據。

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
      "low_bull_high_2": 0.14,                       // 牛市低高位比例係數 / Bull market low-high ratio coefficient
      "timestamp": 1282003200000,                    // 時間戳（毫秒）/ Timestamp (milliseconds)
      "price": 0.07,                                 // 當前價格 / Current price
      "ma_350": 0.07,                                // 350日移動平均 / 350-day moving average
      "accumulation_high_1_6": 0.11200000000000002,  // 累積高位比例（1/6倍黃金比例）/ Accumulation high ratio (1/6 golden ratio)
      "x_3": 0.21000000000000002,                    // 黃金比例倍數 x3 / Golden ratio multiple x3
      "x_5": 0.35000000000000003,                    // 黃金比例倍數 x5 / Golden ratio multiple x5
      "x_8": 0.56,                                   // 黃金比例倍數 x8 / Golden ratio multiple x8
      "x_13": 0.9100000000000001,                    // 黃金比例倍數 x13 / Golden ratio multiple x13
      "x_21": 1.4700000000000002                     // 黃金比例倍數 x21 / Golden ratio multiple x21
    }
  ]
}

```

