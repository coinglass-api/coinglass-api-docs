# 期权 - 期权最大痛点


```
GET /api/option/max-pain
```


该接口提供期权的最大痛点相关数据。

***缓存/ 更新频率 :*** 1分钟一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "date": "250422",                                   // 日期（YYMMDD 格式）
      "call_open_interest_market_value": 1616749.22,      // 看涨期权市场价值（美元）
      "put_open_interest": 512.5,                         // 看跌期权未平仓合约数量（张）
      "put_open_interest_market_value": 49687.62,         // 看跌期权市场价值（美元）
      "max_pain_price": "84000",                          // 最大痛苦点价格
      "call_open_interest": 953.7,                        // 看涨期权未平仓合约数量（张）
      "call_open_interest_notional": 83519113.56,         // 看涨期权名义价值（美元）
      "put_open_interest_notional": 44881569.13           // 看跌期权名义价值（美元）
    },
    {
      "date": "250423",                                 
      "call_open_interest_market_value": 2274700.52,     ）
      "put_open_interest": 1204.3,                       
      "put_open_interest_market_value": 374536.01,       
      "max_pain_price": "85000",                         
      "call_open_interest": 1302.2,                      
      "call_open_interest_notional": 114040373.53,       
      "put_open_interest_notional": 105465691.73          
    }
  ]
}

```

 **Parameters:**
| 名称       | 类型     | 必填  | 描述                             |
| -------- | ------ | --- | ------------------------------ |
| symbol   | string | YES | 交易币种（例如：BTC、ETH）               |
| exchange | string | YES | 交易所名称（例如：Deribit、Binance、OKX）。 |

