# 链上 - 链上转账 - 大额转账


```
GET /api/chain/v2/whale-transfer
```


该接口提供近半年内金额不低于 1000 万美元 的大额链上转账，支持 Bitcoin、Ethereum、Tron、Ripple、Dogecoin、Litecoin、Polygon、Algorand、Bitcoin Cash 和 Solana 等主流区块链。

***缓存 / 更新频率:*** 实时.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0", // 状态码："0" 表示成功
  "data": [
    {
       "transaction_hash":    "0x910ade7323eae57017c1894078ff1ce319fe908709ba185d81147588ceb06dcc",//转账哈希
      "amount_usd": "18403606.873493258", // 转账金额（美元）
      "asset_quantity": "10081.791421235566", // 转账数量
      "asset_symbol": "WETH", // 资产符号
      "from": "unknown wallet", // 发送方
      "to": "unknown wallet", // 接收方
      "blockchain_name": "ethereum", // 区块链名称
      "block_height": 22402402, // 区块高度
      "block_timestamp": 1746265043 // 区块时间
    },
    {
      "transaction_hash": "7b1fa0327a1e68fbcc397eee0a75ae8ced8c19c08d32f5cfd2ec5d3ba04e59fe",//转账哈希
      "amount_usd": "18413630.94247512", // 转账金额（美元）
      "asset_quantity": "10087.28276721801", // 转账数量
      "asset_symbol": "WETH", // 资产符号
      "from": "unknown wallet", // 发送方
      "to": "unknown wallet", // 接收方
      "blockchain_name": "ethereum", // 区块链名称
      "block_height": 22402402, // 区块高度
      "block_timestamp": 1746265043 // 区块时间
    }
    ....
  ]
}
```

 **Parameters:**
| 名称         | 类型     | 必填 | 描述                                         |
| ---------- | ------ | -- | ------------------------------------------ |
| symbol     | string | NO | 交易币种（例如：BTC）。通过 support-coins API 获取支持的币种。 |
| start_time | string | NO | 起始时间戳（单位：毫秒，例如：1641522717000）。             |
| end_time   | string | NO | 结束时间戳（单位：毫秒，例如：1641522717000）。             |

