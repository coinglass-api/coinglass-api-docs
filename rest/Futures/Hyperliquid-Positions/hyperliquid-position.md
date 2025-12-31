# Futures - Hyperliquid Positions - Hyperliquid Wallet Positions by Coin


```
GET /api/hyperliquid/position
```


This endpoint provides real-time wallet position data by coin on Hyperliquid, including user addresses, position size, margin balance, and unrealized PnL for each account.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name         | Type   | Mandatory | Description                                                                       |
| ------------ | ------ | --------- | --------------------------------------------------------------------------------- |
| symbol       | string | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API. |
| current_page | string | NO        | Current page number being returned                                                |


**Response Data:**

```json
{
  "code": "0",                     // Status code (0 = success)
  "data": {
    "total_pages": 10,          // Total pages of position data
    "current_page":1,   // Current page number being returned
    "list": [
      {
        "user": "0x5b5d51203a0f9079f8aeb098a6523a13f298c060",           //User Wallet address
        "symbol": "BTC",           // Symbol
        "position_size": -2683.14, // Position size (positive = long, negative = short)
        "entry_price": 111459.6,   // Entry price
        "mark_price": 116638,      // Current price
        "liq_price": 150629.52,    // Liquidation price
        "leverage": 10,            // Leverage
        "margin_balance": 31263482.07,        // Margin balance (USD)
        "position_value_usd": 312634820.77,   // Position value (USD)
        "unrealized_pnl": -13572345.06,       // Unrealized profit/loss (USD)
        "funding_fee": -12534553.66,          // Funding fee (USD)
        "margin_mode": "cross",               // Margin mode ("cross" or "isolated")
        "create_time": 1752152867098,         // Open time (timestamp)
        "update_time": 1758162698266          // Last update (timestamp)
      }
    ]
  }
}
```

