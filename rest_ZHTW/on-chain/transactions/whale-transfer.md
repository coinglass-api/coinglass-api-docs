# 鏈上 -  鏈上轉帳 - 大額轉賬


```
GET /api/chain/v2/whale-transfer
```


該接口提供近半年內金額不低於 1000 萬美元 的大額鏈上轉賬，支援 Bitcoin、Ethereum、Tron、Ripple、Dogecoin、Litecoin、Polygon、Algorand、Bitcoin Cash 和 Solana 等主流區塊鏈。

***快取 / 更新頻率:*** 即時更新.

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0", // 狀態碼："0" 表示成功
  "data": [
    {
       "transaction_hash": "0x910ade7323eae57017c1894078ff1ce319fe908709ba185d81147588ceb06dcc",//轉賬哈希
      "amount_usd": "18403606.873493258", // 轉帳金額（美元）
      "asset_quantity": "10081.791421235566", // 轉帳數量
      "asset_symbol": "WETH", // 資產符號
      "from": "unknown wallet", // 發送方
      "to": "unknown wallet", // 接收方
      "blockchain_name": "ethereum", // 區塊鏈名稱
      "block_height": 22402402, // 區塊高度
      "block_timestamp": 1746265043 // 區塊時間
    },
    {
      "transaction_hash": "7b1fa0327a1e68fbcc397eee0a75ae8ced8c19c08d32f5cfd2ec5d3ba04e59fe", //轉賬哈希
      "amount_usd": "18413630.94247512", // 轉帳金額（美元）
      "asset_quantity": "10087.28276721801", // 轉帳數量
      "asset_symbol": "WETH", // 資產符號
      "from": "unknown wallet", // 發送方
      "to": "unknown wallet", // 接收方
      "blockchain_name": "ethereum", // 區塊鏈名稱
      "block_height": 22402402, // 區塊高度
      "block_timestamp": 1746265043 // 區塊時間
    }
    ....
  ]
}
```

 **Parameters:**
| 名称         | 类型     | 必填 | 描述                                         |
| ---------- | ------ | -- | ------------------------------------------ |
| symbol     | string | NO | 交易幣種（例如：BTC）。透過 support-coins API 取得支援的幣種。 |
| start_time | string | NO | 起始時間戳（單位：毫秒，例如：1641522717000）。             |
| end_time   | string | NO | 結束時間戳記（單位：毫秒，例如：1641522717000）。            |

