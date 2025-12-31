# 合约 - 爆仓与清算 - 爆仓订单


```
GET /api/futures/liquidation/order
```


该接口提供过去7天内的爆仓订单数据，包含交易所、交易对及爆仓金额等详细信息。

***缓存 / 更新频率:*** 1秒钟一次.

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
      "exchange_name": "BINANCE", // 交易所名称
      "symbol": "BTCUSDT", // 交易对符号
      "base_asset": "BTC", // 币种
      "price": 87535.9, // 爆仓价格
      "usd_value": 205534.2932, // 成交金额（美元）
      "side": 2, // 订单方向（1：买入，2：卖出）
      "time": 1745216319263 // 时间戳
    },
    {
      "exchange_name": "BINANCE", // 交易所名称
      "symbol": "BTCUSDT", // 交易对符号
      "base_asset": "BTC", // 币种
      "price": 87465.2, // 爆仓价格
      "usd_value": 15918.6664, // 成交金额（美元）
      "side": 2, // 订单方向（1：买入，2：卖出）
      "time": 1745215647165 // 时间戳
    }
  ]
}

```

 **Parameters:**
| 名称                     | 类型      | 必填  | 描述                                                            |
| ---------------------- | ------- | --- | ------------------------------------------------------------- |
| exchange               | string  | YES | 交易所名称（例如：Binance、OKX）。可通过 support-exchange-pair 接口获取支持的交易所列表。 |
| symbol                 | string  | YES | 交易币种（例如：BTC）。可通过 support-coins 接口获取支持的币种列表。                   |
| min_liquidation_amount | string  | YES | 爆仓订单的最小金额阈值。每个请求最多返回 200 条记录                                  |
| start_time             | integer | NO  | 开始时间戳（毫秒）（例如：1641522717000）。                                  |
| end_time               | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                                  |

