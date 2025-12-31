# 現貨 - 交易市場 - 交易對市場列表


```
GET /api/spot/pairs-markets
```


該接口提供現貨交易對的相關指標數據

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
      "symbol": "BTC/USDT",                // 交易對
      "exchange_name": "Binance",          // 交易所名稱
      "current_price": 87503.55,           // 當前價格

      "price_change_1h": 99.55,            // 1小時價格變動
      "price_change_percent_1h": 0.11,     // 1小時價格變動百分比
      "volume_usd_1h": 54425251.2426,      // 1小時交易量 (USD)
      "buy_volume_usd_1h": 29304086.0661,  // 1小時買入交易量 (USD)
      "sell_volume_usd_1h": 25121165.1759, // 1小時賣出交易量 (USD)
      "volume_change_usd_1h": -24851651.918,   // 1小時交易量變動 (USD)
      "volume_change_percent_1h": -31.35,  // 1小時交易量變動百分比
      "net_flows_usd_1h": 4182920.8902,    // 1小時淨流入 (USD)

      "price_change_4h": 209.56,           // 4小時價格變動
      "price_change_percent_4h": 0.24,     // 4小時價格變動百分比
      "volume_usd_4h": 264625587.5144,     // 4小時交易量 (USD)
      "buy_volume_usd_4h": 137768056.2376, // 4小時買入交易量 (USD)
      "sell_volume_usd_4h": 126857531.2762, // 4小時賣出交易量 (USD)
      "volume_change_4h": -526166190.0218, // 4小時交易量變動 (USD)
      "volume_change_percent_4h": -66.54,  // 4小時交易量變動百分比
      "net_flows_usd_4h": 10910524.9614,   // 4小時淨流入 (USD)

      "price_change_12h": 2925.55,         // 12小時價格變動
      "price_change_percent_12h": 3.46,    // 12小時價格變動百分比
      "volume_usd_12h": 1212930000.2011,   // 12小時交易量 (USD)
      "buy_volume_usd_12h": 662857153.6506, // 12小時買入交易量 (USD)
      "sell_volume_usd_12h": 550072846.5499, // 12小時賣出交易量 (USD)
      "volume_change_12h": 842092388.1946, // 12小時交易量變動 (USD)
      "volume_change_percent_12h": 227.08, // 12小時交易量變動百分比
      "net_flows_usd_12h": 112784307.1007, // 12小時淨流入 (USD)

      "price_change_24h": 2735.79,         // 24小時價格變動
      "price_change_percent_24h": 3.23,    // 24小時價格變動百分比
      "volume_usd_24h": 1585522232.603,    // 24小時交易量 (USD)
      "buy_volume_usd_24h": 843617569.7248, // 24小時買入交易量 (USD)
      "sell_volume_usd_24h": 741904662.8776, // 24小時賣出交易量 (USD)
      "volume_change_24h": 873336140.8197, // 24小時交易量變動 (USD)
      "volume_change_percent_24h": 122.63, // 24小時交易量變動百分比
      "net_flows_usd_24h": 101712906.8472, // 24小時淨流入 (USD)

      "price_change_1w": 3057.83,          // 1周價格變動
      "price_change_percent_1w": 3.62,     // 1周價格變動百分比
      "volume_usd_1w": 6808077059.7062,    // 1周交易量 (USD)
      "buy_volume_usd_1w": 3374037733.8429, // 1周買入交易量 (USD)
      "sell_volume_usd_1w": 3434039325.8627, // 1周賣出交易量 (USD)
      "volume_change_usd_1w": -11208235126.1193, // 1周交易量變動 (USD)
      "volume_change_percent_1w": -62.21,  // 1周交易量變動百分比
      "net_flows_usd_1w": -60001592.0198   // 1周淨流入 (USD)
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                         |
| ------ | ------ | --- | ------------------------------------------ |
| symbol | string | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。 |

