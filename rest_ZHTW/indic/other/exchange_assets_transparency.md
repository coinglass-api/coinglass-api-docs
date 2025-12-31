# 指標 - 其他指標 - 交易所資產透明度證明


```
GET /api/exchange_assets_transparency/list
```


此接口提供各大交易所資產的即時透明度資料，包括總資產餘額、資金流入、資產變動、未平倉量、槓桿率及交易量等。

***快取 / 更新頻率:*** 1小时更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",                         // 狀態碼
  "data": [
    {
      "exchange_name": "Binance",       // 交易所名稱
      "exchange_logo_url": "https://cdn.coinglasscdn.com/static/exchanges/270.png",  // 交易所logo
      "balance_usd": 178382444198.04,   // 總資產
      "balance_change_usd_24h": -4244709940.9,  // 24小時價值變化
      "balance_change_usd_7d": 183489103818.63, // 7天價值變化
      "inflow_usd_24h": 1104357008.908988,      // 24小時流入
      "inflow_usd_7d": 870098130.1614555,       // 7天流入
      "open_interest": 28940016260,             // 合約持倉
      "average_leverage": 0.1622,               // 平均槓桿
      "volume_usd": 114901619432                // 交易量
    },
    {
      "exchange_name": "Bitfinex",              // 交易所名稱
      "exchange_logo_url": "https://cdn.coinglasscdn.com/static/exchanges/bitfinex.jpg", // 交易所logo
      "balance_usd": 25836820506.17,            // 總資產
      "balance_change_usd_24h": -164420313.45,  // 24小時價值變化
      "balance_change_usd_7d": 26135897993.59,  // 7天價值變化
      "inflow_usd_24h": 225181636.35856062,     // 24小時流入
      "inflow_usd_7d": 706172180.891416,        // 7天流入
      "open_interest": 732439767,               // 合約持倉
      "average_leverage": 0.0283,               // 平均槓桿
      "volume_usd": 68891576                    // 交易量
    }
  ]
}

```

