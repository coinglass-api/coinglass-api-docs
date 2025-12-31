# ETF - 以太坊 ETF - 以太坊 ETF 流入流出歷史


```
GET /api/etf/ethereum/flow-history
```


該接口提供以太坊交易所交易基金（ETF）的流入流出歷史數據。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json

{
  "code": "0",
  "data": [
    {
      "timestamp": 1721692800000,  //時間戳
      "flow_usd": 106600000,  // 資金流入/流出（USD）
      "price_usd": 3438.09,  // 當前價格
      "etf_flows": [      // ETF 流動性列表
        {
          "etf_ticker": "ETHA",   // ETF 代碼
          "flow_usd": 266500000    // 資金流動（USD）
        },
        {
          "etf_ticker": "FETH",  
          "flow_usd": 71300000
        },

      ]
    }
  ]
}

```

