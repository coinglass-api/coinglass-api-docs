# 链上 - 代币 - 代币解锁详情


```
GET /api/coin/vesting
```


该接口返回指定代币的详细锁仓数据及即将到来的解锁计划。

***缓存 / 更新频率:*** 实时更新

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0", // 返回状态码
  "data": {
    "market_cap": 9366969675.066894, // 市值
    "symbol": "HYPE", // 代币符号
    "total_untracked": 451880000, // 未追踪数量
    "listing_date": 1732838400000, // 上线时间
    "vesting_start_date": 1732838400000, // 锁仓开始时间
    "total_supply": 999835210, // 总供应量
    "total_locked": 236721940, // 总锁仓量
    "total_unlocked": 310986320, // 总解锁量
    "vesting_end_date": 1859068800000, // 锁仓结束时间
    "next_unlock": { // 下次解锁信息
      "date": 1764720000000, // 解锁时间
      "next_unlock_token_amount": "216580" // 解锁数量
    },
    "circulating_supply": 270772999, // 流通量
    "total_untracked_percent": 45.188, // 未追踪占比
    "allocations": [ // 分配列表
      {
        "is_untracked": true, // 是否未追踪
        "allocation_of_supply": 38.888, // 占总供应比例
        "name": "Future Emissions & Community Rewards", // 分配名称
        "token_amount": "388880000" // 代币数量
      },
      {
        "is_untracked": false, // 是否未追踪
        "allocation_of_supply": 31, // 占总供应比例
        "name": "Genesis Distribution", // 分配名称
        "unlock_type": "nonlinear", // 解锁方式
        "token_amount": "310000000", // 代币数量
        "tge_unlocked_token_amount": "310000000", // TGE 解锁数量
        "unlocked_token_amount": "310000000", // 已解锁数量
        "tge_unlock_percent": 100 // TGE 解锁比例
      },
      {
        "is_untracked": false, // 是否未追踪
        "vesting_start_date": 1764374400000, // 锁仓开始时间
        "locked_token_amount": "236721940", // 锁仓数量
        "vesting_end_date": 1859068800000, // 锁仓结束时间
        "tge_unlocked_token_amount": "0", // TGE 解锁数量
        "next_unlock": { // 下次解锁信息
          "date": 1764720000000, // 解锁时间
          "next_unlock_token_amount": "216580" // 解锁数量
        },
        "unlocked_token_amount": "866320", // 已解锁数量
        "tge_unlock_percent": 0, // TGE 解锁比例
        "vesting_duration_value": 3, // 锁仓时长数值
        "vesting_duration_type": "year", // 锁仓时长单位
        "allocation_of_supply": 23.8, // 占总供应比例
        "unlock_frequency_type": "day", // 解锁频率类型
        "name": "Core Contributors", // 分配名称
        "unlock_type": "linear", // 解锁方式
        "token_amount": "238000000", // 代币数量
        "unlock_frequency_value": 1 // 解锁频率数值
      },
      {
        "is_untracked": true, // 是否未追踪
        "allocation_of_supply": 6, // 占总供应比例
        "name": "Hyper Foundation", // 分配名称
        "token_amount": "60000000" // 代币数量
      },
      {
        "is_untracked": true, // 是否未追踪
        "allocation_of_supply": 0.3, // 占总供应比例
        "name": "Community Grants", // 分配名称
        "token_amount": "3000000" // 代币数量
      },
      {
        "is_untracked": false, // 是否未追踪
        "allocation_of_supply": 0.012, // 占总供应比例
        "name": "HIP-2", // 分配名称
        "unlock_type": "nonlinear", // 解锁方式
        "token_amount": "120000", // 代币数量
        "tge_unlocked_token_amount": "120000", // TGE 解锁数量
        "unlocked_token_amount": "120000", // 已解锁数量
        "tge_unlock_percent": 100 // TGE 解锁比例
      }
    ],
    "fully_diluted_valuation": 34587740013.671524, // 全稀释估值
    "name": "Hyperliquid", // 项目名称
    "max_supply": 1000000000, // 最大供应量
    "chart": [ // 图表数据
      {
        "date": 1732838400000, // 图表时间
        "allocations": [ // 图表分配
          {
            "name": "Genesis Distribution", // 名称
            "unlocked_percent": 31, // 解锁比例
            "token_amount": "310000000", // 代币数量
            "unlocked_token_amount": "310000000" // 解锁数量
          },
          {
            "name": "Core Contributors", // 名称
            "unlocked_percent": 0, // 解锁比例
            "token_amount": "238000000", // 代币数量
            "unlocked_token_amount": "0" // 解锁数量
          },
          {
            "name": "HIP-2", // 名称
            "unlocked_percent": 0.012, // 解锁比例
            "token_amount": "120000", // 代币数量
            "unlocked_token_amount": "120000" // 解锁数量
          }
        ],
        "is_tge": true, // 是否为 TGE
        "unlocked_percent": 31.012, // 总解锁比例
        "unlocked_token_amount": "310120000" // 总解锁数量
      }
    ],
    "untracked_allocation_names": [ // 未追踪分配名称列表
      "Community Grants",
      "Future Emissions & Community Rewards",
      "Hyper Foundation"
    ]
  }
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                                 |
| ------ | ------ | --- | -------------------------------------------------- |
| symbol | string | YES | 交易代币（例如 HYPE）。可通过 “token-unlock-list” 接口获取支持的代币列表。 |

