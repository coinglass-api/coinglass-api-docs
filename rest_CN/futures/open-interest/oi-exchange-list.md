# 合约 - 持仓 - 币种交易所持仓


```
GET /api/futures/open-interest/exchange-list
```


该接口提供某个币种在多个交易所的持仓量（Open Interest）数据

***缓存 / 更新频率:*** 10秒钟更新一次

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
      "exchange": "All", // 交易所名称，"All"表示所有交易所汇总
      "symbol": "BTC", // 币种符号

      "open_interest_usd": 57437891724.5572, // 未平仓合约价值(USD)，表示所有未平仓合约的总价值
      "open_interest_quantity": 659557.3064, // 未平仓合约数量，表示所有未平仓合约的总数量

      "open_interest_by_stable_coin_margin": 48920274435.15, // 稳定币本位未平仓合约价值(USD)，合约采用稳定币作为保证金
      "open_interest_quantity_by_coin_margin": 97551.2547, // 币本位未平仓合约数量
      "open_interest_quantity_by_stable_coin_margin": 562006.0517, // 稳定币本位未平仓合约数量

      "open_interest_change_percent_5m": 0.34, // 5分钟内未平仓合约变化百分比
      "open_interest_change_percent_15m": 0.59, // 15分钟内未平仓合约变化百分比
      "open_interest_change_percent_30m": 1.42, // 30分钟内未平仓合约变化百分比
      "open_interest_change_percent_1h": 2.27, // 1小时内未平仓合约变化百分比
      "open_interest_change_percent_4h": 2.95, // 4小时内未平仓合约变化百分比
      "open_interest_change_percent_24h": 0.9 // 24小时内未平仓合约变化百分比
    },
    {
      "exchange": "CME", // 交易所名称
      "symbol": "BTC", // 币种符号

      "open_interest_usd": 12294999402.5, // 未平仓合约价值(USD)，表示所有未平仓合约的总价值
      "open_interest_quantity": 141275.5, // 未平仓合约数量，表示所有未平仓合约的总数量

      "open_interest_by_stable_coin_margin": 12294999402.5, // 稳定币本位未平仓合约价值(USD)，合约采用稳定币作为保证金
      "open_interest_quantity_by_coin_margin": 0, // 币本位未平仓合约数量
      "open_interest_quantity_by_stable_coin_margin": 141275.5, // 稳定币本位未平仓合约数量

      "open_interest_change_percent_5m": 0.08, // 5分钟内未平仓合约变化百分比
      "open_interest_change_percent_15m": 0.14, // 15分钟内未平仓合约变化百分比
      "open_interest_change_percent_30m": 0.49, // 30分钟内未平仓合约变化百分比
      "open_interest_change_percent_1h": 1.13, // 1小时内未平仓合约变化百分比
      "open_interest_change_percent_4h": 2.4, // 4小时内未平仓合约变化百分比
      "open_interest_change_percent_24h": 2.08 // 24小时内未平仓合约变化百分比
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                          |
| ------ | ------ | --- | ------------------------------------------- |
| symbol | string | YES | 交易币种（例如：BTC）。可通过 support-coins 接口获取支持的币种列表。 |

