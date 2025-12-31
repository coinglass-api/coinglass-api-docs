# 合約數據 - 資金費率 - 資金費率套利


```
GET /api/futures/funding-rate/arbitrage
```


該接口提供不同交易所間的合約幣種資金費率套利數據。

***快取 / 更新頻率:*** 每20秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "SUPRA", // 幣種名稱

      "buy": { // 做多的交易所資訊（低資金費率）
        "exchange": "MEXC", // 交易所名稱
        "open_interest_usd": 848218.2833, // 平台未平倉合約金額（美元）
        "funding_rate_interval": 4, // 資金費率結算間隔（小時）
        "funding_rate": -0.994 // 當前資金費率（%）
      },

      "sell": { // 做空的交易所資訊（高資金費率）
        "exchange": "Gate.io", // 交易所名稱
        "open_interest_usd": 448263.5072, // 平台未平倉合約金額（美元）
        "funding_rate_interval": 4, // 資金費率結算間隔（小時）
        "funding_rate": 0.005 // 當前資金費率（%）
      },

      "apr": 2187.81, // 年化收益率（APR，%）
      "funding": 0.999, // 資金費率收益差（long 和 short 之間的資金費率差）
      "fee": 0.03, // 交易手續費率（雙邊總和）
      "spread": -0.09, // 跨平台價格差（%）
      "next_funding_time": 1745222400000 // 下一次資金費率結算時間（時間戳，毫秒）
    }
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填  | 描述                               |
| ------------- | ------- | --- | -------------------------------- |
| usd           | integer | YES | 套利投資本金（例如：10000）                 |
| exchange_list | string  | NO  | 篩選交易所名稱清單（例如「Binance,OKX,Bybit」） |

