# Futures - Hyperliquid Positions - Hyperliquid Wallet PNL Distribution


```
GET /api/hyperliquid/wallet/pnl-distribution
```


This endpoint provides real-time Hyperliquid wallet PNL distribution data, grouped by PNL size tiers, including address counts, long/short position values, sentiment indicators, and profit/loss distribution.

**Cache / Update Frequency:** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |



**Response Data:**

```json
{
  "code": "0",
  "data": [
  {
    "group_name": "Money_Printer", // PnL tier label
    // money_printer | smart_money | grinder | humble_earner
    // exit_liquidity | semi_rekt | full_rekt | giga_rekt

    "all_address_count": 518, // total addresses
    "position_address_count": 286, // addresses with positions
    "position_address_percent": 55.22, // position address %

    "bias_score": -0.42, // long/short bias score

    "bias_remark": "bearish", // sentiment label
    // bearish | slightly_bearish | indecisive | bullish | very_bullish

    "minimum_amount": 100000, // min PnL range
    "maximum_amount": 1000000, // max PnL range

    "long_position_usd": 1624390818.866083999, // long position value
    "short_position_usd": 2374121810.5067759868, // short position value
    "long_position_usd_percent": 40.62, // long value %
    "short_position_usd_percent": 59.38, // short value %

    "position_usd": 3998512629.3728599858, // total position value

    "profit_address_count": 211, // profitable addresses
    "loss_address_count": 75, // losing addresses
    "profit_address_percent": 73.78, // profit %
    "loss_address_percent": 26.22 // loss %
    }
  ]

}
```

