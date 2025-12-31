# 鏈上 - 交易所數據 - 交易所資產透明度


```
GET /api/exchange/assets
```


此接口提供交易所錢包的資產持有數據，包括錢包地址、資產餘額、美元估值以及每種資產的即時價格數據。

***快取 / 更新頻率:*** 每 1小時更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版    | 創業版      | 標準版 | 專業版 | 企業版 |
| :----- | :----- | :------- | :-- | :-- | :-- |
| 可用性    | ✅      | ✅        | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "wallet_address": "34xp4vRoCGJym3xR7yCVPFHoCNxv4Twseo",
      "balance": 248597.54,
      "balance_usd": 21757721869.92,
      "symbol": "BTC",
      "assets_name": "Bitcoin",
      "price": 87521.87117346626
    },
    {
      "wallet_address": "3M219KR5vEneNb47ewrPfWyb5jQ2DjxRP6",
      "balance": 139456.08,
      "balance_usd": 12205457068.12,
      "symbol": "BTC",
      "assets_name": "Bitcoin",
      "price": 87521.87117346626
    },
```

 **Parameters:**
| 名称       | 类型     | 必填  | 描述                                                           |
| -------- | ------ | --- | ------------------------------------------------------------ |
| exchange | string | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |
| per_page | string | NO  | 每頁返回的結果數量。                                                   |
| page     | string | NO  | 分頁的頁碼，默認值為 1。                                                |

