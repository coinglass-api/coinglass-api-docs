# 合约 - Hyperliquid 仓位 - Hyperliquid 仓位


```
GET /api/hyperliquid/position
```


该接口提供 Hyperliquid 上的仓位数据，包括每个账户的用户地址、仓位大小、保证金余额和未实现盈亏。

***缓存/ 更新频率 :*** 实时更新.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",                     // 状态码（0 表示成功）
  "data": {
    "total_pages": 10,          // 仓位数据的总页数
    "current_page": 1,            // 当前返回的页码
    "list": [
      {
        "user": "0x5b5d51203a0f9079f8aeb098a6523a13f298c060",     // 用户钱包地址
        "symbol": "BTC",           // 交易对（币种）
        "position_size": -2683.14, // 仓位大小（正数为做多，负数为做空）
        "entry_price": 111459.6,   // 开仓价格
        "mark_price": 116638,      // 当前标记价格
        "liq_price": 150629.52,    // 强平价格
        "leverage": 10,            // 杠杆倍数
        "margin_balance": 31263482.07,        // 保证金余额（美元）
        "position_value_usd": 312634820.77,   // 仓位价值（美元）
        "unrealized_pnl": -13572345.06,       // 未实现盈亏（美元）
        "funding_fee": -12534553.66,          // 资金费用（美元）
        "margin_mode": "cross",               // 保证金模式（"cross" 表示全仓，"isolated" 表示逐仓）
        "create_time": 1752152867098,         // 开仓时间（时间戳，毫秒）
        "update_time": 1758162698266          // 更新时间（时间戳，毫秒）
      }
    ]
  }
}

```

 **Parameters:**
| 名称           | 类型      | 必填  | 描述                                           |
| ------------ | ------- | --- | -------------------------------------------- |
| symbol       | string  | YES | 交易币种（例如：BTC）。通过 supported-coins API 获取支持的币种。 |
| current_page | integer | NO  | 返回当前页码                                       |

