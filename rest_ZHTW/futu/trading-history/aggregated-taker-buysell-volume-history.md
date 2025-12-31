# 合約數據 - 主動買賣 - 幣種主動買賣歷史


```
GET /api/futures/aggregated-taker-buy-sell-volume/history
```


該接口提供合約市場中幣種的主動買入與賣出成交量的歷史數據。

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
      "time": 1741622400000, // 時間戳（毫秒）
      "aggregated_buy_volume_usd": 968834542.3787, // 聚合买单成交量（美元）
      "aggregated_sell_volume_usd": 1054582654.8138 // 聚合卖单成交量（美元）
    },
    {
      "time": 1741626000000,
      "aggregated_buy_volume_usd": 1430620763.2041,
      "aggregated_sell_volume_usd": 1559166911.2821
    },
    {
      "time": 1741629600000,
      "aggregated_buy_volume_usd": 1897261721.0129,
      "aggregated_sell_volume_usd": 2003812276.7812
    }
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                     |
| ------------- | ------- | --- | ------------------------------------------------------ |
| exchange_list | string  | YES | 需要聚合的交易所名稱列表（例如： 'Binance,OKX,Bybit'）。                 |
| symbol        | string  | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。             |
| interval      | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。 |
| limit         | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                         |
| start_time    | integer | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                         |
| end_time      | integer | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                         |
| unit          | string  | NO  | 返回數據的單位，可選值為 'usd' 或 'coin'。                           |

