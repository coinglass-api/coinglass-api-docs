# 指标 - 其他指标 - 比特币 vs 美国 M2 货币供应增长


```
GET /api/index/bitcoin-vs-us-m2-growth
```


该接口提供比特币 vs 美国 M2 货币供应增长数据

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
      "timestamp": 1278979200000,
      "price": 0.06183332,
      "us_m2_yoy_growth": 0.1321,
      "us_m2_supply": 8639800000000
    },
    {
      "timestamp": 1279065600000,
      "price": 0.05815725,
      "us_m2_yoy_growth": 0.1321,
      "us_m2_supply": 8639800000000
    },
    {
      "timestamp": 1279152000000,
      "price": 0.05640261,
      "us_m2_yoy_growth": 0.1321,
      "us_m2_supply": 8639800000000
    },
}

```

