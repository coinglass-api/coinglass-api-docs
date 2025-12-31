# 合约 - 资金费率 - 币种资金费率-交易所列表


```
GET /api/futures/funding-rate/exchange-list
```


该接口提供各交易所的币种资金费率数据。

***缓存 / 更新频率:*** 20秒一次

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
      "stablecoin_margin_list": [ // USDT/USD 保证金模式
        {
          "exchange": "Binance", // 交易所
          "funding_rate_interval": 8, // 资金费率结算周期（小时）
          "funding_rate": 0.007343, // 当前资金费率
          "next_funding_time": 1745222400000 // 下次资金费率结算时间（毫秒）
        },
        {
          "exchange": "OKX", // 交易所
          "funding_rate_interval": 8, // 资金费率结算周期（小时）
          "funding_rate": 0.00736901950628, // 当前资金费率
          "next_funding_time": 1745222400000 // 下次资金费率结算时间（毫秒）
        }
      ],
      "token_margin_list": [ // 币本位保证金模式
        {
          "exchange": "Binance", // 交易所
          "funding_rate_interval": 8, // 资金费率结算周期（小时）
          "funding_rate": -0.001829, // 当前资金费率
          "next_funding_time": 1745222400000 // 下次资金费率结算时间（毫秒）
        }
      ]
    }
  ]
}

```

