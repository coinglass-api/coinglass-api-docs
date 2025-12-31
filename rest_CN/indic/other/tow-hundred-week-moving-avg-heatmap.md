# 指标 - 其他指标 - 200周移动平均热力图


```
GET /api/index/200-week-moving-average-heatmap
```


该接口提供200周移动平均热力图数据

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
      "timestamp": 1325203200000,          // 时间戳 (毫秒)
      "price": 4.31063509000584,           // 当前价格
      "moving_average_1440": 4.143619070636635, // 200 周移动平均线 (1440 表示周期)
      "moving_average_1440_ip": 0,         // 移动平均线位置 (IP 指标)
      "buy_quantity": 0,                   // 买单数量
      "sell_quantity": 0                   // 卖单数量
    }
  ]
}

```

