# IPoolPricingOracle 接口文档

## 方法: setPrice

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| poolToken | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| newPrice | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.setPrice(poolToken, newPrice)   ## DApp
IMPCGroupFeignService.setPrice(poolToken, newPrice)  ## java
```

## 方法: getPrice

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| poolToken | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.getPrice(poolToken)   ## DApp
IMPCGroupFeignService.getPrice(poolToken)  ## java
```

## 事件: PriceUpdated

| 参数 | 类型 | 示例值 |
|------|------|---------|
| poolToken | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| newPrice | uint256 | 123 |

**示例**:
```
c.onPriceUpdated(txReceipt)   ## DApp
IMPCGroupFeignService.onPriceUpdated(txReceipt)  ## java
```

