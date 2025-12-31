# 合约 - 爆仓与清算 - 清算最大痛点


```
GET /api/futures/liquidation/max-pain
```


该接口提供主流加密货币的清算“最大痛点”价格，以及清算强度。

***缓存 / 更新频率:*** 实时.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ❌   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "data": [
    {
      "symbol": "BTC",//币种
      "price": 110625.1, //价格
      "long_max_pain_liq_level": 75677278.26,//多单最大痛点清算强度
      "long_max_pain_liq_price": 113046.71, //多单最大痛点清算价格
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
| 名称    | 类型     | 必填 | 描述                                              |
| ----- | ------ | -- | ----------------------------------------------- |
| range | string | NO | 数据时间间隔。支持的取值包括： 12h, 24h, 48h, 3d, 7d, 14d, 30d |

