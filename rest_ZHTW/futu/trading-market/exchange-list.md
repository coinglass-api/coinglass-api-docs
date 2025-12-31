# 合約數據 - 交易市場 - 交易所列表


```
GET /api/futures/exchange-rank
```


此端點提供 CoinGlass 上合約交易所的排名列表。

***快取 / 更新頻率:*** 實時更新

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    {
      "exchange": "Binance",
      "open_interest_usd": 27564494330,
      "volume_usd": 54150896832,
      "liquidation_usd_24h": 58774453.06516198
    },
    {
      "exchange": "OKX",
      "open_interest_usd": 8586569027,
      "volume_usd": 22670494849,
      "liquidation_usd_24h": 19276388.77685
    },
  ]
}
```

