# 指標 - 其他指標 - 比特幣市值佔比


```
GET /api/index/bitcoin-dominance
```


該接口提供比特幣市值佔比數據

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
      "timestamp": 1367366400000,
      "price": 139,
      "bitcoin_dominance": 94.3595,
      "market_cap": 1545031856
    },
    {
      "timestamp": 1367625600000,
      "price": 98.0999984741,
      "bitcoin_dominance": 93.8787,
      "market_cap": 1097883152
    },
    {
      "timestamp": 1367884800000,
      "price": 112.25,
      "bitcoin_dominance": 94.3851,
      "market_cap": 1240126128
    },
}

```

