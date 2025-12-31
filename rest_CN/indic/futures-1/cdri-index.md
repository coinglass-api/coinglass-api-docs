# 指标 - 合约指标 - CDRI 指数


```
GET /api/futures/cdri-index/history 
```


此端点提供 CDRI（CoinGlass 衍生品风险指数）历史数据。

***缓存 / 更新频率:*** 实时更新

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

**响应数据**

```json
{
  "code": "0",
  "data": [
    {
      "time": 1646438400000,
      "cdri_index_value": 50
    },
    {
      "time": 1646524800000,
      "cdri_index_value": 47
    },
  ]
}

```

