# 合約數據 - Hyperliquid 倉位 - Hyperliquid 鯨魚提醒


```
GET /api/hyperliquid/whale-alert
```


該接口提供 Hyperliquid 平台上即時的鯨魚交易提醒，突出展示價值超過 100 萬美元的大額持倉變動。(最多可返回約 200 條最新數據)

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
      "user": "0x3fd4444154242720c0d0c61c74a240d90c127d33", // 用戶地址
      "symbol": "ETH",                                     // 幣種
      "position_size": 12700,                              // 倉位大小（正數為多，負數為空）
      "entry_price": 1611.62,                              // 開倉價格
      "liq_price": 527.2521,                               // 強平價格
      "position_value_usd": 21003260,                      // 倉位價值（美元）
      "position_action": 2,                                // 倉位操作類型（1: 開倉，2: 平倉）
      "create_time": 1745219517000                         // 開倉時間（時間戳，毫秒）
    },
    {
      "user": "0x1cadadf0e884ac5527ae596a4fc1017a4ffd4e2c",
      "symbol": "BTC",
      "position_size": 33.54032,
      "entry_price": 87486.2,
      "liq_price": 44836.8126,
      "position_value_usd": 2936421.4757,
      "position_action": 2,
      "create_time": 1745219477000
    }
  ]
}

```

