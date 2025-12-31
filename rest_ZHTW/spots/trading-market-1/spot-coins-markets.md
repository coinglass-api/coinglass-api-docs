# 現貨 - 交易市場 - 幣種市場列表


```
GET /api/spot/coins-markets
```


該接口提供現貨幣種的相關指標數據數據

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0", 
  "msg": "success", 
  "data": [
    {
      "symbol": "BTC", // 幣種代號，如 BTC 表示比特幣
      "current_price": 87500, // 當前幣價（美元）

      "market_cap": 1735007745495.3037, // 當前市值（美元）

      // 各週期內價格變化（單位：美元）
      "price_change_5m": 101.5, // 最近5分鐘價格變化
      "price_change_15m": 46.18, // 最近15分鐘價格變化
      "price_change_30m": -77.22, // 最近30分鐘價格變化
      "price_change_1h": 12.56, // 最近1小時價格變化
      "price_change_4h": 147.75, // 最近4小時價格變化
      "price_change_12h": 147.75, // 最近12小時價格變化
      "price_change_24h": 2799.99, // 最近24小時價格變化
      "price_change_1w": 2989.69, // 最近1週價格變化

      // 各週期內價格變化百分比（單位：%）
      "price_change_percent_5m": 0.12, // 最近5分鐘價格漲跌幅
      "price_change_percent_15m": 0.05, // 最近15分鐘價格漲跌幅
      "price_change_percent_30m": -0.09, // 最近30分鐘價格漲跌幅
      "price_change_percent_1h": 0.01, // 最近1小時價格漲跌幅
      "price_change_percent_4h": 0.17, // 最近4小時價格漲跌幅
      "price_change_percent_12h": 0.17, // 最近12小時價格漲跌幅
      "price_change_percent_24h": 3.31, // 最近24小時價格漲跌幅
      "price_change_percent_1w": 3.54, // 最近1週價格漲跌幅

      // 各週期內成交量（單位：美元）
      "volume_usd_1h": 129491564.6994, // 最近1小時成交總量
      "volume_usd_5m": 11056683.8336, // 最近5分鐘成交總量
      "volume_usd_15m": 50625331.2542, // 最近15分鐘成交總量
      "volume_usd_30m": 80070296.0794, // 最近30分鐘成交總量
      "volume_usd_4h": 580775143.5162, // 最近4小時成交總量
      "volume_usd_12h": 2663308247.353, // 最近12小時成交總量
      "volume_usd_24h": 3719093876.3834, // 最近24小時成交總量
      "volume_usd_1w": 16801739001.0272, // 最近1週成交總量

      // 各週期內成交量變化值（單位：美元，與上一個週期比較）
      "volume_change_usd_1h": -35317032.6336, // 成交量變化：最近1小時與前一小時相比
      "volume_change_usd_5m": -110911976.2243,
      "volume_change_usd_15m": -59017725.7105,
      "volume_change_usd_30m": -39864985.2519,
      "volume_change_usd_4h": -1084757627.3629,
      "volume_change_usd_12h": 1624238611.116,
      "volume_change_usd_24h": 1967797576.5416,
      "volume_change_usd_1w": -23396586539.5365,

      // 各週期內成交量變化百分比（單位：%）
      "volume_change_percent_1h": -21.43, // 成交量變化百分比：1小時
      "volume_change_percent_5m": -90.93,
      "volume_change_percent_15m": -53.83,
      "volume_change_percent_30m": -33.24,
      "volume_change_percent_4h": -65.13,
      "volume_change_percent_12h": 156.32,
      "volume_change_percent_24h": 112.36,
      "volume_change_percent_1w": 3.54,

      // 各週期內主動買入成交量（單位：美元）
      "buy_volume_usd_1h": 55687151.2164,
      "buy_volume_usd_5m": 4634327.6087,
      "buy_volume_usd_15m": 20222399.059,
      "buy_volume_usd_30m": 33140975.4441,
      "buy_volume_usd_4h": 278174843.6339,
      "buy_volume_usd_12h": 1410854413.4688,
      "buy_volume_usd_24h": 1923920264.0666,
      "buy_volume_usd_1w": 8116673333.4846,

      // 各週期內主動賣出成交量（單位：美元）
      "sell_volume_usd_1h": 73804413.4829,
      "sell_volume_usd_5m": 6422356.2248,
      "sell_volume_usd_15m": 30402932.1951,
      "sell_volume_usd_30m": 46929320.6352,
      "sell_volume_usd_4h": 302600299.8822,
      "sell_volume_usd_12h": 1252453833.8841,
      "sell_volume_usd_24h": 1795173612.3167,
      "sell_volume_usd_1w": 8685065667.5425,

      // 主動成交量淨流入（= 買入 - 賣出），單位：美元
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
| per_page | integer | NO | 每頁返回的結果數量。    |
| page     | integer | NO | 分頁的頁碼，默認值為 1。 |

