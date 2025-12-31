# ETF - 以太坊 ETF - 以太坊 ETF 列表


```
GET /api/etf/ethereum/list
```


該接口提供以太坊交易所交易基金（ETF）的關鍵狀態資訊列表。

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
      "ticker": "ETHA",                                  // ETF 代碼
      "name": "iShares Ethereum Trust ETF",              // ETF 名稱
      "region": "us",                                    // 地區
      "market_status": "closed",                         // 市場狀態
      "primary_exchange": "XNAS",                        // 主要交易所
      "cik_code": "0002000638",                          // CIK 代碼
      "type": "Spot",                                    // 類型
      "market_cap": "544896000.00",                      // 市值
      "list_date": 1721692800000,                        // 上市日期
      "shares_outstanding": "28800000",                  // 已發行份額
      "aum": "",                                         // 管理資產總值
      "management_fee_percent": "0.25",                  // 管理費
      "last_trade_time": 1722988779939,                  // 最新交易時間
      "last_quote_time": 1722988799379,                  // 最新計價時間
      "volume_quantity": 5592645,                        // 交易量
      "volume_usd": 106447049.343,                       // 美元交易量
      "price": 18.92,                                    // 市場價格
      "price_change": 0.67,                              // 價格變化
      "price_change_percent": 3.67,                      // 價格變化百分比
      "asset_info": {
        "nav": 18.11,                                  // 淨值
        "premium_discount": 0.77,                      // 溢價/折扣
        "holding_quantity": 237882.8821,                 // 持倉數量
        "change_percent_1d": 0,                        // 1天變化百分比
        "change_quantity_1d": 0,                         // 1天變化值
        "change_percent_7d": 56.69,                    // 7天變化百分比
        "change_quantity_7d": 86060.9115,                // 7天變化值
        "date": "2024-08-05"                           // 數據日期
      },
      "update_time": 1722995656637                       // 更新時間
    }
  ]
}

```

