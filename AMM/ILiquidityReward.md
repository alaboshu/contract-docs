# ILiquidityReward 接口文档

## 方法: addLiquidityReward

**功能说明**: 添加某个 NFT 的流动性奖励

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenId | uint256 | NFT ID | 123 |
| amount | uint256 | 奖励数量 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.addLiquidityReward(tokenId, amount)   ## DApp
IMPCGroupFeignService.addLiquidityReward(tokenId, amount)  ## java
```

## 方法: collectReward

**功能说明**: 收取 NFT 的流动性奖励

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
c.collectReward(tokenId)   ## DApp
IMPCGroupFeignService.collectReward(tokenId)  ## java
```

