# 指标 - 合约指标 - 指数移动平均线 (EMA)


```
GET /api/futures/indicators/ema
```


该接口用于获取交易对的指数移动平均线 (EMA)。

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
      "time": 1677196800000,
      "ema_value": 24175.55
    },
    {
      "time": 1677283200000,
      "ema_value": 24133.28
    },
    ....
  ]
}
```

 **Parameters:**
| 名称          | 类型      | 必填  | 描述                                                          |
| ----------- | ------- | --- | ----------------------------------------------------------- |
| exchange    | string  | YES | 交易所名称（例如：Binance、OKX）。支持的交易所可通过 support-exchange-pair 接口获取。 |
| symbol      | string  | YES | 交易对（例如：BTCUSDT）。支持的交易对可通过 support-exchange-pair 接口获取。       |
| interval    | string  | YES | 数据时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。      |
| limit       | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                            |
| start_time  | integer | NO  | 起始时间戳（毫秒）（例如：1641522717000）。                                |
| end_time    | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                                |
| window      | integer | NO  | 窗口大小 —— 定义用于指标计算的数据点数量（例如：EMA 的窗口为 10）。                     |
| series_type | string  | NO  | 价格类型 —— 指定计算中使用的价格类型。支持的取值：open、high、low、close。默认值：close。   |

