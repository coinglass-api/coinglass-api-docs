# ETF - 比特币 ETF - ETF价格历史


```
GET /api/etf/bitcoin/price/history
```


该接口提供比特币ETF的历史价格数据，包括每个数据点的开盘价、最高价、最低价、收盘价（OHLC）以及交易量信息。

***缓存/ 更新频率 :*** 1天一次.

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
      "time": 1731056460000,     // 时间戳（毫秒）
      "open": 60.47,                  // 开盘价
      "high": 60.47,                  // 最高价
      "low": 60.47,                   // 最低价
      "close": 60.47,                 // 收盘价
      "volume": 100                   // 成交量
    },
    ...
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                          |
| ------ | ------ | --- | --------------------------- |
| ticker | string | YES | ETF 股票代码 (例如., GBTC, IBIT). |
| range  | string | YES | 数据的时间范围（ (例如, 1d,7d,all).   |

