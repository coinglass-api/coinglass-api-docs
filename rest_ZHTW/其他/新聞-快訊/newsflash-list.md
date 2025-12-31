# 其他 - 新聞、快訊 - 快訊


```
GET /api/newsflash/list
```


這個接口提供即時快訊列表（最多回傳近1000條快訊）

***快取 / 更新頻率:*** 實時更新

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    {
      "newsflash_picture": "https://image.panewslab.com/upload/image/20220108/S6c26d7af3a974db1ab40792d50f33581.jpeg", //快訊圖片
      "newsflash_title": "BTC跌破102000美元，日內下跌0.03%",  //快訊標題
      "newsflash_content": "PANews 11月7日消息，歐易OKX行情顯示，BTC剛跌破102,000美元，現報101,980.10美元/枚，日內下跌0.03%。",  // 快訊內容
      "source_name": "PANews", // 快訊來源名稱
      "source_website_logo": "https://cdn.coinglasscdn.com/news/panews.png", // 快訊來源logo
      "newsflash_release_time": 1762484600000  // 快訊發佈時間
    },
    {
      "newsflash_title": "BTC反彈突破102000 USDT，24H漲幅1.36%",
      "newsflash_content": " Odaily星球日報訊OKX 行情顯示，BTC 反彈突破102000 USDT，現報102033.9 USDT，24H 漲幅收窄至1.36%。 （本條快訊由AI輔助生成）",
      "source_name": "ODAILY",
      "source_website_logo": "https://cdn.coinglasscdn.com/news/odaily.png",
      "newsflash_release_time": 1762484473000
    },
  ]
}

```

 **Parameters:**
| 名称         | 类型      | 必填 | 描述                              |
| ---------- | ------- | -- | ------------------------------- |
| start_time | integer | NO | 起始時間戳（單位：毫秒，例如：1641522717000）。  |
| end_time   | integer | NO | 結束時間戳記（單位：毫秒，例如：1641522717000）。 |
| language   | string  | NO | 支援的語言： 'zh' 、'zh-tw'            |
| page       | integer | NO | 目前頁碼                            |
| per_page   | integer | NO | 每頁回傳條數                          |

