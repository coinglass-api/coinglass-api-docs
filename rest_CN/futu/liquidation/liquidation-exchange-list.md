# 合约 - 爆仓与清算 - 币种交易所爆仓列表


```
GET /api/futures/liquidation/exchange-list
```


该接口提供指定币种在各大交易所的爆仓数据列表。

***缓存 / 更新频率:*** 10秒钟一次.

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
      "exchange": "All", // 所有交易所的总数据
      "liquidation_usd": 14673519.81739075, // 总爆仓金额（美元）
      "long_liquidation_usd": 451394.17404598, // 多单爆仓金额（美元）
      "short_liquidation_usd": 14222125.64334477 // 空单爆仓金额（美元）
    },
    {
      "exchange": "Bybit", // 交易所名称
      "liquidation_usd": 4585290.13404, // 总爆仓金额（美元）
      "long_liquidation_usd": 104560.13885, // 多单爆仓金额（美元）
      "short_liquidation_usd": 4480729.99519 // 空单爆仓金额（美元）
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                          |
| ------ | ------ | --- | ------------------------------------------- |
| symbol | string | NO  | 交易币种（例如：BTC）。可通过 support-coins 接口获取支持的币种列表。 |
| range  | string | YES | 数据的时间范围（例如：1h、4h、12h、24h）。                  |

