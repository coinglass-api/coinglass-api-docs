# 指标 - 合约指标 - 移动平均收敛发散指标 (MACD)


```
GET /api/futures/indicators/macd
```


该接口用于获取交易对的移动平均收敛发散指标 (MACD)。

***缓存/ 更新频率***：实时更新

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
      "time": 1678665600000,
      "macd_value": -837.307
    },
    {
      "time": 1678752000000,
      "macd_value": -575.43
    },
    ....
  ]
}
```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                          |
| ------------- | ------- | --- | ----------------------------------------------------------- |
| exchange      | string  | YES | 交易所名称（例如：Binance、OKX）。支持的交易所可通过 support-exchange-pair 接口获取。 |
| symbol        | string  | YES | 交易对（例如：BTCUSDT）。支持的交易对可通过 support-exchange-pair 接口获取。       |
| interval      | string  | YES | 数据时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。      |
| limit         | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                            |
| start_time    | integer | NO  | 起始时间戳（毫秒）（例如：1641522717000）。                                |
| end_time      | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                                |
| series_type   | string  | NO  | 价格类型 —— 指定计算中使用的价格类型。支持的取值：open、high、low、close。默认值：close。   |
| fast_window   | integer | NO  | 用于指标计算的快速周期窗口大小（例如：MACD 的快速周期为 12）。                         |
| slow_window   | integer | NO  | 用于指标计算的慢速周期窗口大小（例如：MACD 的慢速周期为 26）。                         |
| signal_window | integer | NO  | 用于平滑快慢线差值的信号线窗口大小（例如：MACD 的信号线周期为 9）。                       |

