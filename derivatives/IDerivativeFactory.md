# IDerivativeFactory 接口文档

## 方法: createOption

**功能说明**: 创建期权合约

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| poolId | string calldata | 设备池ID | "示例文本" |
| strike | uint256 | 行权价格 | 123 |
| expiry | uint256 | 到期时间（timestamp） | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.createOption(poolId, strike, expiry)   ## DApp
IMPCGroupFeignService.createOption(poolId, strike, expiry)  ## java
```

## 方法: setUnderlying

**功能说明**: 绑定标的资产（设备池代币）

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| poolToken | address | 标的资产地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.setUnderlying(poolToken)   ## DApp
IMPCGroupFeignService.setUnderlying(poolToken)  ## java
```

