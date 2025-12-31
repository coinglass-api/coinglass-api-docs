# 合約數據 - Hyperliquid 倉位 - Hyperliquid 倉位


```
GET /api/hyperliquid/position
```


該接口提供 Hyperliquid 上的倉位數據，包括每個賬戶的用戶地址、倉位大小、保證金餘額和未實現盈虧。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",                     // 狀態碼（0 表示成功）
  "data": {
    "total_pages": 10,          // 倉位數據的總頁數
    "current_page": 1,            // 當前返回的頁碼
    "list": [
      {
        "user": "0x5b5d51203a0f9079f8aeb098a6523a13f298c060",     // 用戶錢包地址
        "symbol": "BTC",           // 交易對（幣種）
        "position_size": -2683.14, // 倉位大小（正數為做多，負數為做空）
        "entry_price": 111459.6,   // 開倉價格
        "mark_price": 116638,      // 當前標記價格
        "liq_price": 150629.52,    // 強平價格
        "leverage": 10,            // 槓桿倍數
        "margin_balance": 31263482.07,        // 保證金餘額（美元）
        "position_value_usd": 312634820.77,   // 倉位價值（美元）
        "unrealized_pnl": -13572345.06,       // 未實現盈虧（美元）
        "funding_fee": -12534553.66,          // 資金費用（美元）
        "margin_mode": "cross",               // 保證金模式（"cross" 表示全倉，"isolated" 表示逐倉）
        "create_time": 1752152867098,         // 開倉時間（時間戳，毫秒）
        "update_time": 1758162698266          // 更新時間（時間戳，毫秒）
      }
    ]
  }
}
```

 **Parameters:**
| 名称           | 类型     | 必填  | 描述                                           |
| ------------ | ------ | --- | -------------------------------------------- |
| symbol       | string | YES | 交易幣種（例如：BTC）。透過 supported-coins API 獲取支援的幣種。 |
| current_page | string | NO  | 返回當前頁碼                                       |

