# ETF - 以太坊 ETF - 以太坊ETF列表


```
GET /api/etf/ethereum/list
```


该接口提供以太坊交易所交易基金（ETF）的关键状态信息列表。

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
      "ticker": "ETHA",                                  // ETF 代码
      "name": "iShares Ethereum Trust ETF",              // ETF 名称
      "region": "us",                                    // 地区
      "market_status": "closed",                         // 市场状态
      "primary_exchange": "XNAS",                        // 主要交易所
      "cik_code": "0002000638",                          // CIK 代码
      "type": "Spot",                                    // 类型
      "market_cap": "544896000.00",                      // 市值
      "list_date": 1721692800000,                        // 上市日期
      "shares_outstanding": "28800000",                  // 已发行份额
      "aum": "",                                         // 管理资产总值
      "management_fee_percent": "0.25",                  // 管理费
      "last_trade_time": 1722988779939,                  // 最新交易时间
      "last_quote_time": 1722988799379,                  // 最新计价时间
      "volume_quantity": 5592645,                        // 交易量
      "volume_usd": 106447049.343,                       // 美元交易量
      "price": 18.92,                                    // 市场价格
      "price_change": 0.67,                              // 价格变化
      "price_change_percent": 3.67,                      // 价格变化百分比
      "asset_info": {
        "nav": 18.11,                                  // 净值
        "premium_discount": 0.77,                      // 溢价/折扣
        "holding_quantity": 237882.8821,                 // 持仓数量
        "change_percent_1d": 0,                        // 1天变化百分比
        "change_quantity_1d": 0,                         // 1天变化值
        "change_percent_7d": 56.69,                    // 7天变化百分比
        "change_quantity_7d": 86060.9115,                // 7天变化值
        "date": "2024-08-05"                           // 数据日期
      },
      "update_time": 1722995656637                       // 更新时间
    }
  ]
}

```

