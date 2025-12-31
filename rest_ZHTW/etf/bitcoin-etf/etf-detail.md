# ETF - 比特幣 ETF - 比特幣 ETF 詳情


```
GET /api/etf/bitcoin/detail
```


該接口提供某只比特幣交易所交易基金（ETF）的詳細數據。

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
  "data": {
    "ticker_info": {
      "id": 1,                                         // ETF ID
      "ticker": "GBTC",                                // ETF 代碼
      "name": "Grayscale Bitcoin Trust ETF",           // ETF 名稱
      "market": "stocks",                              // 市場類型
      "region": "us",                                  // 地區
      "primary_exchange": "ARCX",                      // 主要交易所
      "fund_type": "ETV",                              // 產品類型
      "active": "true",                                // 是否活躍
      "currency_name": "usd",                          // 貨幣名稱
      "cik_code": "0001588489",                        // CIK 編號
      "composite_figi": "BBG008748J88",                // 綜合 FIGI
      "share_class_figi": "BBG008748J97",              // 股份類 FIGI
      "phone_number": "212-668-1427",                  // 聯繫電話
      "tag": "BTC",                                    // 資產標籤
      "type2": "Spot",                                 // 產品類型2
      "address": {
        "address_1": "{\"address2\":\"4TH FLOOR\",\"city\":\"STAMFORD\",\"address1\":\"290 HARBOR DRIVE\",\"state\":\"CT\",\"postal_code\":\"06902\"}"
      },                                               // 公司地址（JSON 字符串，需解析）
      "sic_code": "6221",                              // SIC 編碼
      "sic_description": "COMMODITY CONTRACTS BROKERS & DEALERS", // 行業描述
      "ticker_root": "GBTC",                           // Ticker Root
      "list_date": 1424822400000,                      // 上市日期（時間戳，毫秒）
      "share_class_shares_outstanding": "240750100",   // 流通份額
      "round_lot": "100",                              // 每手份額
      "status": 1,                                     // 狀態
      "update_time": 1745224505000                     // 更新時間（時間戳，毫秒）
    },
    "market_status": "early_trading",                  // 市場狀態
    "name": "Grayscale Bitcoin Trust ETF",             // ETF 名稱
    "ticker": "GBTC",                                  // ETF 代碼
    "type": "stocks",                                  // 市場類型
    "session": {
      "change": 2.22,                                  // 漲跌
      "change_percent": 3.309,                         // 漲跌幅（%）
      "early_trading_change": 2.22,                    // 盤前漲跌
      "early_trading_change_percent": 3.309,           // 盤前漲跌幅（%）
      "close": 67.09,                                  // 收盤價
      "high": 67.56,                                   // 最高價
      "low": 66.15,                                    // 最低價
      "open": 66.86,                                   // 開盤價
      "volume": 1068092,                               // 成交量
      "previous_close": 67.09,                         // 前收盤價
      "price": 69.31                                   // 最新價
    },
    "last_quote": {
      "last_updated": 1745226801708029700,             // 更新時間（納秒級時間戳）
      "timeframe": "REAL-TIME",                        // 時間類型（如實時）
      "ask": 69.29,                                    // 賣價
      "ask_size": 34,                                  // 賣量
      "ask_exchange": 8,                               // 賣方交易所代碼
      "bid": 69.18,                                    // 買價
      "bid_size": 3,                                   // 買量
      "bid_exchange": 11                               // 買方交易所代碼
    },
    "last_trade": {
      "last_updated": 1745226730467043600,             // 更新時間（納秒級時間戳）
      "timeframe": "REAL-TIME",                        // 時間類型（如實時）
      "id": "62879131651684",                          // 交易ID
      "price": 69.31,                                  // 成交價
      "size": 30,                                      // 成交量
      "exchange": 12,                                  // 交易所代碼
      "conditions": [12, 37]                           // 交易條件數組
    },
    "performance": {
      "low_price_52week": 39.56,                       // 52周最低價
      "high_price_52week": 86.11,                      // 52周最高價
      "high_price_52week_date": 1734238800000,         // 52周最高價日期（時間戳）
      "low_price_52week_date": 1722744000000,          // 52周最低價日期（時間戳）
      "ydt_change_percent": -12.23,                    // 年初至今漲跌幅（%）
      "year_change_percent": 13.98,                    // 年漲跌幅（%）
      "avg_vol_usd_10d": 518227                        // 過去10日平均交易金額（美元）
    }
  }
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                    |
| ------ | ------ | --- | --------------------- |
| ticker | string | YES | ETF 代碼（例如：GBTC、IBIT）。 |

