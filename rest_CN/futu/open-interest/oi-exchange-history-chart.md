# 合约 - 持仓 - 币种交易所持仓历史


```
GET /api/futures/open-interest/exchange-history-chart
```


该接口用于获取某一加密货币在多个交易所的历史持仓量数据，适用于图表展示。

***缓存 / 更新频率:*** 10秒钟更新一次

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版    | 创业版      | 标准版 | 专业版 | 企业版 |
| :----- | :----- | :------- | :-- | :-- | :-- |
| 可用性    | ✅      | ✅        | ✅   | ✅   | ✅   |
| 颗粒度    | `>=4h` | ​`>=30m` | 无限制 | 无限制 | 无限制 |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "time_list": [1721649600000, ...], // 时间戳列表（毫秒）
    "price_list": [67490.3, ...], // 价格列表（与 time_list 对应）

    "data_map": { // 各交易所未平仓合约数据
      "Binance": [8018229234, ...], // Binance 未平仓合约（与 time_list 对应）
      "Bitmex": [395160842, ...] // BitMEX 未平仓合约（与 time_list 对应）
      // ...
    }
  }
}
```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                          |
| ------ | ------ | --- | ------------------------------------------- |
| symbol | string | YES | 交易币种（例如：BTC）。可通过 support-coins 接口获取支持的币种列表。 |
| range  | string | YES | 数据时间范围（例如：all，1m，15m，1h，4h，12h）             |
| unit   | string | NO  | 返回数据的单位，可以选择 'usd' 或 'coin'。                |

