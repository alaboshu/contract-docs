# IWrappedAsset 接口文档

## 方法: wrap

**功能说明**: 封装远程链资产

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| remoteAssetId | bytes32 | 远程资产ID | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| amount | uint256 | 封装数量 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.wrap(remoteAssetId, amount)   ## DApp
IMPCGroupFeignService.wrap(remoteAssetId, amount)  ## java
```

## 方法: unwrap

**功能说明**: 解封跨链资产

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| remoteAssetId | bytes32 | 远程资产ID | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| amount | uint256 | 解封数量 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.unwrap(remoteAssetId, amount)   ## DApp
IMPCGroupFeignService.unwrap(remoteAssetId, amount)  ## java
```

## 方法: getReceiveAssetId

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| symbol | string calldata |  | "示例文本" |
| token | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| bytes32 | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**示例**:
```
c.getReceiveAssetId(symbol, token)   ## DApp
IMPCGroupFeignService.getReceiveAssetId(symbol, token)  ## java
```

