# IRwaLiquidityMining 接口文档

## 方法: stake

**功能说明**: 质押 LP NFT

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenId | uint256 | NFT ID | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.stake(tokenId)   ## DApp
IMPCGroupFeignService.stake(tokenId)  ## java
```

## 方法: unstake

**功能说明**: 解除质押

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenId | uint256 | NFT ID | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.unstake(tokenId)   ## DApp
IMPCGroupFeignService.unstake(tokenId)  ## java
```

## 方法: claimReward

**功能说明**: 领取奖励

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address | 用户地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.claimReward(user)   ## DApp
IMPCGroupFeignService.claimReward(user)  ## java
```

