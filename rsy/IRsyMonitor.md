# IRsyMonitor 接口文档

## 方法: recordChainEvent

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| eventType | string memory |  | "示例文本" |
| eventHash | string memory |  | "示例文本" |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.recordChainEvent(eventType, eventHash)   ## DApp
IMPCGroupFeignService.recordChainEvent(eventType, eventHash)  ## java
```

## 方法: syncWallet

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| onchainBalance | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.syncWallet(user, onchainBalance)   ## DApp
IMPCGroupFeignService.syncWallet(user, onchainBalance)  ## java
```

## 方法: compareBalance

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| offchainBalance | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| bool | bool |  | true |

**示例**:
```
c.compareBalance(user, offchainBalance)   ## DApp
IMPCGroupFeignService.compareBalance(user, offchainBalance)  ## java
```

