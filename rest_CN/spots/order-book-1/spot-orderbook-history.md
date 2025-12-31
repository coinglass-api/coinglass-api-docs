# 现货 - 订单薄 - 交易对挂单深度历史(±范围)


```
GET /api/spot/orderbook/ask-bids-history
```


该接口提供现货交易对的历史订单簿数据，包含指定价格范围内的买盘和卖盘挂单总量。

***缓存 / 更新频率:*** 5秒一次.

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
      "bids_usd": 81639959.9338,        // 多单总金额（美元）
      "bids_quantity": 1276.645,        // 多单总数量
      "asks_usd": 78533053.6862,        // 空单总金额（美元）
      "asks_quantity": 1217.125,        // 空单总数量
      "time": 1714003200000             // 时间戳（毫秒）
    },
    {
      "bids_usd": 62345879.8821,
      "bids_quantity": 980.473,
      "asks_usd": 65918423.4715,
      "asks_quantity": 1021.644,
      "time": 1714089600000
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
| range      | string  | NO  | 深度百分比（例如：0.25、0.5、0.75、1、2、3、5、10）。                           |

