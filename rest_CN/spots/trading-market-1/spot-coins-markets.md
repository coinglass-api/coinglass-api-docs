# 现货 - 交易市场 - 币种市场列表


```
GET /api/spot/coins-markets
```


该接口提供现货币种的相关指标信息。

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
      "symbol": "BTC", // 币种代号，如 BTC 表示比特币
      "current_price": 87500, // 当前币价（美元）

      "market_cap": 1735007745495.3037, // 当前市值（美元）

      // 各周期内价格变化（单位：美元）
      "price_change_5m": 101.5, // 最近5分钟价格变化
      "price_change_15m": 46.18, // 最近15分钟价格变化
      "price_change_30m": -77.22, // 最近30分钟价格变化
      "price_change_1h": 12.56, // 最近1小时价格变化
      "price_change_4h": 147.75, // 最近4小时价格变化
      "price_change_12h": 147.75, // 最近12小时价格变化
      "price_change_24h": 2799.99, // 最近24小时价格变化
      "price_change_1w": 2989.69, // 最近1周价格变化

      // 各周期内价格变化百分比（单位：%）
      "price_change_percent_5m": 0.12, // 最近5分钟价格涨跌幅
      "price_change_percent_15m": 0.05, // 最近15分钟价格涨跌幅
      "price_change_percent_30m": -0.09, // 最近30分钟价格涨跌幅
      "price_change_percent_1h": 0.01, // 最近1小时价格涨跌幅
      "price_change_percent_4h": 0.17, // 最近4小时价格涨跌幅
      "price_change_percent_12h": 0.17, // 最近12小时价格涨跌幅
      "price_change_percent_24h": 3.31, // 最近24小时价格涨跌幅
      "price_change_percent_1w": 3.54, // 最近1周价格涨跌幅

      // 各周期内成交量（单位：美元）
      "volume_usd_1h": 129491564.6994, // 最近1小时成交总量
      "volume_usd_5m": 11056683.8336, // 最近5分钟成交总量
      "volume_usd_15m": 50625331.2542, // 最近15分钟成交总量
      "volume_usd_30m": 80070296.0794, // 最近30分钟成交总量
      "volume_usd_4h": 580775143.5162, // 最近4小时成交总量
      "volume_usd_12h": 2663308247.353, // 最近12小时成交总量
      "volume_usd_24h": 3719093876.3834, // 最近24小时成交总量
      "volume_usd_1w": 16801739001.0272, // 最近1周成交总量

      // 各周期内成交量变化值（单位：美元，与上一个周期比较）
      "volume_change_usd_1h": -35317032.6336, // 成交量变化：最近1小时与前一小时相比
      "volume_change_usd_5m": -110911976.2243,
      "volume_change_usd_15m": -59017725.7105,
      "volume_change_usd_30m": -39864985.2519,
      "volume_change_usd_4h": -1084757627.3629,
      "volume_change_usd_12h": 1624238611.116,
      "volume_change_usd_24h": 1967797576.5416,
      "volume_change_usd_1w": -23396586539.5365,

      // 各周期内成交量变化百分比（单位：%）
      "volume_change_percent_1h": -21.43, // 成交量变化百分比：1小时
      "volume_change_percent_5m": -90.93,
      "volume_change_percent_15m": -53.83,
      "volume_change_percent_30m": -33.24,
      "volume_change_percent_4h": -65.13,
      "volume_change_percent_12h": 156.32,
      "volume_change_percent_24h": 112.36,
      "volume_change_percent_1w": 3.54,

      // 各周期内主动买入成交量（单位：美元）
      "buy_volume_usd_1h": 55687151.2164,
      "buy_volume_usd_5m": 4634327.6087,
      "buy_volume_usd_15m": 20222399.059,
      "buy_volume_usd_30m": 33140975.4441,
      "buy_volume_usd_4h": 278174843.6339,
      "buy_volume_usd_12h": 1410854413.4688,
      "buy_volume_usd_24h": 1923920264.0666,
      "buy_volume_usd_1w": 8116673333.4846,

      // 各周期内主动卖出成交量（单位：美元）
      "sell_volume_usd_1h": 73804413.4829,
      "sell_volume_usd_5m": 6422356.2248,
      "sell_volume_usd_15m": 30402932.1951,
      "sell_volume_usd_30m": 46929320.6352,
      "sell_volume_usd_4h": 302600299.8822,
      "sell_volume_usd_12h": 1252453833.8841,
      "sell_volume_usd_24h": 1795173612.3167,
      "sell_volume_usd_1w": 8685065667.5425,

      // 主动成交量净流入（= 买入 - 卖出），单位：美元
      "volume_flow_usd_1h": -18117262.2665,
      "volume_flow_usd_5m": -1788028.6161,
      "volume_flow_usd_15m": -10180533.1361,
      "volume_flow_usd_30m": -13788345.1911,
      "volume_flow_usd_4h": -24425456.2483,
      "volume_flow_usd_12h": 158400579.5847,
      "volume_flow_usd_24h": 128746651.7499,
      "volume_flow_usd_1w": -568392334.0579
    }
  ]
}

```

 **Parameters:**
| 名称       | 类型      | 必填 | 描述            |
| -------- | ------- | -- | ------------- |
| per_page | integer | NO | 每页返回的结果数量。    |
| page     | integer | NO | 分页的页码，默认值为 1。 |

