# 合约 - 交易市场 - 币种涨跌幅


```
GET /api/futures/coins-price-change
```


该接口提供币种在多个时间周期内的涨跌幅和振幅数据。

***缓存/ 更新频率 :*** 实时更新.

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
      "symbol": "BTC", // 币种
      "current_price": 84518.4, // 当前价格

      "price_change_percent_5m": -0.04, // 5分钟价格涨跌幅 (%)
      "price_change_percent_15m": -0.09, // 15分钟价格涨跌幅 (%)
      "price_change_percent_30m": -0.11, // 30分钟价格涨跌幅 (%)
      "price_change_percent_1h": -0.17, // 1小时价格涨跌幅 (%)
      "price_change_percent_4h": -0.54, // 4小时价格涨跌幅 (%)
      "price_change_percent_12h": -0.6, // 12小时价格涨跌幅 (%)
      "price_change_percent_24h": 0.24, // 24小时价格涨跌幅 (%)

      "price_amplitude_percent_5m": 0.07, // 5分钟价格振幅 (%)
      "price_amplitude_percent_15m": 0.16, // 15分钟价格振幅 (%)
      "price_amplitude_percent_30m": 0.18, // 30分钟价格振幅 (%)
      "price_amplitude_percent_1h": 0.26, // 1小时价格振幅 (%)
      "price_amplitude_percent_4h": 0.63, // 4小时价格振幅 (%)
      "price_amplitude_percent_12h": 1.17, // 12小时价格振幅 (%)
      "price_amplitude_percent_24h": 2.06 // 24小时价格振幅 (%)
    },
    {
      "symbol": "ETH", // 币种
      "current_price": 1573.45, // 当前价格

      "price_change_percent_5m": -0.04, // 5分钟价格涨跌幅 (%)
      "price_change_percent_15m": -0.34, // 15分钟价格涨跌幅 (%)
      "price_change_percent_30m": -0.38, // 30分钟价格涨跌幅 (%)
      "price_change_percent_1h": -0.54, // 1小时价格涨跌幅 (%)
      "price_change_percent_4h": -0.77, // 4小时价格涨跌幅 (%)
      "price_change_percent_12h": -1.99, // 12小时价格涨跌幅 (%)
      "price_change_percent_24h": -1.41, // 24小时价格涨跌幅 (%)

      "price_amplitude_percent_5m": 0.13, // 5分钟价格振幅 (%)
      "price_amplitude_percent_15m": 0.4, // 15分钟价格振幅 (%)
      "price_amplitude_percent_30m": 0.47, // 30分钟价格振幅 (%)
      "price_amplitude_percent_1h": 0.66, // 1小时价格振幅 (%)
      "price_amplitude_percent_4h": 0.9, // 4小时价格振幅 (%)
      "price_amplitude_percent_12h": 2.74, // 12小时价格振幅 (%)
      "price_amplitude_percent_24h": 3.47 // 24小时价格振幅 (%)
    }
  ]
}

```

