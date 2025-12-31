# 现货 - 订单薄 - 大额订单薄


```
GET /api/spot/orderbook/large-limit-order
```


该接口提供现货交易中当前订单簿中的大额限价挂单数据。(阈值: BTC ≥ 35万, ETH ≥ 25万, Other ≥ 1万)

***缓存 / 更新频率:*** 实时更新

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 响应数据

```json
  "code": "0",
  "msg": "success",
  "data":[
  {
    "id": 2536823422,
    "exchange_name": "Binance",            // 交易所名称
    "symbol": "BTCUSDT",                   // 交易对
    "base_asset": "BTC",                   // 基础币种
    "quote_asset": "USDT",                 // 计价币种

    "limit_price": 56932,                  // 委托价格
    "start_time": 1722964242000,           // 委托开始时间（毫秒）
    "start_quantity": 28.39774,            // 初始数量
    "start_usd_value": 1616740.1337,       // 初始价值（USD）

    "current_quantity": 18.77405,          // 当前剩余数量
    "current_usd_value": 1068844.21,       // 当前剩余价值（USD）
    "current_time": 1722964272000,         // 当前时间（毫秒）

    "executed_volume": 0,                  // 成交数量
    "executed_usd_value": 0,               // 成交价值（USD）
    "trade_count": 0,                      // 成交笔数

    "order_side": 2,                       // 委托方向：1-卖单，2-买单
    "order_state": 1                       // 委托状态：1-挂单中，2-已完成，3-已撤销
  }
]
}
```

 **Parameters:**
| 名称       | 类型     | 必填  | 描述                                                            |
| -------- | ------ | --- | ------------------------------------------------------------- |
| exchange | string | YES | 交易所名称（例如：Binance、OKX）。可通过 support-exchange-pair 接口获取支持的交易所列表。 |
| symbol   | string | YES | 交易对（例如：BTCUSDT）。可通过 support-exchange-pair 接口获取支持的交易对列表。       |

