# 指標 - 合約指標 - 合約基差


```
GET /api/futures/basis/history
```


該接口提供合約基差的歷史數據，包括開盤與收盤時的基差數值。

***快取 / 更新頻率:*** 即時更新.\\

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1741629600000,            // 時間戳（毫秒）
      "open_basis": 0.0504,             // 開盤基差（單位：%）
      "close_basis": 0.0445,            // 收盤基差（單位：%）
      "open_change": 39.5,              // 開盤時基差相較前一時段變化幅度（單位：%）
      "close_change": 34.56             // 收盤時基差相較前一時段變化幅度（單位：%）
    },
    {
      "time": 1741633200000,            // 時間戳（毫秒）
      "open_basis": 0.0446,             // 開盤基差（單位：%）
      "close_basis": 0.03,              // 收盤基差（單位：%）
      "open_change": 34.65,             // 開盤時基差變化幅度（單位：%）
      "close_change": 23.74             // 收盤時基差變化幅度（單位：%）
    }
  ]
}

```

 **Parameters:**
| 名称         | 类型     | 必填  | 描述                                                           |
| ---------- | ------ | --- | ------------------------------------------------------------ |
| exchange   | string | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |
| symbol     | string | YES | 交易對（例如：BTCUSDT）。可透過 support-exchange-pair 接口查詢支持的交易對。        |
| interval   | string | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。       |
| limit      | string | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                               |
| start_time | string | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                               |
| end_time   | string | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                               |

