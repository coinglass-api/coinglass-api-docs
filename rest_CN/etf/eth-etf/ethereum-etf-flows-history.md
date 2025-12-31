# ETF - 以太坊 ETF - 以太坊ETF流入流出历史


```
GET /api/etf/ethereum/flow-history
```


该接口提供以太坊交易所交易基金（ETF）的流入流出历史数据。

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "data": [
    {
      "timestamp": 1721692800000,  // 时间戳
      "flow_usd": 106600000,  // 资金流入/流出（USD）
      "price_usd": 3438.09,  // 当前价格
      "etf_flows": [     // ETF 流动性列表
        {
          "etf_ticker": "ETHA",   // ETF 代码
          "flow_usd": 266500000     // 资金流动（USD）
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

