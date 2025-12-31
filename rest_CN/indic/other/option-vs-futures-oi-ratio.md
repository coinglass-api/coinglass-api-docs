# 指标 - 其他指标 - 期权持仓 vs 合约持仓


```
GET /api/futures/delisted-exchange-pairs
```


该接口提供期权持仓 vs 合约持仓数据

***缓存 / 更新频率:*** 1天更新一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "data": {
    "Binance": [
      {
        "instrument_id": "1000LUNCBUSD",
        "base_asset": "1000LUNC",
        "quote_asset": "BUSD"
      },
      {
        "instrument_id": "1000SHIBBUSD",
        "base_asset": "1000SHIB",
        "quote_asset": "BUSD"
      },
      {
        "instrument_id": "ADABUSD",
        "base_asset": "ADA",
        "quote_asset": "BUSD"
      },
}

```

