# IDCAPlan 接口文档

## 方法: startDCAPlan

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.startDCAPlan(token, amount)   ## DApp
IMPCGroupFeignService.startDCAPlan(token, amount)  ## java
```

## 方法: executeDCA

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.executeDCA(token)   ## DApp
IMPCGroupFeignService.executeDCA(token)  ## java
```

