# 合约 - 主动买卖 - 聚合累计成交量差值（CVD）


```
GET /api/futures/aggregated-cvd/history
```


该接口提供合约交易所币种的历史 CVD 数据，是该币种的多个交易对聚合数据。

***缓存 / 更新频率:*** 实时.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "data": [
    {
      "time": 1762254000000,
      "agg_taker_buy_vol": 461937243.0899,
      "agg_taker_sell_vol": 415687343.2719,
      "cum_vol_delta": 46249899.818
    },
    {
      "time": 1762257600,
      "agg_taker_buy_vol": 390296231.4588,
      "agg_taker_sell_vol": 469137635.9107,
      "cum_vol_delta": -32591504.6339
    },
    {
      "time": 1762261200,
      "agg_taker_buy_vol": 461378798.1884,
      "agg_taker_sell_vol": 450407935.7885,
      "cum_vol_delta": -21620642.234
    },
  ]
}
```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                                          |
| ------------- | ------- | --- | --------------------------------------------------------------------------- |
| exchange_list | string  | YES | 以逗号分隔的交易所名称（例如："binance, okx, bybit"）。可通过 support-exchange-pair 接口获取支持的交易所。 |
| symbol        | string  | YES | 交易币种（例如：BTC）。通过 support-coins API 获取支持的币种。                                  |
| interval      | integer | YES | 每次请求的结果数量。默认值：1000，最大值：1000。                                                |
| limit         | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                                            |
| start_time    | integer | NO  | 起始时间戳（单位：毫秒，例如：1641522717000）。                                              |
| end_time      | integer | NO  | 结束时间戳（单位：毫秒，例如：1641522717000）。                                              |
| unit          | string  | NO  | 返回数据的单位，可以选择 'usd' 或 'coin'。                                                |

