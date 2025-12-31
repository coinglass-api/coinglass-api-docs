# ETF - 比特幣 ETF - 比特幣 ETF 列表


```
GET /api/etf/bitcoin/list
```


該接口提供比特幣交易型基金（ETF）的關鍵數據列表。

***快取 / 更新頻率:*** 每 1天更新一次

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
      "ticker": "GBTC",                                // ETF標識符
      "fund_name": "Grayscale Bitcoin Trust ETF",      // 基金名稱
      "region": "us",                                  // 所属地區
      "market_status": "early_trading",                // 市場狀態 (open/closed/early_trading等)
      "primary_exchange": "ARCX",                      // 主交易所
      "cik_code": "0001588489",                        // CIK代碼 (唯一標識符)
      "fund_type": "Spot",                             // 基金類型 (Spot/ETF/Futures等)
      "list_date": 1424822400000,                      // 上市日期 (時間戳，單位毫秒)
      "shares_outstanding": "240750100",               // 流通股數
      "aum_usd": "16137543152.34",                     // 管理資產總值 (USD)
      "management_fee_percent": "1.5",                 // 管理費率 (%)
      "last_trade_time": 1745225312958,                // 最新成交時間 (時間戳，單位毫秒)
      "last_quote_time": 1745225389483,                // 最新計價時間 (時間戳，單位毫秒)
      "volume_quantity": 1068092,                      // 成交量
      "volume_usd": 71485902.2312,                     // 成交量 (USD)
      "price_change_usd": 0.47,                        // 價格變化 (USD)
      "price_change_percent": 0.71,                    // 價格變化 (%)
      "asset_details": {
        "net_asset_value_usd": 67.03,                  // 淨值 (USD)
        "premium_discount_percent": 0.09,              // 溢價/折價率 (%)
        "btc_holding": 190124.5441,                    // BTC餘額
        "btc_change_percent_24h": 0,                   // 24小時BTC變化 (%)
        "btc_change_24h": -7.8136,                     // 24小時BTC變化量
        "btc_change_percent_7d": -0.32,                // 7天BTC變化 (%)
        "btc_change_7d": -615.563,                     // 7天BTC變化量
        "update_date": "2025-04-17"                    // 更新時間
      },
      "update_timestamp": 1745224505000                // 資料更新時間 (時間戳，單位毫秒)
    }
  ]
}

```

