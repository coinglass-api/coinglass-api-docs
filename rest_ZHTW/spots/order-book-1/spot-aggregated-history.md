# 現貨 - 訂單簿 - 幣種聚合掛單深度歷史（±範圍）


```
GET /api/spot/orderbook/aggregated-ask-bids-history
```


該接口提供現貨幣種聚合歷史訂單簿數據，包含指定價格範圍內的買盤和賣盤掛單總量。

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
      "aggregated_bids_usd": 12679537.0806,         // 聚合多單金額（美元）
      "aggregated_bids_quantity": 197.99861,        // 聚合多單數量
      "aggregated_asks_usd": 10985519.9268,         // 聚合空單金額（美元）
      "aggregated_asks_quantity": 170.382,          // 聚合空單數量
      "time": 1714003200000                         // 時間戳（毫秒）
    },
    {
      "aggregated_bids_usd": 18423845.1947,
      "aggregated_bids_quantity": 265.483,
      "aggregated_asks_usd": 17384271.5521,
      "aggregated_asks_quantity": 240.785,
      "time": 1714089600000
    }
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                      |
| ------------- | ------- | --- | ------------------------------------------------------- |
| exchange_list | string  | YES | 需要聚合的交易所名稱列表（例如：'ALL'，或 'Binance, OKX, Bybit'）。         |
| symbol        | string  | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。              |
| interval      | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。  |
| limit         | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                          |
| start_time    | integer | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                          |
| end_time      | integer | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                          |
| range         | string  | NO  | 深度百分比（例如：0.25、0.5、0.75、1、2、3、5、10）。                     |

