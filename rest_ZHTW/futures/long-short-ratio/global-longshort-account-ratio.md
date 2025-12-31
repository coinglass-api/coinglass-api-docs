# 合約數據 - 多空比 - 交易對多空比歷史


```
GET /api/futures/global-long-short-account-ratio/history
```


該接口提供交易所交易對的多空帳戶比歷史數據。

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
      "time": 1741604400000, // 時間戳（毫秒）
      "global_account_long_percent": 73.88, // 帳戶多單比例（%）
      "global_account_short_percent": 26.12, // 帳戶空單比例（%）
      "global_account_long_short_ratio": 2.83 // 帳戶多空比（多/空）
    },
    {
      "time": 1741608000000, // 時間戳（毫秒）
      "global_account_long_percent": 73.24, // 帳戶多單比例（%）
      "global_account_short_percent": 26.76, // 帳戶空單比例（%）
      "global_account_long_short_ratio": 2.74 // 帳戶多空比（多/空）
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

