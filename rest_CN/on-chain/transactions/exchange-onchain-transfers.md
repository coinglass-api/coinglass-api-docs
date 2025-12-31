# 链上 - 链上转账 - 交易所链上转账（ERC-20）


```
GET /api/exchange/chain/tx/list
```


该接口提供基于 ERC-20 协议的交易所链上转账数据。

***缓存/ 更新频率 :*** 实时更新.

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
      "transaction_hash": "0xb8d08182d2de176ac42dceba9ff82a7a5fe650c1e56285d6810daac9561ff9dc", // 交易哈希
      "asset_symbol": "USDT",                       // 资产符号
      "amount_usd": 9998.5,                         // 美元金额
      "asset_quantity": 9998.5,                     // 数量
      "exchange_name": "Coinbase",                 // 交易所名称
      "transfer_type": 1,                           // 转账类型：1: 转入, 2: 转出, 3: 内部转账
      "from_address": "0x16c6897438c4f0c7894862d884549e8564c4025f", // 转出地址
      "to_address": "0xa9d1e08c7793af67e9d92fe308d5697fb81d3e43",   // 转入地址
      "transaction_time": 1745224211                // 交易时间（时间戳，单位秒）
    },
    {
      "transaction_hash": "0x033c56cb05654f2c360235eff99c84f0eee9c6330fc7012930adfe0a88789c0f", // 交易哈希
      "asset_symbol": "MANA",                       // 资产符号
      "amount_usd": 6368.95196834,                  // 美元金额
      "asset_quantity": 20091.33113044,             // 数量
      "exchange_name": "Binance",                  // 交易所名称
      "transfer_type": 1,                           // 转账类型：1: 转入, 2: 转出, 3: 内部转账
      "from_address": "0x06fd4ba7973a0d39a91734bbc35bc2bcaa99e3b0", // 转出地址
      "to_address": "0x28c6c06298d514db089934071355e5743bf21d60",   // 转入地址
      "transaction_time": 1745224211                // 交易时间（时间戳，单位秒）
    }
  ]
}

```

 **Parameters:**
| 名称         | 类型      | 必填 | 描述                                   |
| ---------- | ------- | -- | ------------------------------------ |
| symbol     | string  | NO | 只支持传入在以太坊（ETH）网络上支持的 ERC-20 协议代币的符号。 |
| start_time | integer | NO | 开始时间戳（毫秒）（例如：1641522717000）。         |
| min_usd    | number  | NO | 最小转账金额筛选，单位为美元（USD）。                 |
| per_page   | integer | NO | 每页返回的结果数量。                           |
| page       | integer | NO | 分页的页码，默认值为 1。                        |

