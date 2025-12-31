# ETF - 比特币 ETF - 比特币ETF列表


```
GET /api/etf/bitcoin/list
```


该接口提供比特币交易型基金（ETF）的关键信息列表

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
  "data": [
    {
      "ticker": "GBTC",                                // ETF标识符
      "fund_name": "Grayscale Bitcoin Trust ETF",      // 基金名称
      "region": "us",                                  // 所属地区
      "market_status": "early_trading",                // 市场状态 (open/closed/early_trading等)
      "primary_exchange": "ARCX",                      // 主交易所
      "cik_code": "0001588489",                        // CIK代码 (唯一标识符)
      "fund_type": "Spot",                             // 基金类型 (Spot/ETF/Futures等)
      "list_date": 1424822400000,                      // 上市日期 (时间戳，单位毫秒)
      "shares_outstanding": "240750100",               // 流通股数
      "aum_usd": "16137543152.34",                     // 管理资产总值 (USD)
      "management_fee_percent": "1.5",                 // 管理费率 (%)
      "last_trade_time": 1745225312958,                // 最新成交时间 (时间戳，单位毫秒)
      "last_quote_time": 1745225389483,                // 最新计价时间 (时间戳，单位毫秒)
      "volume_quantity": 1068092,                      // 成交量
      "volume_usd": 71485902.2312,                     // 成交量 (USD)
      "price_change_usd": 0.47,                        // 价格变化 (USD)
      "price_change_percent": 0.71,                    // 价格变化 (%)
      "asset_details": {
        "net_asset_value_usd": 67.03,                  // 净值 (USD)
        "premium_discount_percent": 0.09,              // 溢价/折价率 (%)
        "btc_holding": 190124.5441,                    // BTC余额
        "btc_change_percent_24h": 0,                   // 24小时BTC变化 (%)
        "btc_change_24h": -7.8136,                     // 24小时BTC变化量
        "btc_change_percent_7d": -0.32,                // 7天BTC变化 (%)
        "btc_change_7d": -615.563,                     // 7天BTC变化量
        "update_date": "2025-04-17"                    // 更新时间
      },
      "update_timestamp": 1745224505000                // 数据更新时间 (时间戳，单位毫秒)
    }
  ]
}

```

