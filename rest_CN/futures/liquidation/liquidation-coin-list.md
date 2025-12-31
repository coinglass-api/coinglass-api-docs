# 合约 - 爆仓与清算 - 交易所币种爆仓列表


```
GET /api/futures/liquidation/coin-list
```


该接口提供指定交易所内所有币种的爆仓数据。

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
      "symbol": "BTC", // 币种符号
      "liquidation_usd_24h": 82280481.50425325, // 过去24小时总爆仓金额（美元）
      "long_liquidation_usd_24h": 68437447.33734027, // 过去24小时多单爆仓金额（美元）
      "short_liquidation_usd_24h": 13843034.16691298, // 过去24小时空单爆仓金额（美元）

      "liquidation_usd_12h": 68331844.36224127, // 过去12小时总爆仓金额
      "long_liquidation_usd_12h": 66614158.47451427, // 过去12小时多单爆仓金额
      "short_liquidation_usd_12h": 1717685.887727, // 过去12小时空单爆仓金额

      "liquidation_usd_4h": 11381137.080643, // 过去4小时总爆仓金额
      "long_liquidation_usd_4h": 10921633.272973, // 过去4小时多单爆仓金额
      "short_liquidation_usd_4h": 459503.80767, // 过去4小时空单爆仓金额

      "liquidation_usd_1h": 3283635.95309, // 过去1小时总爆仓金额
      "long_liquidation_usd_1h": 3182915.16289, // 过去1小时多单爆仓金额
      "short_liquidation_usd_1h": 100720.7902 // 过去1小时空单爆仓金额
    },
    {
      "symbol": "ETH", // 币种
      "liquidation_usd_24h": 40690629.51728708,
      "long_liquidation_usd_24h": 23696395.11024007,
      "short_liquidation_usd_24h": 16994234.40704701,
      "liquidation_usd_12h": 24938270.19977256,
      "long_liquidation_usd_12h": 22675785.96343007,
      "short_liquidation_usd_12h": 2262484.23634249,
      "liquidation_usd_4h": 8034894.33790068,
      "long_liquidation_usd_4h": 7683841.24631068,
      "short_liquidation_usd_4h": 351053.09159,
      "liquidation_usd_1h": 6103879.82428372,
      "long_liquidation_usd_1h": 6098481.11604372,
      "short_liquidation_usd_1h": 5398.70824
    }
  ]
}

```

 **Parameters:**
| 名称       | 类型     | 必填  | 描述                                                            |
| -------- | ------ | --- | ------------------------------------------------------------- |
| exchange | string | YES | 交易所名称（例如：Binance、OKX）。可通过 support-exchange-pair 接口获取支持的交易所列表。 |

