# 期權 - 期權最大痛點


```
GET /api/option/max-pain
```


該接口提供期權的最大痛點相關數據。

***快取 / 更新頻率:*** 每 1 分鐘更新一次

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
      "date": "250422",                                   // 日期（YYMMDD 格式）
      "call_open_interest_market_value": 1616749.22,      // 看漲期權市場價值（美元）
      "put_open_interest": 512.5,                         // 看跌期權未平倉合約數量（張）
      "put_open_interest_market_value": 49687.62,         // 看跌期權市場價值（美元）
      "max_pain_price": "84000",                          // 最大痛苦點價格
      "call_open_interest": 953.7,                        // 看漲期權未平倉合約數量（張）
      "call_open_interest_notional": 83519113.56,         // 看漲期權名義價值（美元）
      "put_open_interest_notional": 44881569.13           // 看跌期權名義價值（美元）
    },
    {
      "date": "250423",                                 
      "call_open_interest_market_value": 2274700.52,     // 看漲期權市場價值（美元）
      "put_open_interest": 1204.3,                       // 看跌期權未平倉合約數量（張）
      "put_open_interest_market_value": 374536.01,       // 看跌期權市場價值（美元）
      "max_pain_price": "85000",                         // 最大痛苦點價格
      "call_open_interest": 1302.2,                      // 看漲期權未平倉合約數量（張）
      "call_open_interest_notional": 114040373.53,       // 看漲期權名義價值（美元）
      "put_open_interest_notional": 105465691.73          // 看跌期權名義價值（美元）
    }
  ]
}

```

 **Parameters:**
| 名称       | 类型     | 必填  | 描述                             |
| -------- | ------ | --- | ------------------------------ |
| symbol   | string | YES | 交易幣種（例如：BTC、ETH）               |
| exchange | string | YES | 交易所名稱（例如：Deribit、Binance、OKX）。 |

