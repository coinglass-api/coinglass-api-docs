# 指标 - 其他指标 - 普尔倍数


```
GET /api/index/puell-multiple
```


该接口提供 Puell Multiple 指标相关数据，包括在特定时间点的比特币价格、买入/卖出数量，以及对应的普尔倍数数值。

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
      "timestamp": 1282003200000,           // 时间戳（毫秒）
      "price": 0.07,                         // 当日价格
      "puell_multiple": 1                   // Puell Multiple 指标数值
    },
    {
      "timestamp": 1282089600000,           // 时间戳（毫秒）
      "price": 0.068,                        // 当日价格
      "puell_multiple": 1.0007745933384973  // Puell Multiple 指标数值
    }
  ]
}

```

