# 現貨 - 訂單簿 - 交易對掛單深度歷史（±範圍）


```
GET /api/spot/orderbook/ask-bids-history
```


該接口提供現貨交易對的歷史訂單簿數據，包含指定價格範圍內的買盤和賣盤掛單總量。

***快取 / 更新頻率:*** 每 5 秒鐘更新一次

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
      "bids_usd": 81639959.9338,        // 多單總金額（美元）
      "bids_quantity": 1276.645,        // 多單總數量
      "asks_usd": 78533053.6862,        // 空單總金額（美元）
      "asks_quantity": 1217.125,        // 空單總數量
      "time": 1714003200000             // 時間戳（毫秒）
    },
    {
      "bids_usd": 62345879.8821,
      "bids_quantity": 980.473,
      "asks_usd": 65918423.4715,
      "asks_quantity": 1021.644,
      "time": 1714089600000
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
| range      | string  | NO  | 深度百分比（例如：0.25、0.5、0.75、1、2、3、5、10）。                          |

