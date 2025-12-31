# On-Chain - Token - Token Vesting


```
GET /api/coin/vesting
```


This endpoint returns detailed vesting data and upcoming unlock schedules for a specific token.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |

<br />

<br />

```json
{
  "code": "0",
  "data": {
 {
  "market_cap": 9366969675.066894, // market cap
  "symbol": "HYPE", // token symbol
  "total_untracked": 451880000, // untracked supply
  "listing_date": 1732838400000, // listing time
  "vesting_start_date": 1732838400000, // vesting start
  "total_supply": 999835210, // total supply
  "total_locked": 236721940, // total locked
  "total_unlocked": 310986320, // total unlocked
  "vesting_end_date": 1859068800000, // vesting end
  "next_unlock": { // next unlock info
    "date": 1764720000000, // unlock time
    "next_unlock_token_amount": "216580" // unlock amount
  },
  "circulating_supply": 270772999, // circulating supply
  "total_untracked_percent": 45.188, // untracked percent
  "allocations": [ // allocation list
    {
      "is_untracked": true, // untracked flag
      "allocation_of_supply": 38.888, // supply percent
      "name": "Future Emissions & Community Rewards", // allocation name
      "token_amount": "388880000" // token amount
    },
    {
      "is_untracked": false, // untracked flag
      "allocation_of_supply": 31, // supply percent
      "name": "Genesis Distribution", // allocation name
      "unlock_type": "nonlinear", // unlock type
      "token_amount": "310000000", // token amount
      "tge_unlocked_token_amount": "310000000", // TGE unlocked
      "unlocked_token_amount": "310000000", // total unlocked
      "tge_unlock_percent": 100 // TGE percent
    },
    {
      "is_untracked": false, // untracked flag
      "vesting_start_date": 1764374400000, // vesting start
      "locked_token_amount": "236721940", // locked amount
      "vesting_end_date": 1859068800000, // vesting end
      "tge_unlocked_token_amount": "0", // TGE unlocked
      "next_unlock": { // next unlock info
        "date": 1764720000000, // unlock time
        "next_unlock_token_amount": "216580" // unlock amount
      },
      "unlocked_token_amount": "866320", // unlocked amount
      "tge_unlock_percent": 0, // TGE percent
      "vesting_duration_value": 3, // duration value
      "vesting_duration_type": "year", // duration type
      "allocation_of_supply": 23.8, // supply percent
      "unlock_frequency_type": "day", // unlock unit
      "name": "Core Contributors", // allocation name
      "unlock_type": "linear", // unlock type
      "token_amount": "238000000", // token amount
      "unlock_frequency_value": 1 // unlock interval
    },
    {
      "is_untracked": true, // untracked flag
      "allocation_of_supply": 6, // supply percent
      "name": "Hyper Foundation", // allocation name
      "token_amount": "60000000" // token amount
    },
    {
      "is_untracked": true, // untracked flag
      "allocation_of_supply": 0.3, // supply percent
      "name": "Community Grants", // allocation name
      "token_amount": "3000000" // token amount
    },
    {
      "is_untracked": false, // untracked flag
      "allocation_of_supply": 0.012, // supply percent
      "name": "HIP-2", // allocation name
      "unlock_type": "nonlinear", // unlock type
      "token_amount": "120000", // token amount
      "tge_unlocked_token_amount": "120000", // TGE unlocked
      "unlocked_token_amount": "120000", // total unlocked
      "tge_unlock_percent": 100 // TGE percent
    }
  ],
  "fully_diluted_valuation": 34587740013.671524, // FDV
  "name": "Hyperliquid", // project name
  "max_supply": 1000000000, // max supply
  "chart": [ // chart data
    {
      "date": 1732838400000, // chart time
      "allocations": [ // chart allocations
        {
          "name": "Genesis Distribution", // name
          "unlocked_percent": 31, // unlocked percent
          "token_amount": "310000000", // token amount
          "unlocked_token_amount": "310000000" // unlocked amount
        },
        {
          "name": "Core Contributors", // name
          "unlocked_percent": 0, // unlocked percent
          "token_amount": "238000000", // token amount
          "unlocked_token_amount": "0" // unlocked amount
        },
        {
          "name": "HIP-2", // name
          "unlocked_percent": 0.012, // unlocked percent
          "token_amount": "120000", // token amount
          "unlocked_token_amount": "120000" // unlocked amount
        }
      ],
      "is_tge": true, // is TGE flag
      "unlocked_percent": 31.012, // total percent
      "unlocked_token_amount": "310120000" // total unlocked
    }
    ],
    "untracked_allocation_names": [
      "Community Grants",
      "Future Emissions & Community Rewards",
      "Hyper Foundation"
    ]
  }
}
```

 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                          |
| ------ | ------ | --------- | ------------------------------------------------------------------------------------ |
| symbol | string | YES       | Trading coin (e.g., HYPE). Retrieve supported coins via the 'token-unlock-list' API. |

