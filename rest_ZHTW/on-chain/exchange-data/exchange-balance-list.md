# 鏈上 - 交易所數據 - 交易所餘額列表


```
GET /api/exchange/balance/list
```


該接口提供各交易所的資產餘額數據，包括 1 天、7 天和 30 天內的餘額變化百分比數據

***快取 / 更新頻率:*** 每 1小時更新一次

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
      "exchange_name": "Coinbase",               // 交易所名稱
      "total_balance": 716590.351233,            // 總餘額
      "balance_change_1d": 638.797302,           // 24小時餘額變動
      "balance_change_percent_1d": 0.09,         // 24小時餘額變動百分比 (%)
      "balance_change_7d": 799.967408,           // 7天餘額變動
      "balance_change_percent_7d": 0.11,         // 7天餘額變動百分比 (%)
      "balance_change_30d": -29121.977486,       // 30天餘額變動
      "balance_change_percent_30d": -3.91        // 30天餘額變動百分比 (%)
    },
    {
      "exchange_name": "Binance",                // 交易所名稱
      "total_balance": 582344.497738,            // 總餘額
      "balance_change_1d": 505.682778,           // 24小時餘額變動
      "balance_change_percent_1d": 0.09,         // 24小時餘額變動百分比 (%)
      "balance_change_7d": -3784.88544,          // 7天餘額變動
      "balance_change_percent_7d": -0.65,        // 7天餘額變動百分比 (%)
      "balance_change_30d": 3753.870055,         // 30天餘額變動
      "balance_change_percent_30d": 0.65         // 30天餘額變動百分比 (%)
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                |
| ------ | ------ | --- | ----------------- |
| symbol | string | YES | 交易幣種（例如：BTC、ETH）。 |

