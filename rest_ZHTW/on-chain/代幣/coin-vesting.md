# 鏈上 - 代幣 - 代幣解鎖詳情


```
GET /api/coin/vesting
```


該接口返回指定代幣的詳細鎖倉數據及即將到來的解鎖計劃。

***快取 / 更新頻率:*** 实时更新

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0", // 返回狀態碼
  "data": {
    "market_cap": 9366969675.066894, // 市值
    "symbol": "HYPE", // 代幣符號
    "total_untracked": 451880000, // 未追蹤數量
    "listing_date": 1732838400000, // 上線時間
    "vesting_start_date": 1732838400000, // 鎖倉開始時間
    "total_supply": 999835210, // 總供應量
    "total_locked": 236721940, // 總鎖倉量
    "total_unlocked": 310986320, // 總解鎖量
    "vesting_end_date": 1859068800000, // 鎖倉結束時間
    "next_unlock": { // 下次解鎖資訊
      "date": 1764720000000, // 解鎖時間
      "next_unlock_token_amount": "216580" // 解鎖數量
    },
    "circulating_supply": 270772999, // 流通量
    "total_untracked_percent": 45.188, // 未追蹤占比
    "allocations": [ // 分配列表
      {
        "is_untracked": true, // 是否未追蹤
        "allocation_of_supply": 38.888, // 占總供應比例
        "name": "Future Emissions & Community Rewards", // 分配名稱
        "token_amount": "388880000" // 代幣數量
      },
      {
        "is_untracked": false, // 是否未追蹤
        "allocation_of_supply": 31, // 占總供應比例
        "name": "Genesis Distribution", // 分配名稱
        "unlock_type": "nonlinear", // 解鎖方式
        "token_amount": "310000000", // 代幣數量
        "tge_unlocked_token_amount": "310000000", // TGE 解鎖數量
        "unlocked_token_amount": "310000000", // 已解鎖數量
        "tge_unlock_percent": 100 // TGE 解鎖比例
      },
      {
        "is_untracked": false, // 是否未追蹤
        "vesting_start_date": 1764374400000, // 鎖倉開始時間
        "locked_token_amount": "236721940", // 鎖倉數量
        "vesting_end_date": 1859068800000, // 鎖倉結束時間
        "tge_unlocked_token_amount": "0", // TGE 解鎖數量
        "next_unlock": { // 下次解鎖資訊
          "date": 1764720000000, // 解鎖時間
          "next_unlock_token_amount": "216580" // 解鎖數量
        },
        "unlocked_token_amount": "866320", // 已解鎖數量
        "tge_unlock_percent": 0, // TGE 解鎖比例
        "vesting_duration_value": 3, // 鎖倉時長數值
        "vesting_duration_type": "year", // 鎖倉時長單位
        "allocation_of_supply": 23.8, // 占總供應比例
        "unlock_frequency_type": "day", // 解鎖頻率類型
        "name": "Core Contributors", // 分配名稱
        "unlock_type": "linear", // 解鎖方式
        "token_amount": "238000000", // 代幣數量
        "unlock_frequency_value": 1 // 解鎖頻率數值
      },
      {
        "is_untracked": true, // 是否未追蹤
        "allocation_of_supply": 6, // 占總供應比例
        "name": "Hyper Foundation", // 分配名稱
        "token_amount": "60000000" // 代幣數量
      },
      {
        "is_untracked": true, // 是否未追蹤
        "allocation_of_supply": 0.3, // 占總供應比例
        "name": "Community Grants", // 分配名稱
        "token_amount": "3000000" // 代幣數量
      },
      {
        "is_untracked": false, // 是否未追蹤
        "allocation_of_supply": 0.012, // 占總供應比例
        "name": "HIP-2", // 分配名稱
        "unlock_type": "nonlinear", // 解鎖方式
        "token_amount": "120000", // 代幣數量
        "tge_unlocked_token_amount": "120000", // TGE 解鎖數量
        "unlocked_token_amount": "120000", // 已解鎖數量
        "tge_unlock_percent": 100 // TGE 解鎖比例
      }
    ],
    "fully_diluted_valuation": 34587740013.671524, // 全稀釋估值
    "name": "Hyperliquid", // 項目名稱
    "max_supply": 1000000000, // 最大供應量
    "chart": [ // 圖表資料
      {
        "date": 1732838400000, // 圖表時間
        "allocations": [ // 圖表分配
          {
            "name": "Genesis Distribution", // 名稱
            "unlocked_percent": 31, // 解鎖比例
            "token_amount": "310000000", // 代幣數量
            "unlocked_token_amount": "310000000" // 解鎖數量
          },
          {
            "name": "Core Contributors", // 名稱
            "unlocked_percent": 0, // 解鎖比例
            "token_amount": "238000000", // 代幣數量
            "unlocked_token_amount": "0" // 解鎖數量
          },
          {
            "name": "HIP-2", // 名稱
            "unlocked_percent": 0.012, // 解鎖比例
            "token_amount": "120000", // 代幣數量
            "unlocked_token_amount": "120000" // 解鎖數量
          }
        ],
        "is_tge": true, // 是否為 TGE
        "unlocked_percent": 31.012, // 總解鎖比例
        "unlocked_token_amount": "310120000" // 總解鎖數量
      }
    ],
    "untracked_allocation_names": [ // 未追蹤分配名稱列表
      "Community Grants",
      "Future Emissions & Community Rewards",
      "Hyper Foundation"
    ]
  }
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                               |
| ------ | ------ | --- | ------------------------------------------------ |
| symbol | string | YES | 交易代幣（例如 HYPE）。可透過「token-unlock-list」接口取得支援的代幣列表。 |

