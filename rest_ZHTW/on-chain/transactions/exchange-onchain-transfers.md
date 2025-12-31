# 鏈上 -  鏈上轉帳 - 交易所鏈上轉帳（ERC-20）


```
GET /api/exchange/chain/tx/list
```


該接口提供基於 ERC-20 協議的交易所鏈上轉帳數據。

***快取 / 更新頻率:*** 即時更新.

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
      "transaction_hash": "0xb8d08182d2de176ac42dceba9ff82a7a5fe650c1e56285d6810daac9561ff9dc", // 交易哈希
      "asset_symbol": "USDT",                       // 資產符號
      "amount_usd": 9998.5,                         // 美元金額
      "asset_quantity": 9998.5,                     // 數量
      "exchange_name": "Coinbase",                 // 交易所名稱
      "transfer_type": 1,                           // 轉賬類型：1: 轉入, 2: 轉出, 3: 內部轉賬
      "from_address": "0x16c6897438c4f0c7894862d884549e8564c4025f", // 轉出地址
      "to_address": "0xa9d1e08c7793af67e9d92fe308d5697fb81d3e43",   // 轉入地址
      "transaction_time": 1745224211                // 交易時間（時間戳，單位秒）
    },
    {
      "transaction_hash": "0x033c56cb05654f2c360235eff99c84f0eee9c6330fc7012930adfe0a88789c0f", // 交易哈希
      "asset_symbol": "MANA",                       // 資產符號
      "amount_usd": 6368.95196834,                  // 美元金額
      "asset_quantity": 20091.33113044,             // 數量
      "exchange_name": "Binance",                  // 交易所名稱
      "transfer_type": 1,                           // 轉賬類型：1: 轉入, 2: 轉出, 3: 內部轉賬
      "from_address": "0x06fd4ba7973a0d39a91734bbc35bc2bcaa99e3b0", // 轉出地址
      "to_address": "0x28c6c06298d514db089934071355e5743bf21d60",   // 轉入地址
      "transaction_time": 1745224211                // 交易時間（時間戳，單位秒）
    }
  ]
}

```

 **Parameters:**
| 名称         | 类型      | 必填 | 描述                              |
| ---------- | ------- | -- | ------------------------------- |
| symbol     | string  | NO | 轉帳幣種（例如：ETH）。                   |
| start_time | integer | NO | 起始時間戳，單位為毫秒（例如：1746776387000）。  |
| min_usd    | number  | NO | 最小轉帳金額篩選，單位為美元（USD）。            |
| per_page   | integer | NO | 每頁返回的結果數量。                      |
| page       | integer | NO | 分頁的頁碼，默認值為 1。                   |

