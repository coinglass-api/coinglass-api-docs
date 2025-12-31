# 合约 - 资金费率 - 资金费率套利


```
GET /api/futures/funding-rate/arbitrage
```


该接口提供不同交易所间的合约币种资金费率套利数据。

***缓存/ 更新频率 :*** 20秒一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "SUPRA", // 币种名称

      "buy": { // 做多的交易所信息（低资金费率）
        "exchange": "MEXC", // 交易所名称
        "open_interest_usd": 848218.2833, // 平台未平仓合约金额（美元）
        "funding_rate_interval": 4, // 资金费率结算间隔（小时）
        "funding_rate": -0.994 // 当前资金费率（%）
      },

      "sell": { // 做空的交易所信息（高资金费率）
        "exchange": "Gate.io", // 交易所名称
        "open_interest_usd": 448263.5072, // 平台未平仓合约金额（美元）
        "funding_rate_interval": 4, // 资金费率结算间隔（小时）
        "funding_rate": 0.005 // 当前资金费率（%）
      },

      "apr": 2187.81, // 年化收益率（APR，%）
      "funding": 0.999, // 资金费率收益差（long和short之间的资金费率差）
      "fee": 0.03, // 交易手续费率（双边总和）
      "spread": -0.09, // 跨平台价格差（%）
      "next_funding_time": 1745222400000 // 下一次资金费率结算时间（时间戳，毫秒）
    }
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                               |
| ------------- | ------- | --- | -------------------------------- |
| usd           | integer | YES | 套利投资本金（例如：10000）                 |
| exchange_list | string  | NO  | 筛选交易所名称列表（例如“Binance,OKX,Bybit”） |

