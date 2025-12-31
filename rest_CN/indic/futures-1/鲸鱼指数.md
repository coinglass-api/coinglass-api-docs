# 指标 - 合约指标 - 鲸鱼指数


```
GET /api/futures/whale-index/history
```


此端点提供鲸鱼指数历史数据。

***缓存/ 更新频率 :*** 实时.

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
      "time": 1665532800000,
      "whale_index_value": -184.8
    },
    {
      "time": 1665619200000,
      "whale_index_value": -118.965
    },
    {
      "time": 1665705600000,
      "whale_index_value": -58.795
    },
    {
      "time": 1665792000000,
      "whale_index_value": -84.095
    },
}
```

 **Parameters:**
| 名称         | 类型     | 必填  | 描述                                                            |
| ---------- | ------ | --- | ------------------------------------------------------------- |
| exchange   | string | YES | 合约交易所名称（例如：Binance、OKX）。可通过 support-exchange-pair 接口获取支持的交易所。 |
| symbol     | string | YES | 交易对（例如：BTCUSDT）。可通过 support-exchange-pair 接口查询支持的交易对          |
| interval   | string | YES | 数据的时间间隔。支持的值：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w           |
| limit      | string | NO  | 每次请求的结果数。默认 1000，最大 1000                                      |
| start_time | string | NO  | 以毫秒为单位的开始时间戳（例如 1641522717000）。                               |
| end_time   | string | NO  | 以毫秒为单位的结束时间戳（例如 1641522717000）。                               |

