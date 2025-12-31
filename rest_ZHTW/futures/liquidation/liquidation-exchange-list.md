# 合約數據 - 爆倉與清算 - 幣種交易所爆倉列表


```
GET /api/futures/liquidation/exchange-list
```


該接口提供指定幣種在各大交易所的爆倉數據列表。

***快取 / 更新頻率:*** 每 10 秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版    | 創業版      | 標準版 | 專業版 | 企業版 |
| :----- | :----- | :------- | :-- | :-- | :-- |
| 可用性    | ✅      | ✅        | ✅   | ✅   | ✅   |
| 颗粒度    | `>=4h` | ​`>=30m` | 無限制 | 無限制 | 無限制 |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "exchange": "All", // 所有交易所的總資料
      "liquidation_usd": 14673519.81739075, // 總爆倉金額（美元）
      "long_liquidation_usd": 451394.17404598, // 多單爆倉金額（美元）
      "short_liquidation_usd": 14222125.64334477 // 空單爆倉金額（美元）
    },
    {
      "exchange": "Bybit", // 交易所名稱
      "liquidation_usd": 4585290.13404, // 總爆倉金額（美元）
      "long_liquidation_usd": 104560.13885, // 多單爆倉金額（美元）
      "short_liquidation_usd": 4480729.99519 // 空單爆倉金額（美元）
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                         |
| ------ | ------ | --- | ------------------------------------------ |
| symbol | string | NO  | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。 |
| range  | string | YES | 數據時間間隔。支持的取值包括：1h、4h、12h、24h               |

