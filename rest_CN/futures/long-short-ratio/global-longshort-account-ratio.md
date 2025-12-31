# 合约 - 多空比 - 交易对账户多空比历史


```
GET /api/futures/global-long-short-account-ratio/history
```


该接口提供交易所交易对的多空账户比历史数据。

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
      "time": 1741604400000, // 时间戳（毫秒）
      "global_account_long_percent": 73.88, // 账户多单比例（%）
      "global_account_short_percent": 26.12, // 账户空单比例（%）
      "global_account_long_short_ratio": 2.83 // 账户多空比（多/空）
    },
    {
      "time": 1741608000000, // 时间戳（毫秒）
      "global_account_long_percent": 73.24, // 账户多单比例（%）
      "global_account_short_percent": 26.76, // 账户空单比例（%）
      "global_account_long_short_ratio": 2.74 // 账户多空比（多/空）
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

