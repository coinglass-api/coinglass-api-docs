# 其他 - 新聞、快訊 - 新聞


```
GET /api/article/list
```


這個接口提供即時新聞清單（最多回傳近1000條新聞）

***快取 / 更新頻率:*** 實時更新

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

 **Parameters:**
| 名称         | 类型      | 必填 | 描述                              |
| ---------- | ------- | -- | ------------------------------- |
| start_time | integer | NO | 起始時間戳（單位：毫秒，例如：1641522717000）。  |
| end_time   | integer | NO | 結束時間戳記（單位：毫秒，例如：1641522717000）。 |
| language   | string  | NO | 支援的語言：'en' 、 'zh' 、'zh-tw'      |
| page       | integer | NO | 目前頁碼                            |
| per_page   | integer | NO | 每頁回傳條數                          |

