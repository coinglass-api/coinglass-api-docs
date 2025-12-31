# 链上 - 交易所数据 - 交易所资产透明度


```
GET /api/exchange/assets
```


此接口提供交易所钱包的资产持有数据，包括钱包地址、资产余额、美元估值以及每种资产的实时价格信息。

***缓存/ 更新频率 :*** 1小时一次.

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
| 名称       | 类型     | 必填  | 描述                                                            |
| -------- | ------ | --- | ------------------------------------------------------------- |
| exchange | string | YES | 交易所名称（例如：Binance、OKX）。可通过 support-exchange-pair 接口获取支持的交易所列表。 |
| per_page | string | NO  | 每页返回的数据数量。                                                    |
| page     | string | NO  | 用于分页的页码，默认值为 1。                                               |

