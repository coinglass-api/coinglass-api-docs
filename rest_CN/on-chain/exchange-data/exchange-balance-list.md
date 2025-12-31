# 链上 - 交易所数据 - 交易所余额列表


```
GET /api/exchange/balance/list
```


该接口提供各交易所的资产余额数据，包括 1 天、7 天和 30 天内的余额变化百分比信息。

***缓存/ 更新频率 :*** 1小时一次.

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
      "exchange_name": "Coinbase",               // 交易所名称
      "total_balance": 716590.351233,            // 总余额
      "balance_change_1d": 638.797302,           // 24小时余额变动
      "balance_change_percent_1d": 0.09,         // 24小时余额变动百分比 (%)
      "balance_change_7d": 799.967408,           // 7天余额变动
      "balance_change_percent_7d": 0.11,         // 7天余额变动百分比 (%)
      "balance_change_30d": -29121.977486,       // 30天余额变动
      "balance_change_percent_30d": -3.91        // 30天余额变动百分比 (%)
    },
    {
      "exchange_name": "Binance",                // 交易所名称
      "total_balance": 582344.497738,            // 总余额
      "balance_change_1d": 505.682778,           // 24小时余额变动
      "balance_change_percent_1d": 0.09,         // 24小时余额变动百分比 (%)
      "balance_change_7d": -3784.88544,          // 7天余额变动
      "balance_change_percent_7d": -0.65,        // 7天余额变动百分比 (%)
      "balance_change_30d": 3753.870055,         // 30天余额变动
      "balance_change_percent_30d": 0.65         // 30天余额变动百分比 (%)
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                |
| ------ | ------ | --- | ----------------- |
| symbol | string | YES | 交易币种（例如：BTC、ETH）。 |

