# 指標 - 其他指標 - 短期持有者持有比特幣數量


```
GET /api/index/bitcoin-short-term-holder-supply
```


該接口提供短期持有者持有比特幣數量數據

***快取 / 更新頻率:*** 1天更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

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

