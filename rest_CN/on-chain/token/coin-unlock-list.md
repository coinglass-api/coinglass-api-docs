# 链上 - 代币 - 代币解锁列表


```
GET /api/coin/unlock-list
```


该接口返回代币解锁数据以及即将到来的解锁计划。

***缓存 / 更新频率:*** 实时更新

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0", // 返回状态码
  "data": [ // 代币列表
    {
      "symbol": "GT", // 代币符号
      "name": "GateToken", // 代币名称
      "symbol_logo_url": "https://cdn.coinglasscdn.com/static/img/coins/gt.jpg", // 图标链接
      "price": 10.377, // 最新价格
      "price_change_percent_24h": 2.67, // 24小时涨跌幅
      "market_cap": 1217683606.698, // 市值
      "total_supply": 300000000, // 总供应量
      "fully_diluted_valuation": 3115642754.097, // 全稀释估值
      "total_locked": 74868300, // 锁仓数量
      "circulating_supply": 117344474, // 流通供应量
      "total_unlocked": 162691500, // 已解锁数量
      "next_unlock_date": 1765152000000, // 下次解锁时间
      "next_unlock_tokens": 48600, // 下次解锁数量
      "next_unlock_of_circulating": 0.041416522093745974, // 占流通量比例
      "next_unlock_of_supply": 0.0162 // 占总供应量比例
    },
    ....
  ]
}

```

 **Parameters:**
| 名称       | 类型      | 必填 | 描述     |
| -------- | ------- | -- | ------ |
| per_page | integer | NO | 每页返回数量 |
| page     | integer | NO | 页码     |

