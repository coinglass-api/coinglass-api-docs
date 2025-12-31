# 合约 - 交易市场 - 交易对市场列表


```
GET /api/futures/pairs-markets
```


该接口提供合约交易对的相关指标信息。

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
      "instrument_id": "BTCUSDT", // 合约交易对
      "exchange_name": "Binance", // 交易所名称
      "symbol": "BTC/USDT", // 币种对

      "current_price": 84604.3, // 当前价格
      "index_price": 84646.66222222, // 指数价格
      "price_change_percent_24h": 0.67, // 24小时价格变化(%)

      "volume_usd": 11317580109.5041, // 24小时交易量(USD)
      "volume_usd_change_percent_24h": -32.13, // 24小时交易量变化(%)

      "long_volume_usd": 5800829746.047, // 多单成交价值(USD)
      "short_volume_usd": 5516750363.4571, // 空单成交价值(USD)
      "long_volume_quantity": 1130850, // 多单成交笔数
      "short_volume_quantity": 1162710, // 空单成交笔数

      "open_interest_quantity": 77881.234, // 未平仓合约数量
      "open_interest_usd": 6589095073.8296, // 未平仓合约价值(USD)
      "open_interest_change_percent_24h": 1.9, // 24小时未平仓合约变化(%)

      "long_liquidation_usd_24h": 3654182.12, // 近24小时多单爆仓金额(USD)
      "short_liquidation_usd_24h": 4099047.79, // 近24小时空单爆仓金额(USD)

      "funding_rate": 0.002007, // 当前资金费率
      "next_funding_time": 1744963200000, // 下一次资金费率时间戳

      "open_interest_volume_radio": 0.5822, // 未平仓合约与交易量比率
      "oi_vol_ratio_change_percent_24h": 50.13 // 24小时比率变化(%)
    },
    {
      "instrument_id": "BTC_USDT", // 合约交易对
      "exchange_name": "Gate.io", // 交易所名称
      "symbol": "BTC/USDT", // 币种对

      "current_price": 84616.3, // 当前价格
      "index_price": 84643.36, // 指数价格
      "price_change_percent_24h": 0.69, // 24小时价格变化(%)

      "volume_usd": 1711484049.255, // 24小时交易量(USD)
      "volume_usd_change_percent_24h": -67.03, // 24小时交易量变化(%)

      "long_volume_usd": 870432407.5966, // 多单成交价值(USD)
      "short_volume_usd": 841051641.6584, // 空单成交价值(USD)
      "long_volume_quantity": 210027, // 多单成交笔数
      "short_volume_quantity": 218777, // 空单成交笔数

      "open_interest_quantity": 69477.278, // 未平仓合约数量
      "open_interest_usd": 5878785139.331, // 未平仓合约价值(USD)
      "open_interest_change_percent_24h": 3.82, // 24小时未平仓合约变化(%)

      "long_liquidation_usd_24h": 1502896.68, // 近24小时多单爆仓金额(USD)
      "short_liquidation_usd_24h": 1037959.7, // 近24小时空单爆仓金额(USD)

      "funding_rate": 0.0022, // 当前资金费率

      "open_interest_volume_radio": 3.4349, // 未平仓合约与交易量比率
      "oi_vol_ratio_change_percent_24h": 214.93 // 24小时比率变化(%)
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                            |
| ------ | ------ | --- | --------------------------------------------- |
| symbol | string | YES | 交易币种（例如：BTC）。可通过 'support-coins' 接口获取支持的币种列表。 |

