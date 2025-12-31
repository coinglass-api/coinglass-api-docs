# 指标 - 合约指标 - 币种RSI列表


```
GET /api/futures/rsi/list
```


该接口提供多种加密货币在不同时间周期下的相对强弱指数（RSI）数值。

***缓存/ 更新频率***: 10秒一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "BTC",                                  // 币种符号，例如 BTC 表示比特币
      "rsi_15m": 54.71,                                 // 15分钟相对强弱指数（RSI）
      "price_change_percent_15m": 0.04,                 // 15分钟内价格涨跌幅（单位：%）
      "rsi_1h": 71.91,                                  // 1小时相对强弱指数（RSI）
      "price_change_percent_1h": -0.23,                 // 1小时内价格涨跌幅（单位：%）
      "rsi_4h": 72.12,                                  // 4小时相对强弱指数（RSI）
      "price_change_percent_4h": -0.09,                 // 4小时内价格涨跌幅（单位：%）
      "rsi_12h": 62.33,                                 // 12小时相对强弱指数（RSI）
      "price_change_percent_12h": 2.72,                 // 12小时内价格涨跌幅（单位：%）
      "rsi_24h": 57.88,                                 // 24小时相对强弱指数（RSI）
      "price_change_percent_24h": 3.4,                  // 24小时内价格涨跌幅（单位：%）
      "rsi_1w": 52.04,                                  // 1周相对强弱指数（RSI）
      "price_change_percent_1w": 2.6,                   // 1周内价格涨跌幅（单位：%）
      "current_price": 87348.6                          // 当前价格（单位：USD）
    },
    {
      "symbol": "ETH",                                  // 币种符号，例如 ETH 表示以太坊
      "rsi_15m": 54.35,                                 // 15分钟相对强弱指数（RSI）
      "price_change_percent_15m": -0.13,                // 15分钟内价格涨跌幅
      "rsi_1h": 67.93,                                  // 1小时相对强弱指数（RSI）
      "price_change_percent_1h": -0.26,                 // 1小时内价格涨跌幅
      "rsi_4h": 63.6,                                   // 4小时相对强弱指数（RSI）
      "price_change_percent_4h": 0.2,                   // 4小时内价格涨跌幅
      "rsi_12h": 52.09,                                 // 12小时相对强弱指数（RSI）
      "price_change_percent_12h": 3.41,                 // 12小时内价格涨跌幅
      "rsi_24h": 45.03,                                 // 24小时相对强弱指数（RSI）
      "price_change_percent_24h": 3.27,                 // 24小时内价格涨跌幅
      "rsi_1w": 33.31,                                  // 1周相对强弱指数（RSI）
      "price_change_percent_1w": 3.45,                  // 1周内价格涨跌幅
      "current_price": 1641.36                          // 当前价格（单位：USD）
    }
  ]
}

```

