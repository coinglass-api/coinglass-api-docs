# ETF - 比特币 ETF - 比特币ETF详情


```
GET /api/etf/bitcoin/detail
```


该接口提供某只比特币交易所交易基金（ETF）的详细信息

***缓存/ 更新频率 :*** 1天一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "ticker_info": {
      "id": 1,                                         // ETF ID
      "ticker": "GBTC",                                // ETF 代码
      "name": "Grayscale Bitcoin Trust ETF",           // ETF 名称
      "market": "stocks",                              // 市场类型
      "region": "us",                                  // 地区
      "primary_exchange": "ARCX",                      // 主要交易所
      "fund_type": "ETV",                              // 产品类型
      "active": "true",                                // 是否活跃
      "currency_name": "usd",                          // 货币名称
      "cik_code": "0001588489",                        // CIK 编号
      "composite_figi": "BBG008748J88",                // 综合 FIGI
      "share_class_figi": "BBG008748J97",              // 股份类 FIGI
      "phone_number": "212-668-1427",                  // 联系电话
      "tag": "BTC",                                    // 资产标签
      "type2": "Spot",                                 // 产品类型2
      "address": {
        "address_1": "{\"address2\":\"4TH FLOOR\",\"city\":\"STAMFORD\",\"address1\":\"290 HARBOR DRIVE\",\"state\":\"CT\",\"postal_code\":\"06902\"}"
      },                                               // 公司地址（JSON 字符串，需解析）
      "sic_code": "6221",                              // SIC 编码
      "sic_description": "COMMODITY CONTRACTS BROKERS & DEALERS", // 行业描述
      "ticker_root": "GBTC",                           // Ticker Root
      "list_date": 1424822400000,                      // 上市日期（时间戳，毫秒）
      "share_class_shares_outstanding": "240750100",   // 流通份额
      "round_lot": "100",                              // 每手份额
      "status": 1,                                     // 状态
      "update_time": 1745224505000                     // 更新时间（时间戳，毫秒）
    },
    "market_status": "early_trading",                  // 市场状态
    "name": "Grayscale Bitcoin Trust ETF",             // ETF 名称
    "ticker": "GBTC",                                  // ETF 代码
    "type": "stocks",                                  // 市场类型
    "session": {
      "change": 2.22,                                  // 涨跌
      "change_percent": 3.309,                         // 涨跌幅（%）
      "early_trading_change": 2.22,                    // 盘前涨跌
      "early_trading_change_percent": 3.309,           // 盘前涨跌幅（%）
      "close": 67.09,                                  // 收盘价
      "high": 67.56,                                   // 最高价
      "low": 66.15,                                    // 最低价
      "open": 66.86,                                   // 开盘价
      "volume": 1068092,                               // 成交量
      "previous_close": 67.09,                         // 前收盘价
      "price": 69.31                                   // 最新价
    },
    "last_quote": {
      "last_updated": 1745226801708029700,             // 更新时间（纳秒级时间戳）
      "timeframe": "REAL-TIME",                        // 时间类型（如实时）
      "ask": 69.29,                                    // 卖价
      "ask_size": 34,                                  // 卖量
      "ask_exchange": 8,                               // 卖方交易所代码
      "bid": 69.18,                                    // 买价
      "bid_size": 3,                                   // 买量
      "bid_exchange": 11                               // 买方交易所代码
    },
    "last_trade": {
      "last_updated": 1745226730467043600,             // 更新时间（纳秒级时间戳）
      "timeframe": "REAL-TIME",                        // 时间类型（如实时）
      "id": "62879131651684",                          // 交易ID
      "price": 69.31,                                  // 成交价
      "size": 30,                                      // 成交量
      "exchange": 12,                                  // 交易所代码
      "conditions": [12, 37]                           // 交易条件数组
    },
    "performance": {
      "low_price_52week": 39.56,                       // 52周最低价
      "high_price_52week": 86.11,                      // 52周最高价
      "high_price_52week_date": 1734238800000,         // 52周最高价日期（时间戳）
      "low_price_52week_date": 1722744000000,          // 52周最低价日期（时间戳）
      "ydt_change_percent": -12.23,                    // 年初至今涨跌幅（%）
      "year_change_percent": 13.98,                    // 年涨跌幅（%）
      "avg_vol_usd_10d": 518227                        // 过去10日平均交易金额（美元）
    }
  }
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                   |
| ------ | ------ | --- | -------------------- |
| ticker | string | YES | 股票代码，例如：GBTC,IBIT... |

