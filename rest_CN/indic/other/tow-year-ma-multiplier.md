# 指标 - 其他指标 - 两年MA乘数指标


```
GET /api/index/2-year-ma-multiplier
```


该接口提供两年MA乘数指标数据

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
      "timestamp": 1282003200000,               // 时间戳 (毫秒)
      "price": 0.07,                            // 当前价格
      "moving_average_730": 0.07,               // 2 年移动平均线 (730 表示周期)
      "moving_average_730_multiplier_5": 0.35000000000000003, // 2 年移动平均线的 5 倍 (Multiplier)
    }
  ]
}

```

