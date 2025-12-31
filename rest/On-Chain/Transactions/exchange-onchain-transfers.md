# On-Chain - Transactions - Exchange On-chain Transfers (ERC-20)


```
GET /api/exchange/chain/tx/list
```


This endpoint provides on-chain transfer records (ERC-20) for exchanges.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                            |
| ---------- | ------- | --------- | -------------------------------------------------------------------------------------- |
| symbol     | string  | NO        | Must be a token symbol supported by the ERC-20 protocol on the Ethereum (ETH) network. |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1706089927315).                                 |
| min_usd    | number  | NO        | Minimum transfer amount filter, specified in USD.                                      |
| per_page   | integer | NO        | Number of results per page.  Max:100                                                   |
| page       | integer | NO        | Page number for pagination, default: 1.                                                |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "transaction_hash": "0xb8d08182d2de176ac42dceba9ff82a7a5fe650c1e56285d6810daac9561ff9dc", // Transaction hash
      "asset_symbol": "USDT",                       // Asset symbol
      "amount_usd": 9998.5,                         // Amount in USD
      "asset_quantity": 9998.5,                     // Quantity
      "exchange_name": "Coinbase",                 // Exchange name
      "transfer_type": 1,                           // Transfer type: 1 = Inflow, 2 = Outflow, 3 = Internal transfer
      "from_address": "0x16c6897438c4f0c7894862d884549e8564c4025f", // From address
      "to_address": "0xa9d1e08c7793af67e9d92fe308d5697fb81d3e43",   // To address
      "transaction_time": 1745224211                // Transaction time (timestamp in seconds)
    },
    {
      "transaction_hash": "0x033c56cb05654f2c360235eff99c84f0eee9c6330fc7012930adfe0a88789c0f", // Transaction hash
      "asset_symbol": "MANA",                       // Asset symbol
      "amount_usd": 6368.95196834,                  // Amount in USD
      "asset_quantity": 20091.33113044,             // Quantity
      "exchange_name": "Binance",                  // Exchange name
      "transfer_type": 1,                           // Transfer type: 1 = Inflow, 2 = Outflow, 3 = Internal transfer
      "from_address": "0x06fd4ba7973a0d39a91734bbc35bc2bcaa99e3b0", // From address
      "to_address": "0x28c6c06298d514db089934071355e5743bf21d60",   // To address
      "transaction_time": 1745224211                // Transaction time (timestamp in seconds)
    }
  ]
}

```

