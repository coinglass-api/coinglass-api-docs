# 合约 - 交易市场 - 下架的交易所和交易对


```
GET /api/futures/delisted-exchange-pairs
```


此接口查询已下线的合约交易所和交易对。

***缓存 / 更新频率:*** 每30分钟更新一次

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
        "instrument_id": "BTCUSD_PERP",// 合约交易对
        "base_asset": "BTC",// 基础币种
        "quote_asset": "USD"// 计价币种
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

