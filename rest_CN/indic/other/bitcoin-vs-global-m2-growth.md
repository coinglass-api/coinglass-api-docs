# 指标 - 其他指标 - 比特币 vs 全球 M2 货币供应增长


```
GET /api/index/bitcoin-vs-global-m2-growth
```


该接口提供比特币 vs 全球 M2 货币供应增长数据

***缓存 / 更新频率:*** 1天更新一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "data": [
    {
      "timestamp": 1369008000000,
      "price": 117.8186364699,
      "global_m2_yoy_growth": 5.5654014717,
      "global_m2_supply": 59166686473105
    },
    {
      "timestamp": 1369612800000,
      "price": 126.392905903,
      "global_m2_yoy_growth": 5.8571414345,
      "global_m2_supply": 59490171457382
    },
    {
      "timestamp": 1370217600000,
      "price": 122.9491879018,
      "global_m2_yoy_growth": 6.7670545757,
      "global_m2_supply": 60072386054198
    },
}

```

