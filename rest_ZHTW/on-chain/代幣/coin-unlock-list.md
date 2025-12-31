# 鏈上 - 代幣 - 代幣解鎖列表


```
GET /api/coin/unlock-list
```


該接口返回代幣解鎖數據以及即將到來的解鎖計劃。

***快取 / 更新頻率:*** 实时更新

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0", // 返回狀態碼
  "data": [ // 代幣列表
    {
      "symbol": "GT", // 代幣符號
      "name": "GateToken", // 代幣名稱
      "symbol_logo_url": "https://cdn.coinglasscdn.com/static/img/coins/gt.jpg", // 圖標連結
      "price": 10.377, // 最新價格
      "price_change_percent_24h": 2.67, // 24小時漲跌幅
      "market_cap": 1217683606.698, // 市值
      "total_supply": 300000000, // 總供應量
      "fully_diluted_valuation": 3115642754.097, // 全稀釋估值
      "total_locked": 74868300, // 鎖倉數量
      "circulating_supply": 117344474, // 流通供應量
      "total_unlocked": 162691500, // 已解鎖數量
      "next_unlock_date": 1765152000000, // 下次解鎖時間
      "next_unlock_tokens": 48600, // 下次解鎖數量
      "next_unlock_of_circulating": 0.041416522093745974, // 佔流通量比例
      "next_unlock_of_supply": 0.0162 // 佔總供應量比例
    },
    ....
  ]
}

```

 **Parameters:**
| 名称       | 类型      | 必填 | 描述     |
| -------- | ------- | -- | ------ |
| per_page | integer | NO | 每頁返回數量 |
| page     | integer | NO | 頁碼     |

