# 合约 - 多空比 - 净持仓


```
GET /api/futures/net-position/history
```


该接口提供合约的历史净持仓数据，包括净多仓位变化和净空仓位变化。

***缓存/ 更新频率 :*** 实时更新.

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
      "net_long_change": -478.43,//数量
      "net_short_change": 0,
      "time": 1751652000000
    },
    {
      "net_long_change": -776.79,
      "net_short_change": 0,
      "time": 1751655600000
    },
}
```

 **Parameters:**
| 名称         | 类型      | 必填  | 描述                                                              |
| ---------- | ------- | --- | --------------------------------------------------------------- |
| exchange   | string  | YES | 交易所名称（例如：Binance、OKX）。可通过 supported-exchange-pair 接口获取支持的交易所列表。 |
| symbol     | string  | YES | 交易对（例如：BTCUSDT）。可通过 supported-exchange-pair 接口获取支持的交易对列表。       |
| interval   | string  | YES | 数据的时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。         |
| limit      | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                                |
| start_time | integer | NO  | 开始时间戳（毫秒）（例如：1641522717000）。                                    |
| end_time   | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                                    |

