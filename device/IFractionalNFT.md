# IFractionalNFT 接口文档

## 方法: fractionalize

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenId | uint256 |  | 123 |
| shares | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.fractionalize(tokenId, shares)   ## DApp
IMPCGroupFeignService.fractionalize(tokenId, shares)  ## java
```

## 方法: defractionalize

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenId | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.defractionalize(tokenId)   ## DApp
IMPCGroupFeignService.defractionalize(tokenId)  ## java
```

## 方法: getShares

**功能说明**: Returns the shares associated with a specific token ID.

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenId | uint256 | The ID of the token to query. | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.getShares(tokenId)   ## DApp
IMPCGroupFeignService.getShares(tokenId)  ## java
```

## 事件: Fractionalized

| 参数 | 类型 | 示例值 |
|------|------|---------|
| tokenId | uint256 indexed | 123 |
| shares | uint256 | 123 |

**示例**:
```
c.onFractionalized(txReceipt)   ## DApp
IMPCGroupFeignService.onFractionalized(txReceipt)  ## java
```

## 事件: Defractionalized

| 参数 | 类型 | 示例值 |
|------|------|---------|
| tokenId | uint256 indexed | 123 |

**示例**:
```
c.onDefractionalized(txReceipt)   ## DApp
IMPCGroupFeignService.onDefractionalized(txReceipt)  ## java
```

