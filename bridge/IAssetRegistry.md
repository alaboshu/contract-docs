# IAssetRegistry 接口文档

## 结构体: AssetInfo

| 字段 | 类型 | 示例值 |
|------|------|---------|
| issuer | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| assetId | string | "示例文本" |
| token | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| totalSupply// | uint256 | 123 |
| metadata | string | "示例文本" |
| exists | bool | true |

## 方法: registerAsset

**功能说明**: 注册资产

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address | 资产代币地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| info | AssetInfo calldata | 资产信息 |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.registerAsset(token, info)   ## DApp
IMPCGroupFeignService.registerAsset(token, info)  ## java
```

## 方法: getAssetInfo

**功能说明**: 获取资产信息

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address | 代币地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | AssetInfo |  |  |

**示例**:
```
c.getAssetInfo(token)   ## DApp
IMPCGroupFeignService.getAssetInfo(token)  ## java
```

