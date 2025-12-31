# 合约 - Hyperliquid 仓位 - Hyperliquid 鲸鱼提醒


```
GET /api/hyperliquid/whale-alert
```


该接口提供 Hyperliquid 平台上实时的鲸鱼交易提醒，突出展示价值超过 100 万美元的大额持仓变动。（最多可返回 200 条最新数据）

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
      "user": "0x3fd4444154242720c0d0c61c74a240d90c127d33", // 用户地址
      "symbol": "ETH",                                     // 币种
      "position_size": 12700,                              // 仓位大小（正数为多，负数为空）
      "entry_price": 1611.62,                              // 开仓价格
      "liq_price": 527.2521,                               // 强平价格
      "position_value_usd": 21003260,                      // 仓位价值（美元）
      "position_action": 2,                                // 仓位操作类型（1: 开仓，2: 平仓）
      "create_time": 1745219517000                         // 开仓时间（时间戳，毫秒）
    },
    {
      "user": "0x1cadadf0e884ac5527ae596a4fc1017a4ffd4e2c",
      "symbol": "BTC",
      "position_size": 33.54032,
      "entry_price": 87486.2,
      "liq_price": 44836.8126,
      "position_value_usd": 2936421.4757,
      "position_action": 2,
      "create_time": 1745219477000
    }
  ]
}

```

