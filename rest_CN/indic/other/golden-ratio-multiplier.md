# 指标 - 其他指标 - 比特币黄金比例乘数


```
GET /api/index/golden-ratio-multiplier
```


该接口提供比特币黄金比例乘数（Golden Ratio Multiplier）的相关数据

***缓存 / 更新频率:*** 每天一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "low_bull_high_2": 0.14,                       // 牛市低高位比例系数 / Bull market low-high ratio coefficient
      "timestamp": 1282003200000,                    // 时间戳（毫秒）/ Timestamp (milliseconds)
      "price": 0.07,                                 // 当前价格 / Current price
      "ma_350": 0.07,                                // 350日移动平均 / 350-day moving average
      "accumulation_high_1_6": 0.11200000000000002,  // 累积高位比例（1/6倍黄金比例）/ Accumulation high ratio (1/6 golden ratio)
      "x_3": 0.21000000000000002,                    // 黄金比例倍数 x3 / Golden ratio multiple x3
      "x_5": 0.35000000000000003,                    // 黄金比例倍数 x5 / Golden ratio multiple x5
      "x_8": 0.56,                                   // 黄金比例倍数 x8 / Golden ratio multiple x8
      "x_13": 0.9100000000000001,                    // 黄金比例倍数 x13 / Golden ratio multiple x13
      "x_21": 1.4700000000000002                     // 黄金比例倍数 x21 / Golden ratio multiple x21
    },

  ]
}

```

