# ETF - 比特幣 ETF - ETF 價格歷史


```
GET /api/etf/bitcoin/price/history
```


該接口提供比特幣 ETF 的歷史價格數據，包括每個數據點的開盤價、最高價、最低價、收盤價（OHLC）以及交易量數據。

***快取 / 更新頻率:*** 每 1天更新一次

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
      "time": 1731056460000,     // 時間戳（毫秒）
      "open": 60.47,              // 開盤價
      "high": 60.47,              // 最高價
      "low": 60.47,               // 最低價
      "close": 60.47,             // 收盤價
      "volume": 100               // 成交量
    },
    ...
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                        |
| ------ | ------ | --- | ------------------------- |
| ticker | string | YES | ETF 代碼（例如：GBTC、IBIT）。     |
| range  | string | YES | 數據時間間隔。支持的取值包括： 1d,7d,all |

