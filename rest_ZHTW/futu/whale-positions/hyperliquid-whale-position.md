# 合約數據 - Hyperliquid 倉位 - Hyperliquid 鯨魚持倉


```
GET /api/hyperliquid/whale-position
```


該接口提供 Hyperliquid 平台上鯨魚的持倉數據，篩選出價值超過 100 萬美元的持倉數據。

***快取 / 更新頻率:*** 即時更新.

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
      "user": "0x20c2d95a3dfdca9e9ad12794d5fa6fad99da44f5", // 用戶地址
      "symbol": "ETH",                                   // 幣種
      "position_size": -44727.1273,                      // 倉位大小（正為做多，負為做空）
      "entry_price": 2249.7,                             // 開倉價格
      "mark_price": 1645.8,                              // 當前標記價格
      "liq_price": 2358.2766,                            // 強平價格
      "leverage": 25,                                    // 杠杆倍數
      "margin_balance": 2943581.7019,                    // 保證金餘額（USD）
      "position_value_usd": 73589542.5467,               // 倉位價值（USD）
      "unrealized_pnl": 27033236.424,                    // 未實現盈虧（USD）
      "funding_fee": -3107520.7373,                      // 資金費用（USD）
      "margin_mode": "cross",                            // 保證金模式（cross 表示全倉）
      "create_time": 1741680802000,                      // 開倉時間（時間戳，毫秒）
      "update_time": 1745219966000                       // 更新時間（時間戳，毫秒）
    },
    {
      "user": "0xf967239debef10dbc78e9bbbb2d8a16b72a614eb",
      "symbol": "BTC",
      "position_size": -800,
      "entry_price": 84931.3,
      "mark_price": 87427,
      "liq_price": 92263.798,
      "leverage": 15,
      "margin_balance": 4812076.3896,
      "position_value_usd": 69921600,
      "unrealized_pnl": -1976493.6819,
      "funding_fee": 14390.0346,
      "margin_mode": "isolated",                         // 保證金模式（isolated 表示逐倉）
      "create_time": 1743982804000,
      "update_time": 1745219969000
    }
  ]
}

```

