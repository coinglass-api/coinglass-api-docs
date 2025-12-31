# 期權 - 期權相關


```
GET /api/option/info
```


該接口提供不同交易所期權的持倉量與成交量等詳細數據。

***快取 / 更新頻率:*** 每 30 秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "exchange_name": "All",                           // 交易所名稱
      "open_interest": 361038.78,                       // 未平倉合約數量（張）
      "oi_market_share": 100,                           // 持倉占有率（%）
      "open_interest_change_24h": 2.72,                 // 24 小時未平倉合約變化（%）
      "open_interest_usd": 31623069708.138245,          // 未平倉合約價值（美元）
      "volume_usd_24h": 2764676957.0569425,             // 24 小時交易量（美元）
      "volume_change_percent_24h": 303.1                // 24 小時交易量變化（%）
    },
    {
      "exchange_name": "Deribit",                       // 交易所名稱
      "open_interest": 262641.9,                        // 未平倉合約數量（張）
      "oi_market_share": 72.74,                         // 持倉占有率（%）
      "open_interest_change_24h": 2.57,                 // 24 小時未平倉合約變化（%）
      "open_interest_usd": 23005403973.349,             // 未平倉合約價值（美元）
      "volume_usd_24h": 2080336672.709                  // 24 小時交易量（美元）
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                |
| ------ | ------ | --- | ----------------- |
| symbol | string | YES | 交易幣種（例如：BTC、ETH）。 |

