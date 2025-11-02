# IRwaLPToken 接口文档

## 结构体: Position

| 字段 | 类型 | 示例值 |
|------|------|---------|
| pool | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tickLower | int24 | 123 |
| tickUpper | int24 | 123 |
| liquidity | uint128 | 123 |
| feeGrowthInsideLastX128 | uint256 | 123 |

## 方法: mintPosition

**功能说明**: 铸造新的 LP NFT

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| owner | address | NFT 拥有者 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| position | Position calldata | 头寸信息 |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.mintPosition(owner, position)   ## DApp
IMPCGroupFeignService.mintPosition(owner, position)  ## java
```

## 方法: burnPosition

**功能说明**: 销毁 NFT

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
c.burnPosition(tokenId)   ## DApp
IMPCGroupFeignService.burnPosition(tokenId)  ## java
```

## 方法: getPosition

**功能说明**: 查询 NFT 头寸信息

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenId | uint256 | NFT ID | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | Position |  |  |

**示例**:
```
c.getPosition(tokenId)   ## DApp
IMPCGroupFeignService.getPosition(tokenId)  ## java
```

