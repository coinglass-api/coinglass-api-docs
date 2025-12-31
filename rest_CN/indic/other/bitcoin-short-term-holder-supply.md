# 指标 - 其他指标 - 短期持有者持有比特币数量


```
GET /api/index/bitcoin-short-term-holder-supply
```


该接口提供短期持有者持有比特币数量数据

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
      "price": 10.8584714558738,
      "short_term_holder_supply": 3682358,
      "timestamp": 1313625600000
    },
    {
      "price": 11.6704730432496,
      "short_term_holder_supply": 3682497,
      "timestamp": 1313712000000
    },
    {
      "price": 11.4597317393337,
      "short_term_holder_supply": 3680156,
      "timestamp": 1313798400000
    },
}

```

