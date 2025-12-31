# 现货 - 订单薄 - 币种聚合挂单深度历史(±范围)


```
GET /api/spot/orderbook/aggregated-ask-bids-history
```


该接口提供现货币种聚合历史订单簿数据，包含指定价格范围内的买盘和卖盘挂单总量。

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版    | 创业版      | 标准版 | 专业版 | 企业版 |
| :----- | :----- | :------- | :-- | :-- | :-- |
| 可用性    | ✅      | ✅        | ✅   | ✅   | ✅   |
| 颗粒度    | `>=4h` | ​`>=30m` | 无限制 | 无限制 | 无限制 |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "aggregated_bids_usd": 12679537.0806,         // 聚合多单金额（美元）
      "aggregated_bids_quantity": 197.99861,        // 聚合多单数量
      "aggregated_asks_usd": 10985519.9268,         // 聚合空单金额（美元）
      "aggregated_asks_quantity": 170.382,          // 聚合空单数量
      "time": 1714003200000                         // 时间戳（毫秒）
    },
    {
      "aggregated_bids_usd": 18423845.1947,
      "aggregated_bids_quantity": 265.483,
      "aggregated_asks_usd": 17384271.5521,
      "aggregated_asks_quantity": 240.785,
      "time": 1714089600000
    }
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                      |
| ------------- | ------- | --- | ------------------------------------------------------- |
| exchange_list | string  | YES | 需要聚合的交易所名称列表（例如：'ALL'，或 'Binance, OKX, Bybit'）。         |
| symbol        | string  | YES | 交易币种（例如：BTC）。可通过 support-coins 接口获取支持的币种列表。             |
| interval      | string  | YES | 数据的时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。 |
| limit         | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                        |
| start_time    | integer | NO  | 开始时间戳（毫秒）（例如：1641522717000）。                            |
| end_time      | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                            |
| range         | string  | NO  | 深度百分比（例如：0.25、0.5、0.75、1、2、3、5、10）。                     |

