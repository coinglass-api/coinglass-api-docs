# ETF - 以太坊 ETF - 以太坊 ETF 淨資產歷史


```
GET /api/etf/ethereum/net-assets/history
```


該接口提供以太坊為基礎的交易所交易基金（ETF）的歷史淨資產數據。

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
      "net_assets_usd": 51671409241.39,         // 淨資產總額（USD）
      "change_usd": 655300000,                  // 當日資金變化（USD）
      "timestamp": 1704931200000,               // 日期（時間戳，單位毫秒）
      "price_usd": 1637.8                      // 當日ETH價格（USD）
    },
    {
      "net_assets_usd": 51874409241.39,         // 淨資產總額（USD）
      "change_usd": 203000000,                  // 當日資金變化（USD）
      "timestamp": 1705017600000,               // 日期（時間戳，單位毫秒）
      "price_usd": 1637.8                      // 當日ETH價格（USD）
    }
  ]
}

```

