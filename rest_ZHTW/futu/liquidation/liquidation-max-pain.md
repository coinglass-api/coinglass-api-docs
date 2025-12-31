# 合約數據 - 爆倉與清算 - 清算最大痛點


```
GET /api/futures/liquidation/max-pain
```


該接口提供主流加密貨幣的清算「最大痛點」價格，以及清算強度。

***快取 / 更新頻率:*** 即時更新.

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ❌   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    {
      "symbol": "BTC",//幣種
      "price": 110625.1, //價格
      "long_max_pain_liq_level": 75677278.26,//多單最大痛點清算強度
      "long_max_pain_liq_price": 113046.71, //多單最大痛點清算價格
      "short_max_pain_liq_level": 44617473.19,
      "short_max_pain_liq_price": 109748.37
    
    {
      "symbol": "ETH",
      "price": 3914.14,
      "long_max_pain_liq_level": 34406421.23,
      "long_max_pain_liq_price": 3955.722,
      "short_max_pain_liq_level": 44375943.61,
      "short_max_pain_liq_price": 3820.002
    },
    {
      "symbol": "SOL",
      "price": 195.1,
      "long_max_pain_liq_level": 12467317.12,
      "long_max_pain_liq_price": 199.468,
      "short_max_pain_liq_level": 12927647.29,
      "short_max_pain_liq_price": 190.186
    },
    ....
  ]
}

```

 **Parameters:**
| 名称    | 类型     | 必填 | 描述                                             |
| ----- | ------ | -- | ---------------------------------------------- |
| range | string | NO | 數據時間間隔。支持的值包括： 12h, 24h, 48h, 3d, 7d, 14d, 30d |

