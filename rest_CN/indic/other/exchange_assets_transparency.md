# 指标 - 其他指标 - 交易所资产透明度证明


```
GET /api/exchange_assets_transparency/list
```


这个接口提供各大交易所资产的实时透明度数据，包括总资产余额、资金流入、资产变动、未平仓量、杠杆率及交易量等信息。

***缓存 / 更新频率:*** 1小时更新一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",                         // 状态码
  "data": [
    {
      "exchange_name": "Binance",       // 交易所名称
      "exchange_logo_url": "https://cdn.coinglasscdn.com/static/exchanges/270.png",  // 交易所logo
      "balance_usd": 178382444198.04,   // 总资产
      "balance_change_usd_24h": -4244709940.9,  // 24小时价值变化
      "balance_change_usd_7d": 183489103818.63, // 7天价值变化
      "inflow_usd_24h": 1104357008.908988,      // 24小时流入
      "inflow_usd_7d": 870098130.1614555,       // 7天流入
      "open_interest": 28940016260,             // 合约持仓
      "average_leverage": 0.1622,               // 平均杠杆
      "volume_usd": 114901619432                // 交易量
    },
    {
      "exchange_name": "Bitfinex",              // 交易所名称
      "exchange_logo_url": "https://cdn.coinglasscdn.com/static/exchanges/bitfinex.jpg", // 交易所logo
      "balance_usd": 25836820506.17,            // 总资产
      "balance_change_usd_24h": -164420313.45,  // 24小时价值变化
      "balance_change_usd_7d": 26135897993.59,  // 7天价值变化
      "inflow_usd_24h": 225181636.35856062,     // 24小时流入
      "inflow_usd_7d": 706172180.891416,        // 7天流入
      "open_interest": 732439767,               // 合约持仓
      "average_leverage": 0.0283,               // 平均杠杆
      "volume_usd": 68891576                    // 交易量
    }
  ]
}

```

