# 現貨 - 主動買賣 - 交易對主動買賣歷史


```
GET /api/spot/taker-buy-sell-volume/history
```


該接口提供現貨市場中交易對的主動買入與賣出成交量的歷史數據。

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
      "taker_buy_volume_usd": "10551.033", // 主動買入成交量（美元）
      "taker_sell_volume_usd": "11308" // 主動賣出成交量（美元）
    },
    {
      "time": 1741626000000,
      "taker_buy_volume_usd": "15484.245",
      "taker_sell_volume_usd": "16316.118"
    },
    {
      "time": 1741629600000,
      "taker_buy_volume_usd": "20340.501",
      "taker_sell_volume_usd": "18977.660"
    }
  ]
}

```

 **Parameters:**
| 名称         | 类型      | 必填  | 描述                                                           |
| ---------- | ------- | --- | ------------------------------------------------------------ |
| exchange   | string  | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |
| symbol     | string  | YES | 交易對（例如：BTCUSDT）。可透過 support-exchange-pair 接口查詢支持的交易對。        |
| interval   | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。       |
| limit      | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                               |
| start_time | integer | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                               |
| end_time   | integer | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                               |

