# 合约 - 交易市场 - 币种市场列表


```
GET /api/futures/coins-markets
```


该接口提供合约币种的相关指标信息。

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",  
  "msg": "success",  
  "data": [
    {
      "symbol": "BTC",  // 币种符号
      "current_price": 84773.6,  // 当前价格（单位：USD）
      "avg_funding_rate_by_oi": 0.00196,  // 按持仓量加权的平均资金费率
      "avg_funding_rate_by_vol": 0.002647,  // 按成交量加权的平均资金费率
      "market_cap_usd": 1683310500117.051,  // 市值（单位：USD）
      "open_interest_market_cap_ratio": 0.0327,  // 未平仓量与市值的比值
      "open_interest_usd": 55002072334.9376,  // 未平仓量（单位：USD）
      "open_interest_quantity": 648525.0328,  // 未平仓合约数量
      "open_interest_volume_ratio": 0.7936,  // 未平仓量与成交量的比值
      "price_change_percent_5m": -0.02,  // 价格5分钟变化百分比
      "price_change_percent_15m": 0.06,  // 价格15分钟变化百分比
      "price_change_percent_30m": 0.03,  // 价格30分钟变化百分比
      "price_change_percent_1h": -0.1,  // 价格1小时变化百分比
      "price_change_percent_4h": -0.15,  // 价格4小时变化百分比
      "price_change_percent_12h": 0.15,  // 价格12小时变化百分比
      "price_change_percent_24h": 1.06,  // 价格24小时变化百分比
      "open_interest_change_percent_5m": 0,  // 未平仓量5分钟变化百分比
      "open_interest_change_percent_15m": 0.04,  // 未平仓量15分钟变化百分比
      "open_interest_change_percent_30m": 0,  // 未平仓量30分钟变化百分比
      "open_interest_change_percent_1h": -0.01,  // 未平仓量1小时变化百分比
      "open_interest_change_percent_4h": 0.17,  // 未平仓量4小时变化百分比
      "open_interest_change_percent_24h": 4.58,  // 未平仓量24小时变化百分比
      "volume_change_percent_5m": -0.03,  // 成交量5分钟变化百分比
      "volume_change_percent_15m": -0.73,  // 成交量15分钟变化百分比
      "volume_change_percent_30m": -1.13,  // 成交量30分钟变化百分比
      "volume_change_percent_1h": -2.33,  // 成交量1小时变化百分比
      "volume_change_percent_4h": -5.83,  // 成交量4小时变化百分比
      "volume_change_percent_24h": -26.38,  // 成交量24小时变化百分比
      "volume_change_usd_1h": 69310404660.3795,  // 成交量1小时变化（单位：USD）
      "volume_change_usd_4h": -4290959532.4414644,  // 成交量4小时变化（单位：USD）
      "volume_change_usd_24h": -24835757605.82467,  // 成交量24小时变化（单位：USD）
      "long_short_ratio_5m": 1.2523,  // 多空比（近5分钟）
      "long_short_ratio_15m": 0.9928,  // 多空比（近15分钟）
      "long_short_ratio_30m": 1.0695,  // 多空比（近30分钟）
      "long_short_ratio_1h": 1.0068,  // 多空比（近1小时）
      "long_short_ratio_4h": 1.0504,  // 多空比（近4小时）
      "long_short_ratio_12h": 1.0317,  // 多空比（近12小时）
      "long_short_ratio_24h": 1.0313,  // 多空比（近24小时）
      "liquidation_usd_1h": 33621.85192,  // 总爆仓金额（近1小时，单位：USD）
      "long_liquidation_usd_1h": 22178.4681,  // 多头爆仓金额（近1小时，单位：USD）
      "short_liquidation_usd_1h": 11443.38382,  // 空头爆仓金额（近1小时，单位：USD）
      "liquidation_usd_4h": 222210.47117,  // 总爆仓金额（近4小时，单位：USD）
      "long_liquidation_usd_4h": 179415.77249,  // 多头爆仓金额（近4小时，单位：USD）
      "short_liquidation_usd_4h": 42794.69868,  // 空头爆仓金额（近4小时，单位：USD）
      "liquidation_usd_12h": 11895453.392145,  // 总爆仓金额（近12小时，单位：USD）
      "long_liquidation_usd_12h": 10223351.23772,  // 多头爆仓金额（近12小时，单位：USD）
      "short_liquidation_usd_12h": 1672102.154425,  // 空头爆仓金额（近12小时，单位：USD）
      "liquidation_usd_24h": 27519292.973646,  // 总爆仓金额（近24小时，单位：USD）
      "long_liquidation_usd_24h": 17793322.595016,  // 多头爆仓金额（近24小时，单位：USD）
      "short_liquidation_usd_24h": 9725970.37863  // 空头爆仓金额（近24小时，单位：USD）
    },
    {
      "symbol": "ETH",  // 币种符号
      "current_price": 1582.55,  // 当前价格（单位：USD）
      "avg_funding_rate_by_oi": 0.001631,  // 持仓量加权平均资金费率
      "avg_funding_rate_by_vol": -0.000601,  // 成交量加权平均资金费率
      "market_cap_usd": 190821695398.62064,  // 市值（单位：USD）
      "open_interest_market_cap_ratio": 0.0925,  // 未平仓量与市值比值
      "open_interest_usd": 17657693967.0459,  // 未平仓量（单位：USD）
      "open_interest_quantity": 11160428.5065,  // 未平仓合约数量
      "open_interest_volume_ratio": 0.5398,  // 未平仓量与成交量比值
      "price_change_percent_5m": 0.07,  // 价格5分钟变化百分比
      "price_change_percent_15m": 0.25,  // 价格15分钟变化百分比
      "price_change_percent_30m": 0.07,  // 价格30分钟变化百分比
      "price_change_percent_1h": -0.11,  // 价格1小时变化百分比
      "price_change_percent_4h": -0.05,  // 价格4小时变化百分比
      "price_change_percent_12h": -0.02,  // 价格12小时变化百分比
      "price_change_percent_24h": 0.16  // 价格24小时变化百分比
      // ...后续字段依此类推
    }
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填 | 描述                                                                            |
| ------------- | ------- | -- | ----------------------------------------------------------------------------- |
| exchange_list | string  | NO | 以逗号分隔的交易所名称（例如："binance, okx, bybit"）。可通过 `support-exchange-pair` 接口获取支持的交易所。 |
| per_page      | integer | NO | 每页返回的结果数量。                                                                    |
| page          | integer | NO | 分页的页码，默认值为 1。                                                                 |

