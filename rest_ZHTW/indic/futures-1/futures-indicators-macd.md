# 指標 - 合約指標 - 移動平均收斂發散指標（MACD）


```
GET /api/futures/indicators/macd
```


該接口用於獲取交易對的移動平均收斂發散指標（MACD）。

***快取 / 更新頻率:*** 实时更新

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    {
      "time": 1678665600000,
      "macd_value": -837.307
    },
    {
      "time": 1678752000000,
      "macd_value": -575.43
    },
    ....
  ]
}
```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                            |
| ------------- | ------- | --- | ------------------------------------------------------------- |
| exchange      | string  | YES | 合約交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。 |
| symbol        | string  | YES | 交易對（例如：BTCUSDT）。可透過 support-exchange-pair 接口查詢支持的交易對。         |
| interval      | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。        |
| limit         | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                                |
| start_time    | integer | NO  | 起始時間戳，單位為毫秒（例如：1641522717000）。                                |
| end_time      | integer | NO  | 結束時間戳，單位為毫秒（例如：1641522717000）。                                |
| series_type   | string  | NO  | 價格類型 —— 指定計算中使用的價格類型。支援的取值：open、high、low、close。預設值：close。     |
| fast_window   | integer | NO  | 用於指標計算的快速週期窗口大小（例如：MACD 的快速週期為 12）。                           |
| slow_window   | integer | NO  | 用於指標計算的慢速週期窗口大小（例如：MACD 的慢速週期為 26）。                           |
| signal_window | integer | NO  | 用於平滑快慢線差值的訊號線窗口大小（例如：MACD 的訊號線週期為 9）。                         |

