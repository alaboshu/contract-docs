# IDelegationDevice 接口文档

## 方法: delegate

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| delegatee | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.delegate(delegatee, amount)   ## DApp
IMPCGroupFeignService.delegate(delegatee, amount)  ## java
```

## 方法: undelegate

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| delegatee | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.undelegate(delegatee)   ## DApp
IMPCGroupFeignService.undelegate(delegatee)  ## java
```

## 方法: getDelegatedAmount

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| delegatee | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.getDelegatedAmount(delegatee)   ## DApp
IMPCGroupFeignService.getDelegatedAmount(delegatee)  ## java
```

## 事件: Delegated

| 参数 | 类型 | 示例值 |
|------|------|---------|
| delegator | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| delegatee | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 123 |

**示例**:
```
c.onDelegated(txReceipt)   ## DApp
IMPCGroupFeignService.onDelegated(txReceipt)  ## java
```

## 事件: Undelegated

| 参数 | 类型 | 示例值 |
|------|------|---------|
| delegator | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| delegatee | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**示例**:
```
c.onUndelegated(txReceipt)   ## DApp
IMPCGroupFeignService.onUndelegated(txReceipt)  ## java
```

