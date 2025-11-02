# IPoolRevenueDistribution 接口文档

## 方法: claimRevenue

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.claimRevenue()   ## DApp
IMPCGroupFeignService.claimRevenue()  ## java
```

## 方法: pendingRevenue

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.pendingRevenue(user)   ## DApp
IMPCGroupFeignService.pendingRevenue(user)  ## java
```

## 事件: RevenueDeposited

| 参数 | 类型 | 示例值 |
|------|------|---------|
| from | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 123 |

**示例**:
```
c.onRevenueDeposited(txReceipt)   ## DApp
IMPCGroupFeignService.onRevenueDeposited(txReceipt)  ## java
```

## 事件: RevenueClaimed

| 参数 | 类型 | 示例值 |
|------|------|---------|
| user | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 123 |

**示例**:
```
c.onRevenueClaimed(txReceipt)   ## DApp
IMPCGroupFeignService.onRevenueClaimed(txReceipt)  ## java
```

