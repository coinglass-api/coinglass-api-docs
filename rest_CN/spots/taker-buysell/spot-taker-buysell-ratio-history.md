# 现货 - 主动买卖 - 交易对主动买卖历史


```
GET /api/spot/taker-buy-sell-volume/history
```


该接口提供现货市场中交易对的主动买入与卖出成交量的历史数据

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
      "time": 1741622400000, // 时间戳（毫秒）
      "taker_buy_volume_usd": "10551.033", // 主动买入成交量（美元）
      "taker_sell_volume_usd": "11308" // 主动卖出成交量（美元）
    },
    {
      "time": 1741626000000,
      "taker_buy_volume_usd": "15484.245",
      "taker_sell_volume_usd": "16316.118"
    },
    {
      "time": 1741629600000,
      "taker_buy_volume_usd": "20340.501",
      "taker_sell_volume_usd": "18977.660"
    }
  ]
}

```

 **Parameters:**
| 名称         | 类型      | 必填  | 描述                                                            |
| ---------- | ------- | --- | ------------------------------------------------------------- |
| exchange   | string  | YES | 交易所名称（例如：Binance、OKX）。可通过 support-exchange-pair 接口获取支持的交易所列表。 |
| symbol     | string  | YES | 交易对（例如：BTCUSDT）。可通过 support-exchange-pair 接口获取支持的交易对列表。       |
| interval   | string  | YES | 数据的时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。       |
| limit      | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                              |
| start_time | integer | NO  | 开始时间戳（毫秒）（例如：1641522717000）。                                  |
| end_time   | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                                  |

