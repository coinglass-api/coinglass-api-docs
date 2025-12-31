# 合约 - 交易市场 - 支持的交易所和交易对


```
GET /api/futures/supported-exchange-pairs
```


该接口允许你查询 CoinGlass 上支持的所有合约交易所及其对应的交易对。

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

 **Parameters:**
| 名称       | 类型     | 必填 | 描述                 |
| -------- | ------ | -- | ------------------ |
| exchange | string | NO | 筛选结果，仅返回指定交易所的交易对。 |

