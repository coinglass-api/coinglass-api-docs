# 指標 - 合約指標 - 鯨魚指數


```
GET /api/futures/whale-index/history
```


此端點提供鯨魚指數的歷史數據。

***快取 / 更新頻率:*** 即時更新

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    {
      "time": 1665532800000,
      "whale_index_value": -184.8
    },
    {
      "time": 1665619200000,
      "whale_index_value": -118.965
    },
    {
      "time": 1665705600000,
      "whale_index_value": -58.795
    },
    {
      "time": 1665792000000,
      "whale_index_value": -84.095
    },
}
```

 **Parameters:**
| 名称         | 类型     | 必填  | 描述                                                            |
| ---------- | ------ | --- | ------------------------------------------------------------- |
| exchange   | string | YES | 合約交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。 |
| symbol     | string | YES | 交易對（例如：BTCUSDT）。可透過 support-exchange-pair 接口查詢支持的交易對          |
| interval   | string | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。        |
| limit      | string | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：4500。                                |
| start_time | string | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）                                 |
| end_time   | string | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                                |

