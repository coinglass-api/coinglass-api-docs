# 合约 - 爆仓与清算 - 币种爆仓历史


```
GET /api/futures/liquidation/aggregated-history
```


该接口提供币种聚合多个交易所的多空爆仓历史数据。

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
      "aggregated_long_liquidation_usd": "4611285.1141", // 聚合多单爆仓金额（美元）
      "aggregated_short_liquidation_usd": "4788636.51145", // 聚合空单爆仓金额（美元）
      "time": 1636588800 // 时间戳
   },
    {
      "aggregated_long_liquidation_usd": "4611285.1141", // 聚合多单爆仓金额（美元）
      "aggregated_short_liquidation_usd": "4788636.51145", // 聚合空单爆仓金额（美元）
      "time": 1636588800 // 时间戳
   },
    ..
  ]
}


```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                                            |
| ------------- | ------- | --- | ----------------------------------------------------------------------------- |
| exchange_list | string  | YES | 以逗号分隔的交易所名称（例如："Binance, OKX, Bybit"）。可通过 support-exchange-pair 接口获取支持的交易所列表。 |
| symbol        | string  | YES | 交易币种（例如：BTC）。可通过 support-coins 接口获取支持的币种列表。                                   |
| interval      | string  | YES | 数据的时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。                       |
| limit         | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                                              |
| start_time    | integer | NO  | 开始时间戳（毫秒）（例如：1641522717000）。                                                  |
| end_time      | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                                                  |

