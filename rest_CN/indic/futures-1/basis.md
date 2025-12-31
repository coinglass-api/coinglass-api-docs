# 指标 - 合约指标 - 合约基差


```
GET /api/futures/basis/history
```


该接口提供合约基差的历史数据，包括开盘与收盘时的基差数值

***缓存/ 更新频率 :*** 实时.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1741629600000,            // 时间戳（毫秒）
      "open_basis": 0.0504,             // 开盘基差（单位：%）
      "close_basis": 0.0445,            // 收盘基差（单位：%）
      "open_change": 39.5,              // 开盘时基差相较前一时段变化幅度（单位：%）
      "close_change": 34.56             // 收盘时基差相较前一时段变化幅度（单位：%）
    },
    {
      "time": 1741633200000,            // 时间戳（毫秒）
      "open_basis": 0.0446,             // 开盘基差（单位：%）
      "close_basis": 0.03,              // 收盘基差（单位：%）
      "open_change": 34.65,             // 开盘时基差变化幅度（单位：%）
      "close_change": 23.74             // 收盘时基差变化幅度（单位：%）
    }
  ]
}

```

 **Parameters:**
| 名称         | 类型     | 必填  | 描述                                                            |
| ---------- | ------ | --- | ------------------------------------------------------------- |
| exchange   | string | YES | 交易所名称（例如：Binance、OKX）。可通过 support-exchange-pair 接口获取支持的交易所列表。 |
| symbol     | string | YES | 交易对（例如：BTCUSDT）。可通过 support-exchange-pair 接口获取支持的交易对列表        |
| interval   | string | YES | 数据的时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w        |
| limit      | string | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                              |
| start_time | string | NO  | 开始时间戳（毫秒）（例如：1641522717000）。                                  |
| end_time   | string | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                                  |

