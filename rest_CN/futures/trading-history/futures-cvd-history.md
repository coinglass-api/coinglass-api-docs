# 合约 - 主动买卖 - 累计成交量差值（CVD）


```
GET /api/futures/cvd/history
```


该接口提供合约交易所交易对的历史累计成交量差值（CVD）数据，包含随时间变化的主动买入量（taker buy）与主动卖出量（taker sell）。

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
      "taker_buy_vol": 350281007.0211,
      "taker_sell_vol": 325339470.9493,
      "cum_vol_delta": 24941536.0718
    },
    {
      "time": 1762257600,
      "taker_buy_vol": 286399814.1275,
      "taker_sell_vol": 347409544.4937,
      "cum_vol_delta": -36068194.2944
    },
    {
      "time": 1762261200,
      "taker_buy_vol": 299952362.4807,
      "taker_sell_vol": 323978642.5934,
      "cum_vol_delta": -60094474.4071
    },
  ]
}
```

 **Parameters:**
| 名称         | 类型      | 必填  | 描述                                                                                                      |
| ---------- | ------- | --- | ------------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES | 交易所名称（例如：Binance、OKX）。支持的交易所可通过 support-exchange-pair 接口获取。                                             |
| symbol     | string  | YES | 交易对（例如：BTCUSDT）。支持的交易对可通过 support-exchange-pair 接口获取。                                                   |
| interval   | string  | YES | Time interval for data aggregation. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w |
| limit      | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                                                                        |
| start_time | integer | NO  | 起始时间戳（毫秒）（例如：1641522717000）。                                                                            |
| end_time   | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                                                                            |

