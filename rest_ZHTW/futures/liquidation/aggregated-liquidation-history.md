# 合約數據 - 爆倉與清算 - 幣種爆倉歷史


```
GET /api/futures/liquidation/aggregated-history
```


該接口提供幣種聚合多個交易所的多空爆倉歷史數據。

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
      "aggregated_long_liquidation_usd": "4611285.1141", // 聚合多單爆倉金額（美元）
      "aggregated_short_liquidation_usd": "4788636.51145", // 聚合空單爆倉金額（美元）
      "time": 1636588800 // 時間戳
    },
    {
      "aggregated_long_liquidation_usd": "4611285.1141", // 聚合多單爆倉金額（美元）
      "aggregated_short_liquidation_usd": "4788636.51145", // 聚合空單爆倉金額（美元）
      "time": 1636588800 // 時間戳
    }
    ..
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                                            |
| ------------- | ------- | --- | ----------------------------------------------------------------------------- |
| exchange_list | string  | YES | 以逗號分隔的交易所名稱（例如："binance, okx, bybit"）。可通過 `support-exchange-pair` 接口獲取支持的交易所。 |
| symbol        | string  | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。                                    |
| interval      | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。                        |
| limit         | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                                                |
| start_time    | integer | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                                                |
| end_time      | integer | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                                                |

