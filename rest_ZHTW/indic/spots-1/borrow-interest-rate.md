# 指標 - 現貨 - 借貸利率


```
GET /api/borrow-interest-rate/history
```


該接口提供加密貨幣的借貸利率數據。

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
      "time": 1741636800,                  // 時間戳 (秒)
      "interest_rate": 0.002989            // 利率
    },
    {
      "time": 1741640400,                  // 時間戳 (秒)
      "interest_rate": 0.002989            // 利率
    }
  ]
}

```

 **Parameters:**
| 名称         | 类型      | 必填  | 描述                                                           |
| ---------- | ------- | --- | ------------------------------------------------------------ |
| exchange   | string  | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |
| symbol     | string  | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。                   |
| interval   | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。       |
| limit      | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                               |
| start_time | integer | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                               |
| end_time   | integer | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                               |

