# 期权 - 期权相关数据


```
GET /api/option/info
```


该接口提供不同交易所期权的持仓量与成交量等详细信息。

***缓存/ 更新频率 :*** 30秒更新一次.

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
      "exchange_name": "All",                           // 交易所名称
      "open_interest": 361038.78,                       // 未平仓合约数量（张）
      "oi_market_share": 100,                           // 持仓占有率（%）
      "open_interest_change_24h": 2.72,                 // 24 小时未平仓合约变化（%）
      "open_interest_usd": 31623069708.138245,          // 未平仓合约价值（美元）
      "volume_usd_24h": 2764676957.0569425,             // 24 小时交易量（美元）
      "volume_change_percent_24h": 303.1                // 24 小时交易量变化（%）
    },
    {
      "exchange_name": "Deribit",                       // 交易所名称
      "open_interest": 262641.9,                        // 未平仓合约数量（张）
      "oi_market_share": 72.74,                         // 持仓占有率（%）
      "open_interest_change_24h": 2.57,                 // 24 小时未平仓合约变化（%）
      "open_interest_usd": 23005403973.349,             // 未平仓合约价值（美元）
      "volume_usd_24h": 2080336672.709                  // 24 小时交易量（美元）
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                |
| ------ | ------ | --- | ----------------- |
| symbol | string | YES | 交易币种（例如：BTC、ETH）。 |

