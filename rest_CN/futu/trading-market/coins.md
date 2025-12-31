# 合约 - 交易市场 - 支持的币种


```
GET /api/futures/supported-coins
```


该接口用于查询 CoinGlass 支持的所有合约币种。

***缓存 / 更新频率:*** 每 1 分钟更新一次

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
      "BTC",
      "ETH",
      "SOL",
      "XRP",
      ...
  ]
}
```

