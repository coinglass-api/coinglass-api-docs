# 合约 - 资金费率 - 累计资金费率-交易所列表


```
GET /api/futures/funding-rate/accumulated-exchange-list
```


该接口提供各交易所的币种累计资金费率数据。

***缓存 / 更新频率:*** 1小时一次

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
      "symbol": "BTC", // 币种
      "stablecoin_margin_list": [ // USDT/USD 保证金模式的累计资金费率
        {
          "exchange": "BINANCE", // 交易所名称
          "funding_rate": 0.001873 // 累计资金费率
        },
        {
          "exchange": "OKX", // 交易所名称
          "funding_rate": 0.00775484 // 累计资金费率
        }
      ],
      "token_margin_list": [ // 币本位保证金模式的累计资金费率
        {
          "exchange": "BINANCE", // 交易所名称
          "funding_rate": -0.003149 // 累计资金费率
        }
      ]
    }
  ]
}

```

 **Parameters:**
| 名称    | 类型     | 必填  | 描述                               |
| ----- | ------ | --- | -------------------------------- |
| range | string | YES | 数据的时间范围 (例如.,1d, 7d, 30d, 365d). |

