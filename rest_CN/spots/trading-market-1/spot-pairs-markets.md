# 现货 - 交易市场 - 交易对市场列表


```
GET /api/spot/pairs-markets
```


该接口提供现货交易对的相关指标信息。

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
      "symbol": "BTC/USDT",                // 交易对
      "exchange_name": "Binance",          // 交易所名称
      "current_price": 87503.55,           // 当前价格

      "price_change_1h": 99.55,            // 1小时价格变动
      "price_change_percent_1h": 0.11,     // 1小时价格变动百分比
      "volume_usd_1h": 54425251.2426,      // 1小时交易量 (USD)
      "buy_volume_usd_1h": 29304086.0661,  // 1小时买入交易量 (USD)
      "sell_volume_usd_1h": 25121165.1759, // 1小时卖出交易量 (USD)
      "volume_change_usd_1h": -24851651.918,   // 1小时交易量变动 (USD)
      "volume_change_percent_1h": -31.35,  // 1小时交易量变动百分比
      "net_flows_usd_1h": 4182920.8902,    // 1小时净流入 (USD)

      "price_change_4h": 209.56,           // 4小时价格变动
      "price_change_percent_4h": 0.24,     // 4小时价格变动百分比
      "volume_usd_4h": 264625587.5144,     // 4小时交易量 (USD)
      "buy_volume_usd_4h": 137768056.2376, // 4小时买入交易量 (USD)
      "sell_volume_usd_4h": 126857531.2762, // 4小时卖出交易量 (USD)
      "volume_change_4h": -526166190.0218, // 4小时交易量变动 (USD)
      "volume_change_percent_4h": -66.54,  // 4小时交易量变动百分比
      "net_flows_usd_4h": 10910524.9614,   // 4小时净流入 (USD)

      "price_change_12h": 2925.55,         // 12小时价格变动
      "price_change_percent_12h": 3.46,    // 12小时价格变动百分比
      "volume_usd_12h": 1212930000.2011,   // 12小时交易量 (USD)
      "buy_volume_usd_12h": 662857153.6506, // 12小时买入交易量 (USD)
      "sell_volume_usd_12h": 550072846.5499, // 12小时卖出交易量 (USD)
      "volume_change_12h": 842092388.1946, // 12小时交易量变动 (USD)
      "volume_change_percent_12h": 227.08, // 12小时交易量变动百分比
      "net_flows_usd_12h": 112784307.1007, // 12小时净流入 (USD)

      "price_change_24h": 2735.79,         // 24小时价格变动
      "price_change_percent_24h": 3.23,    // 24小时价格变动百分比
      "volume_usd_24h": 1585522232.603,    // 24小时交易量 (USD)
      "buy_volume_usd_24h": 843617569.7248, // 24小时买入交易量 (USD)
      "sell_volume_usd_24h": 741904662.8776, // 24小时卖出交易量 (USD)
      "volume_change_24h": 873336140.8197, // 24小时交易量变动 (USD)
      "volume_change_percent_24h": 122.63, // 24小时交易量变动百分比
      "net_flows_usd_24h": 101712906.8472, // 24小时净流入 (USD)

      "price_change_1w": 3057.83,          // 1周价格变动
      "price_change_percent_1w": 3.62,     // 1周价格变动百分比
      "volume_usd_1w": 6808077059.7062,    // 1周交易量 (USD)
      "buy_volume_usd_1w": 3374037733.8429, // 1周买入交易量 (USD)
      "sell_volume_usd_1w": 3434039325.8627, // 1周卖出交易量 (USD)
      "volume_change_usd_1w": -11208235126.1193, // 1周交易量变动 (USD)
      "volume_change_percent_1w": -62.21,  // 1周交易量变动百分比
      "net_flows_usd_1w": -60001592.0198   // 1周净流入 (USD)
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                            |
| ------ | ------ | --- | --------------------------------------------- |
| symbol | string | YES | 交易币种（例如：BTC）。可通过 'support-coins' 接口获取支持的币种列表。 |

