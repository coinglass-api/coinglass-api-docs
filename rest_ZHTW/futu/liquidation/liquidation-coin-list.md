# 合約數據 - 爆倉與清算 - 交易所幣種爆倉列表


```
GET /api/futures/liquidation/coin-list
```


該接口提供指定交易所內所有幣種的爆倉數據。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "BTC", // 幣種符號
      "liquidation_usd_24h": 82280481.50425325, // 過去24小時總爆倉金額（美元）
      "long_liquidation_usd_24h": 68437447.33734027, // 過去24小時多單爆倉金額（美元）
      "short_liquidation_usd_24h": 13843034.16691298, // 過去24小時空單爆倉金額（美元）

      "liquidation_usd_12h": 68331844.36224127, // 過去12小時總爆倉金額
      "long_liquidation_usd_12h": 66614158.47451427, // 過去12小時多單爆倉金額
      "short_liquidation_usd_12h": 1717685.887727, // 過去12小時空單爆倉金額

      "liquidation_usd_4h": 11381137.080643, // 過去4小時總爆倉金額
      "long_liquidation_usd_4h": 10921633.272973, // 過去4小時多單爆倉金額
      "short_liquidation_usd_4h": 459503.80767, // 過去4小時空單爆倉金額

      "liquidation_usd_1h": 3283635.95309, // 過去1小時總爆倉金額
      "long_liquidation_usd_1h": 3182915.16289, // 過去1小時多單爆倉金額
      "short_liquidation_usd_1h": 100720.7902 // 過去1小時空單爆倉金額
    },
    {
      "symbol": "ETH", // 幣種
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
| 名称       | 类型     | 必填  | 描述                                                           |
| -------- | ------ | --- | ------------------------------------------------------------ |
| exchange | string | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |

