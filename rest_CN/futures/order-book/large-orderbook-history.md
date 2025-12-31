# 合约 - 订单薄 - 大额订单薄历史


```
GET /api/futures/orderbook/large-limit-order-history
```


该接口提供合约交易中已完成的大额限价挂单的历史数据。(阈值: BTC ≥ 100万, ETH ≥ 50万, Other ≥ 5万)

***缓存 / 更新频率:*** 实时更新

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
      "id": 2895605135,
      "exchange_name": "Binance",               // 交易所名称
      "symbol": "BTCUSDT",                      // 交易对
      "base_asset": "BTC",                      // 基础币种
      "quote_asset": "USDT",                    // 计价币种
      "price": 89205.9,                         // 委托价格
      "start_time": 1745287309000,              // 委托开始时间 (毫秒)
      "start_quantity": 25.779,                 // 初始委托数量
      "start_usd_value": 2299638.8961,          // 初始委托价值 (USD)
      "current_quantity": 25.779,               // 当前剩余数量
      "current_usd_value": 2299638.8961,        // 当前剩余价值 (USD)
      "current_time": 1745287309000,            // 当前时间 (毫秒)
      "executed_volume": 0,                     // 累计成交量
      "executed_usd_value": 0,                  // 累计成交价值 (USD)
      "trade_count": 0,                         // 累计成交笔数
      "order_side": 1,                          // 委托方向：1-卖单，2-买单
      "order_state": 2,                         // 委托状态：0-未开始，1-挂单中，2-已完成，3-已撤销
      "order_end_time": 1745287328000           // 完成或撤销订单的结束时间 (毫秒)
    },
    ...
  ]
}

```

 **Parameters:**
| 名称         | 类型      | 必填  | 描述                                                           |
| ---------- | ------- | --- | ------------------------------------------------------------ |
| exchange   | string  | YES | 交易所名称（例如：Binance、OKX）。可通过 support-exchange-pair 接口获取支持的交易所列表 |
| symbol     | string  | YES | 交易对（例如：BTCUSDT）。可通过 support-exchange-pair 接口获取支持的交易对列表。      |
| start_time | integer | YES | 开始时间戳（毫秒）（例如：1641522717000）。                                 |
| end_time   | integer | YES | 结束时间戳（毫秒）（例如：1641522717000）。                                 |
| state      | integer | YES | 订单状态说明如下：  1：进行中（In Progress）  2：已完成（Finish）  3：已撤销（Revoke）  |

