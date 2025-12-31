# 指標 - 其他指標 - 比特幣 vs 全球 M2 貨幣供應增長


```
GET /api/index/bitcoin-vs-global-m2-growth
```


該接口提供比特幣 vs 全球 M2 貨幣供應增長數據

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

