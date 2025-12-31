# 指标 - 现货 - Coinbase溢价指数


```
GET /api/coinbase-premium-index
```


该接口提供 Coinbase 比特币溢价指数，反映 Coinbase Pro 与 Binance 之间的比特币价格差异。

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
"time": 1658880000,         // 时间戳（秒）
  "premium": 5.55,            // 溢价金额（USD）
  "premium_rate": 0.0261      // 溢价率（例如 0.0261 表示 2.61%）
    },
    {
"time": 1658880000,         // 时间戳（秒）
  "premium": 5.55,            // 溢价金额（USD）
  "premium_rate": 0.0261      // 溢价率（例如 0.0261 表示 2.61%）
    }
  ]
}
```

 **Parameters:**
| 名称        | 类型      | 必填  | 描述                                                      |
| --------- | ------- | --- | ------------------------------------------------------- |
| interval  | string  | YES | 数据的时间间隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。 |
| limit     | integer | NO  | 每次请求返回的数据条数。默认值为 1000，最大值为 1000。                        |
| startTime | integer | NO  | 开始时间戳（毫秒）（例如：1641522717000）。                            |
| endTime   | integer | NO  | 结束时间戳（毫秒）（例如：1641522717000）。                            |

