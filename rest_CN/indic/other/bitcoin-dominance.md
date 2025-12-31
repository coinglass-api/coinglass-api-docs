# 指标 - 其他指标 - 比特币市值占比


```
GET /api/index/bitcoin-dominance
```


该接口提供比特币市值占比数据

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

