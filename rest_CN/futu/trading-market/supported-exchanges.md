# 合约 - 交易市场 - 支持的交易所


```
GET /api/futures/supported-exchanges
```


该接口用于查询 CoinGlass 支持的所有合约交易所。

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

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

