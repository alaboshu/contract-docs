# IPoolRegistry 接口文档

## 结构体: PoolInfo

| 字段 | 类型 | 示例值 |
|------|------|---------|
| poolId | string | "示例文本" |
| tokenAddress | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| revenueAddress | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| creator | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| createdAt | uint256 | 123 |

## 方法: registerPool

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| poolId | string memory |  | "示例文本" |
| tokenAddress | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| revenueAddress | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| creator | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.registerPool(poolId, tokenAddress, revenueAddress, creator)   ## DApp
IMPCGroupFeignService.registerPool(poolId, tokenAddress, revenueAddress, creator)  ## java
```

## 方法: poolExists

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| poolId | string memory |  | "示例文本" |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| bool | bool |  | true |

**示例**:
```
c.poolExists(poolId)   ## DApp
IMPCGroupFeignService.poolExists(poolId)  ## java
```

## 方法: getPool

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| poolId | string memory |  | "示例文本" |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | PoolInfo |  |  |

**示例**:
```
c.getPool(poolId)   ## DApp
IMPCGroupFeignService.getPool(poolId)  ## java
```

## 方法: getAllPoolIds

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | string[] |  | "示例文本" |

**示例**:
```
c.getAllPoolIds()   ## DApp
IMPCGroupFeignService.getAllPoolIds()  ## java
```

