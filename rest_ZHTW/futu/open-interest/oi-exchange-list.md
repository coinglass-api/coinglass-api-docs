# 合約數據 - 持倉 - 幣種交易所持倉


```
GET /api/futures/open-interest/exchange-list
```


該接口提供某個幣種在多個交易所的持倉量（Open Interest）數據。

***快取 / 更新頻率:***  每 10 秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版    | 創業版      | 標準版 | 專業版 | 企業版 |
| :----- | :----- | :------- | :-- | :-- | :-- |
| 可用性    | ✅      | ✅        | ✅   | ✅   | ✅   |
| 颗粒度    | `>=4h` | ​`>=30m` | 無限制 | 無限制 | 無限制 |

### 回應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "exchange": "All", // 交易所名稱，"All" 表示所有交易所匯總
      "symbol": "BTC", // 幣種符號

      "open_interest_usd": 57437891724.5572, // 未平倉合約價值 (USD)，表示所有未平倉合約的總價值
      "open_interest_quantity": 659557.3064, // 未平倉合約數量，表示所有未平倉合約的總數量

      "open_interest_by_stable_coin_margin": 48920274435.15, // 穩定幣本位未平倉合約價值 (USD)，合約採用穩定幣作為保證金
      "open_interest_quantity_by_coin_margin": 97551.2547, // 幣本位未平倉合約數量
      "open_interest_quantity_by_stable_coin_margin": 562006.0517, // 穩定幣本位未平倉合約數量

      "open_interest_change_percent_5m": 0.34, // 5 分鐘內未平倉合約變化百分比
      "open_interest_change_percent_15m": 0.59, // 15 分鐘內未平倉合約變化百分比
      "open_interest_change_percent_30m": 1.42, // 30 分鐘內未平倉合約變化百分比
      "open_interest_change_percent_1h": 2.27, // 1 小時內未平倉合約變化百分比
      "open_interest_change_percent_4h": 2.95, // 4 小時內未平倉合約變化百分比
      "open_interest_change_percent_24h": 0.9 // 24 小時內未平倉合約變化百分比
    },
    {
      "exchange": "CME", // 交易所名稱
      "symbol": "BTC", // 幣種符號

      "open_interest_usd": 12294999402.5, // 未平倉合約價值 (USD)，表示所有未平倉合約的總價值
      "open_interest_quantity": 141275.5, // 未平倉合約數量，表示所有未平倉合約的總數量

      "open_interest_by_stable_coin_margin": 12294999402.5, // 穩定幣本位未平倉合約價值 (USD)，合約採用穩定幣作為保證金
      "open_interest_quantity_by_coin_margin": 0, // 幣本位未平倉合約數量
      "open_interest_quantity_by_stable_coin_margin": 141275.5, // 穩定幣本位未平倉合約數量

      "open_interest_change_percent_5m": 0.08, // 5 分鐘內未平倉合約變化百分比
      "open_interest_change_percent_15m": 0.14, // 15 分鐘內未平倉合約變化百分比
      "open_interest_change_percent_30m": 0.49, // 30 分鐘內未平倉合約變化百分比
      "open_interest_change_percent_1h": 1.13, // 1 小時內未平倉合約變化百分比
      "open_interest_change_percent_4h": 2.4, // 4 小時內未平倉合約變化百分比
      "open_interest_change_percent_24h": 2.08 // 24 小時內未平倉合約變化百分比
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                         |
| ------ | ------ | --- | ------------------------------------------ |
| symbol | string | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。 |

