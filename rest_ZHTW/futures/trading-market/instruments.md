# 合約數據 - 交易市場 - 支持的交易所和交易對


```
GET /api/futures/supported-exchange-pairs
```


該接口允許你查詢 CoinGlass 上支持的所有合約交易所及其對應的交易對

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
        "instrument_id": "BTCUSD_PERP",// 合約交易對
        "base_asset": "BTC",// 基礎幣種
        "quote_asset": "USD"// 計價幣種
      },
      {
        "instrument_id": "BTCUSD_250627",
        "base_asset": "BTC",
        "quote_asset": "USD"
      },
      ....
      ],
    "Bitget": [
      {
        "instrument_id": "BTCUSDT_UMCBL",
        "base_asset": "BTC",
        "quote_asset": "USDT"
      },
      {
        "instrument_id": "ETHUSDT_UMCBL",
        "base_asset": "ETH",
        "quote_asset": "USDT"
      },
      ...
      ]
      ...
   }
}

```

 **Parameters:**
| 名称       | 类型     | 必填 | 描述                 |
| -------- | ------ | -- | ------------------ |
| exchange | string | NO | 篩選結果，僅傳回指定交易所的交易對。 |

