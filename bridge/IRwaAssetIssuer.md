# IRwaAssetIssuer 接口文档

## 方法: issueAsset

**功能说明**: 创建新的 RWA 资产

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| assetId | string calldata | 资产唯一标识 | "示例文本" |
| supply | uint256 | 总供应量 | 123 |
| metadata | string calldata | 资产元数据（JSON URI 等） | "示例文本" |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.issueAsset(assetId, supply, metadata)   ## DApp
IMPCGroupFeignService.issueAsset(assetId, supply, metadata)  ## java
```

## 方法: mintAsset

**功能说明**: 铸造资产代币

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| to | address | 接收地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 铸造数量 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.mintAsset(token, to, amount)   ## DApp
IMPCGroupFeignService.mintAsset(token, to, amount)  ## java
```

## 方法: getAssettoken

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| assetId | string calldata |  | "示例文本" |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| address | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**示例**:
```
c.getAssettoken(assetId)   ## DApp
IMPCGroupFeignService.getAssettoken(assetId)  ## java
```

