# IDeviceNFT 接口文档

## 方法: mint

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| to | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenId | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.mint(to, tokenId)   ## DApp
IMPCGroupFeignService.mint(to, tokenId)  ## java
```

## 方法: burn

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
c.burn(tokenId)   ## DApp
IMPCGroupFeignService.burn(tokenId)  ## java
```

## 方法: ownerOf

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenId | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| address | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**示例**:
```
c.ownerOf(tokenId)   ## DApp
IMPCGroupFeignService.ownerOf(tokenId)  ## java
```

## 事件: Minted

| 参数 | 类型 | 示例值 |
|------|------|---------|
| to | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenId | uint256 indexed | 123 |

**示例**:
```
c.onMinted(txReceipt)   ## DApp
IMPCGroupFeignService.onMinted(txReceipt)  ## java
```

## 事件: Burned

| 参数 | 类型 | 示例值 |
|------|------|---------|
| tokenId | uint256 indexed | 123 |

**示例**:
```
c.onBurned(txReceipt)   ## DApp
IMPCGroupFeignService.onBurned(txReceipt)  ## java
```

