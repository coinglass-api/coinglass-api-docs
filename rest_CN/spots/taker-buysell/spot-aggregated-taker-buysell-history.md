# 现货 - 主动买卖 - 币种主动买卖历史


```
GET /api/spot/aggregated-taker-buy-sell-volume/history
```


该接口提供现货市场中币种的主动买入与卖出成交量的历史数据

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
      "aggregated_buy_volume_usd": 968834542.3787, // 聚合买单成交量（美元）
      "aggregated_sell_volume_usd": 1054582654.8138 // 聚合卖单成交量（美元）
    },
    {
      "time": 1741626000000,
      "aggregated_buy_volume_usd": 1430620763.2041,
      "aggregated_sell_volume_usd": 1559166911.2821
    },
    {
      "time": 1741629600000,
      "aggregated_buy_volume_usd": 1897261721.0129,
      "aggregated_sell_volume_usd": 2003812276.7812
    }
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                      |
| ------------- | ------- | --- | ------------------------------------------------------- |
| exchange_list | string  | YES | 选择聚合的交易所（例如： 'Binance, OKX, Bybit'）。                    |
| symbol        | string  | YES | 交易币种（例如：BTC）。可通过 support-coins 接口获取支持的币种列表。             |
| interval      | string  | YES | 数据的时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。 |
| limit         | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                        |
| start_time    | integer | NO  | 开始时间戳（毫秒）（例如：1641522717000）。                            |
| end_time      | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                            |
| unit          | string  | NO  | 返回数据的单位，可选值为 'usd' 或 'coin'。                            |

