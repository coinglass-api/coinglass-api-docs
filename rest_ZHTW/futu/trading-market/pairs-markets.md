# 合約數據 - 交易市場 - 交易對市場列表


```
GET /api/futures/pairs-markets
```


該接口提供合約交易對的相關指標數據

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "instrument_id": "BTCUSDT", // 合約交易對
      "exchange_name": "Binance", // 交易所名稱
      "symbol": "BTC/USDT", // 幣種對

      "current_price": 84604.3, // 當前價格
      "index_price": 84646.66222222, // 指數價格
      "price_change_percent_24h": 0.67, // 24小時價格變化(%)

      "volume_usd": 11317580109.5041, // 24小時交易量(USD)
      "volume_usd_change_percent_24h": -32.13, // 24小時交易量變化(%)

      "long_volume_usd": 5800829746.047, // 多單成交價值(USD)
      "short_volume_usd": 5516750363.4571, // 空單成交價值(USD)
      "long_volume_quantity": 1130850, // 多單成交筆數
      "short_volume_quantity": 1162710, // 空單成交筆數

      "open_interest_quantity": 77881.234, // 未平倉合約數量
      "open_interest_usd": 6589095073.8296, // 未平倉合約價值(USD)
      "open_interest_change_percent_24h": 1.9, // 24小時未平倉合約變化(%)

      "long_liquidation_usd_24h": 3654182.12, // 近24小時多單爆倉金額(USD)
      "short_liquidation_usd_24h": 4099047.79, // 近24小時空單爆倉金額(USD)

      "funding_rate": 0.002007, // 當前資金費率
      "next_funding_time": 1744963200000, // 下一次資金費率時間戳

      "open_interest_volume_radio": 0.5822, // 未平倉合約與交易量比率
      "oi_vol_ratio_change_percent_24h": 50.13 // 24小時比率變化(%)
    },
    {
      "instrument_id": "BTC_USDT", // 合約交易對
      "exchange_name": "Gate.io", // 交易所名稱
      "symbol": "BTC/USDT", // 幣種對

      "current_price": 84616.3, // 當前價格
      "index_price": 84643.36, // 指數價格
      "price_change_percent_24h": 0.69, // 24小時價格變化(%)

      "volume_usd": 1711484049.255, // 24小時交易量(USD)
      "volume_usd_change_percent_24h": -67.03, // 24小時交易量變化(%)

      "long_volume_usd": 870432407.5966, // 多單成交價值(USD)
      "short_volume_usd": 841051641.6584, // 空單成交價值(USD)
      "long_volume_quantity": 210027, // 多單成交筆數
      "short_volume_quantity": 218777, // 空單成交筆數

      "open_interest_quantity": 69477.278, // 未平倉合約數量
      "open_interest_usd": 5878785139.331, // 未平倉合約價值(USD)
      "open_interest_change_percent_24h": 3.82, // 24小時未平倉合約變化(%)

      "long_liquidation_usd_24h": 1502896.68, // 近24小時多單爆倉金額(USD)
      "short_liquidation_usd_24h": 1037959.7, // 近24小時空單爆倉金額(USD)

      "funding_rate": 0.0022, // 當前資金費率

      "open_interest_volume_radio": 3.4349, // 未平倉合約與交易量比率
      "oi_vol_ratio_change_percent_24h": 214.93 // 24小時比率變化(%)
    }
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                            |
| ------ | ------ | --- | --------------------------------------------- |
| symbol | string | YES | 交易幣種（例如：BTC）。可通過 'support-coins' 接口獲取支持的幣種列表。 |

