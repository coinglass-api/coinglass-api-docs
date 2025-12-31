# 現貨 - 交易市場 - 支持的交易所和交易對


```
GET /api/spot/supported-exchange-pairs
```


該接口允許你查詢 CoinGlass 上支援的所有現貨交易所及其對應的交易對。

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
  "data": {
    "Binance": [ // 交易所名稱
      {
        "instrument_id": "BTCUSD_USDT", // 現貨交易對
        "base_asset": "BTC", // 基礎幣種
        "quote_asset": "USDT" // 計價幣種
      },
      {
        "instrument_id": "ETHUSD_USDT",
        "base_asset": "ETH",
        "quote_asset": "USDT"
      },
      ....
    ],
    "Bitget": [
      {
        "instrument_id": "AAVE:USD",
        "base_asset": "AAVE",
        "quote_asset": "USD"
      },
      {
        "instrument_id": "ADAUSD",
        "base_asset": "ADA",
        "quote_asset": "USD"
      },
      ...
    ]
  }
}

```

