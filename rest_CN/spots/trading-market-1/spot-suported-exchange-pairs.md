# 现货 - 交易市场 - 支持的交易所和交易对


```
GET /api/spot/supported-exchange-pairs
```


该接口允许你查询 CoinGlass 上支持的所有现货交易所及其对应的交易对。

***缓存 / 更新频率:*** 每 1 分钟更新一次

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "Binance": [ // 交易所名称
      {
        "instrument_id": "BTCUSD_USDT",// 现货交易对
        "base_asset": "BTC",// 基础币种
        "quote_asset": "USDT"// 计价币种
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
      ...
   }
}
```

