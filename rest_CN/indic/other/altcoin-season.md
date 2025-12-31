# 指标 - 其他指标 - 山寨币季节指数


```
GET /api/index/altcoin-season
```


该接口提供山寨币季节指数的数据

***缓存 / 更新频率:*** 5分钟更新一次.

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
      "timestamp": 1491177600000,
      "altcoin_index": 96,
      "altcoin_marketcap": 0
    },
    {
      "timestamp": 1491264000000,
      "altcoin_index": 100,
      "altcoin_marketcap": 0
    },
    {
      "timestamp": 1491350400000,
      "altcoin_index": 96,
      "altcoin_marketcap": 0
    },
}

```

