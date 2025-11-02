# IDelegationFractional 接口文档

## 方法: fractionalize

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
c.fractionalize(token, amount)   ## DApp
IMPCGroupFeignService.fractionalize(token, amount)  ## java
```

## 方法: defractionalize

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
c.defractionalize(token, amount)   ## DApp
IMPCGroupFeignService.defractionalize(token, amount)  ## java
```

## 方法: getFractionalizedAmount

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.getFractionalizedAmount(token)   ## DApp
IMPCGroupFeignService.getFractionalizedAmount(token)  ## java
```

## 事件: Fractionalized

| 参数 | 类型 | 示例值 |
|------|------|---------|
| owner | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| token | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 123 |

**示例**:
```
c.onFractionalized(txReceipt)   ## DApp
IMPCGroupFeignService.onFractionalized(txReceipt)  ## java
```

## 事件: Defractionalized

| 参数 | 类型 | 示例值 |
|------|------|---------|
| owner | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| token | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 123 |

**示例**:
```
c.onDefractionalized(txReceipt)   ## DApp
IMPCGroupFeignService.onDefractionalized(txReceipt)  ## java
```

