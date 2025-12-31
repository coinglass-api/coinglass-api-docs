# 指标 - 其他指标 - 牛市逃顶信号清单


```
GET /api/bull-market-peak-indicator
```


该接口提供牛市逃顶信号清单数据

***缓存 / 更新频率:*** 1天一次.

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
      "indicator_name": "Bitcoin Ahr999 Index",  // 指标名称
      "current_value": "0.78",                  // 当前值
      "target_value": "4",                      // 目标值
      "previous_value": "0.77",                 // 前一值
      "change_value": "0.0009811160359081",     // 变动值
      "comparison_type": ">=",                  // 比较类型
      "hit_status": false                       // 是否满足目标条件
    },
    {
      "indicator_name": "Pi Cycle Top Indicator",  // 指标名称
      "current_value": "85073.0",                  // 当前值
      "target_value": "154582",                    // 目标值
      "previous_value": "85127.0",                 // 前一值
      "change_value": "-54.0",                     // 变动值
      "comparison_type": ">=",                     // 比较类型
      "hit_status": false                          // 是否满足目标条件
    }
  ]
}

```

