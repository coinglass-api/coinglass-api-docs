# 合約數據 - 交易市場 - 支持的交易所


```
GET /api/futures/supported-exchanges
```


該接口允許你查詢 CoinGlass 上支持的所有合約交易所

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    "OKX",
    "Binance",
    "HTX",
    "Bitmex",
    "Bitfinex",
    "Bybit",
    "Deribit",
    "Gate",
    "Kraken",
    "KuCoin",
    "CME",
    "Bitget",
    "dYdX",
    "CoinEx",
    "BingX",
    "Coinbase",
    "Gemini",
    "Crypto.com",
    "Hyperliquid",
    "Bitunix",
    "MEXC",
    "WhiteBIT",
    "Aster",
    "Lighter",
    "EdgeX",
    "Drift",
    "Paradex",
    "Extended",
    "ApeX Omni"
  ]
}
```

