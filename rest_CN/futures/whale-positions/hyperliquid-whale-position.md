# 合约 - Hyperliquid 仓位 - Hyperliquid 鲸鱼持仓


```
GET /api/hyperliquid/whale-position
```


该接口提供 Hyperliquid 平台上鲸鱼的持仓数据，筛选出价值超过 100 万美元的持仓信息。

***缓存 / 更新频率:*** 实时更新

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "user": "0x20c2d95a3dfdca9e9ad12794d5fa6fad99da44f5", // 用户地址
      "symbol": "ETH",                                   // 币种
      "position_size": -44727.1273,                      // 仓位大小（正为做多，负为做空）
      "entry_price": 2249.7,                             // 开仓价格
      "mark_price": 1645.8,                              // 当前标记价格
      "liq_price": 2358.2766,                            // 强平价格
      "leverage": 25,                                    // 杠杆倍数
      "margin_balance": 2943581.7019,                    // 保证金余额（USD）
      "position_value_usd": 73589542.5467,               // 仓位价值（USD）
      "unrealized_pnl": 27033236.424,                    // 未实现盈亏（USD）
      "funding_fee": -3107520.7373,                      // 资金费用（USD）
      "margin_mode": "cross",                            // 保证金模式（cross 表示全仓）
      "create_time": 1741680802000,                      // 开仓时间（时间戳，毫秒）
      "update_time": 1745219966000                       // 更新时间（时间戳，毫秒）
    },
    {
      "user": "0xf967239debef10dbc78e9bbbb2d8a16b72a614eb",
      "symbol": "BTC",
      "position_size": -800,
      "entry_price": 84931.3,
      "mark_price": 87427,
      "liq_price": 92263.798,
      "leverage": 15,
      "margin_balance": 4812076.3896,
      "position_value_usd": 69921600,
      "unrealized_pnl": -1976493.6819,
      "funding_fee": 14390.0346,
      "margin_mode": "isolated",                         // 保证金模式（isolated 表示逐仓）
      "create_time": 1743982804000,
      "update_time": 1745219969000
    }
  ]
}

```

