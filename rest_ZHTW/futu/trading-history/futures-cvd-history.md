# 合約數據 - 主動買賣 - 累計成交量差值（CVD）


```
GET /api/futures/cvd/history
```


該接口提供合約交易所交易對的歷史累計成交量差值（CVD）資料，包含隨時間變化的主動買入量（taker buy）與主動賣出量（taker sell）。

***快取 / 更新頻率:*** 即時更新.

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
      "time": 1762254000000,
      "taker_buy_vol": 350281007.0211,
      "taker_sell_vol": 325339470.9493,
      "cum_vol_delta": 24941536.0718
    },
    {
      "time": 1762257600,
      "taker_buy_vol": 286399814.1275,
      "taker_sell_vol": 347409544.4937,
      "cum_vol_delta": -36068194.2944
    },
    {
      "time": 1762261200,
      "taker_buy_vol": 299952362.4807,
      "taker_sell_vol": 323978642.5934,
      "cum_vol_delta": -60094474.4071
    },
  ]
}
```

 **Parameters:**
| 名称         | 类型      | 必填  | 描述                                                            |
| ---------- | ------- | --- | ------------------------------------------------------------- |
| exchange   | string  | YES | 合約交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。 |
| symbol     | string  | YES | 交易對（例如：BTCUSDT）。可透過 support-exchange-pair 接口查詢支持的交易對。         |
| interval   | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。        |
| limit      | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：1000。                                |
| start_time | string  | NO  | 起始時間戳，單位為毫秒（例如：1641522717000）。                                |
| end_time   | string  | NO  | 結束時間戳，單位為毫秒（例如：1641522717000）。                                |

