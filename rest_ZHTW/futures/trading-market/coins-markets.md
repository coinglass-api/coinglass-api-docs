# 合約數據 - 交易市場 - 幣種市場列表


```
GET /api/futures/coins-markets
```


該接口提供合約幣種的相關指標數據

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
      "symbol": "BTC",  // 幣種符號
      "current_price": 84773.6,  // 當前價格（單位：USD）
      "avg_funding_rate_by_oi": 0.00196,  // 按持倉量加權的平均資金費率
      "avg_funding_rate_by_vol": 0.002647,  // 按成交量加權的平均資金費率
      "market_cap_usd": 1683310500117.051,  // 市值（單位：USD）
      "open_interest_market_cap_ratio": 0.0327,  // 未平倉量與市值的比值
      "open_interest_usd": 55002072334.9376,  // 未平倉量（單位：USD）
      "open_interest_quantity": 648525.0328,  // 未平倉合約數量
      "open_interest_volume_ratio": 0.7936,  // 未平倉量與成交量的比值
      "price_change_percent_5m": -0.02,  // 價格5分鐘變化百分比
      "price_change_percent_15m": 0.06,  // 價格15分鐘變化百分比
      "price_change_percent_30m": 0.03,  // 價格30分鐘變化百分比
      "price_change_percent_1h": -0.1,  // 價格1小時變化百分比
      "price_change_percent_4h": -0.15,  // 價格4小時變化百分比
      "price_change_percent_12h": 0.15,  // 價格12小時變化百分比
      "price_change_percent_24h": 1.06,  // 價格24小時變化百分比
      "open_interest_change_percent_5m": 0,  // 未平倉量5分鐘變化百分比
      "open_interest_change_percent_15m": 0.04,  // 未平倉量15分鐘變化百分比
      "open_interest_change_percent_30m": 0,  // 未平倉量30分鐘變化百分比
      "open_interest_change_percent_1h": -0.01,  // 未平倉量1小時變化百分比
      "open_interest_change_percent_4h": 0.17,  // 未平倉量4小時變化百分比
      "open_interest_change_percent_24h": 4.58,  // 未平倉量24小時變化百分比
      "volume_change_percent_5m": -0.03,  // 成交量5分鐘變化百分比
      "volume_change_percent_15m": -0.73,  // 成交量15分鐘變化百分比
      "volume_change_percent_30m": -1.13,  // 成交量30分鐘變化百分比
      "volume_change_percent_1h": -2.33,  // 成交量1小時變化百分比
      "volume_change_percent_4h": -5.83,  // 成交量4小時變化百分比
      "volume_change_percent_24h": -26.38,  // 成交量24小時變化百分比
      "volume_change_usd_1h": 69310404660.3795,  // 成交量1小時變化（單位：USD）
      "volume_change_usd_4h": -4290959532.4414644,  // 成交量4小時變化（單位：USD）
      "volume_change_usd_24h": -24835757605.82467,  // 成交量24小時變化（單位：USD）
      "long_short_ratio_5m": 1.2523,  // 多空比（近5分鐘）
      "long_short_ratio_15m": 0.9928,  // 多空比（近15分鐘）
      "long_short_ratio_30m": 1.0695,  // 多空比（近30分鐘）
      "long_short_ratio_1h": 1.0068,  // 多空比（近1小時）
      "long_short_ratio_4h": 1.0504,  // 多空比（近4小時）
      "long_short_ratio_12h": 1.0317,  // 多空比（近12小時）
      "long_short_ratio_24h": 1.0313,  // 多空比（近24小時）
      "liquidation_usd_1h": 33621.85192,  // 總爆倉金額（近1小時，單位：USD）
      "long_liquidation_usd_1h": 22178.4681,  // 多頭爆倉金額（近1小時，單位：USD）
      "short_liquidation_usd_1h": 11443.38382,  // 空頭爆倉金額（近1小時，單位：USD）
      "liquidation_usd_4h": 222210.47117,  // 總爆倉金額（近4小時，單位：USD）
      "long_liquidation_usd_4h": 179415.77249,  // 多頭爆倉金額（近4小時，單位：USD）
      "short_liquidation_usd_4h": 42794.69868,  // 空頭爆倉金額（近4小時，單位：USD）
      "liquidation_usd_12h": 11895453.392145,  // 總爆倉金額（近12小時，單位：USD）
      "long_liquidation_usd_12h": 10223351.23772,  // 多頭爆倉金額（近12小時，單位：USD）
      "short_liquidation_usd_12h": 1672102.154425,  // 空頭爆倉金額（近12小時，單位：USD）
      "liquidation_usd_24h": 27519292.973646,  // 總爆倉金額（近24小時，單位：USD）
      "long_liquidation_usd_24h": 17793322.595016,  // 多頭爆倉金額（近24小時，單位：USD）
      "short_liquidation_usd_24h": 9725970.37863  // 空頭爆倉金額（近24小時，單位：USD）
    },
    {
      "symbol": "ETH",  // 幣種符號
      "current_price": 1582.55,  // 當前價格（單位：USD）
      "avg_funding_rate_by_oi": 0.001631,  // 持倉量加權平均資金費率
      "avg_funding_rate_by_vol": -0.000601,  // 成交量加權平均資金費率
      "market_cap_usd": 190821695398.62064,  // 市值（單位：USD）
      "open_interest_market_cap_ratio": 0.0925,  // 未平倉量與市值比值
      "open_interest_usd": 17657693967.0459,  // 未平倉量（單位：USD）
      "open_interest_quantity": 11160428.5065,  // 未平倉合約數量
      "open_interest_volume_ratio": 0.5398,  // 未平倉量與成交量比值
      "price_change_percent_5m": 0.07,  // 價格5分鐘變化百分比
      "price_change_percent_15m": 0.25,  // 價格15分鐘變化百分比
      "price_change_percent_30m": 0.07,  // 價格30分鐘變化百分比
      "price_change_percent_1h": -0.11,  // 價格1小時變化百分比
      "price_change_percent_4h": -0.05,  // 價格4小時變化百分比
      "price_change_percent_12h": -0.02,  // 價格12小時變化百分比
      "price_change_percent_24h": 0.16  // 價格24小時變化百分比
      // ...後續字段依此類推
    }
  ]
}

```

 **Parameters:**
| 名称            | 类型      | 必填 | 描述                                                                            |
| ------------- | ------- | -- | ----------------------------------------------------------------------------- |
| exchange_list | string  | NO | 以逗號分隔的交易所名稱（例如："binance, okx, bybit"）。可通過 `support-exchange-pair` 接口獲取支持的交易所。 |
| per_page      | integer | NO | 每頁返回的結果數量。                                                                    |
| page          | integer | NO | 分頁的頁碼，默認值為 1。                                                                 |

