# 合約數據 - 主動買賣 - 聚合累計成交量差值（CVD）


```
GET /api/futures/aggregated-cvd/history
```


該接口提供合約交易所幣種的歷史 CVD 資料，為該幣種多個交易對的聚合數據。

***快取 / 更新頻率:***  即時更新.

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
      "agg_taker_buy_vol": 461937243.0899,
      "agg_taker_sell_vol": 415687343.2719,
      "cum_vol_delta": 46249899.818
    },
    {
      "time": 1762257600,
      "agg_taker_buy_vol": 390296231.4588,
      "agg_taker_sell_vol": 469137635.9107,
      "cum_vol_delta": -32591504.6339
    },
    {
      "time": 1762261200,
      "agg_taker_buy_vol": 461378798.1884,
      "agg_taker_sell_vol": 450407935.7885,
      "cum_vol_delta": -21620642.234
    },
  ]
}
```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                                                                            |
| ------------- | ------- | --- | ----------------------------------------------------------------------------- |
| exchange_list | string  | YES | 以逗號分隔的交易所名稱（例如："Binance, OKX, Bybit"）。可透過 support-exchange-pair 接口獲取支持的交易所列表。 |
| symbol        | string  | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。                                    |
| interval      | string  | YES | 數據時間間隔。支持的取值包括：1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d、1w。                        |
| limit         | integer | NO  | 每次請求返回的數據筆數。預設值：1000，最大值：1000。                                                |
| start_time    | integer | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                                                |
| end_time      | integer | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                                                |
| unit          | string  | NO  | 返回數據的單位，可選值為 'usd' 或 'coin'。                                                  |

