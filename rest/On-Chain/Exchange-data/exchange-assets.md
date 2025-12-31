# On-Chain - Exchange data - Exchange Assets


```
GET /api/exchange/assets
```


This endpoint provides asset holdings data for exchange wallets, including wallet address, asset balance, USD value, and real-time price information for each asset.

***Cache / Update Frequency:*** every 1 hour for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

# Respones Data

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
| Name     | Type   | Mandatory | Description                                                                                        |
| -------- | ------ | --------- | -------------------------------------------------------------------------------------------------- |
| exchange | string | YES       | Exchange name (e.g., Binance). Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| per_page | string | NO        | Number of results per page.                                                                        |
| page     | string | NO        | Page number for pagination, default: 1                                                             |

