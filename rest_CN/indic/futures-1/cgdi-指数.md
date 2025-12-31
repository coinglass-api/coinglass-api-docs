# 指标 - 合约指标 - CGDI 指数


```
GET /api/futures/cgdi-index/history
```


此端点提供 CGDI（CoinGlass 衍生品指数）历史数据

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
      "time": 1704067200000,
      "cgdi_index_value": 1000
    },
    {
      "time": 1704153600000,
      "cgdi_index_value": 1053.2551
    },
  ]
}

```

