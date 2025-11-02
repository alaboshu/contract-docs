# IMPCRecovery 接口文档

## 事件: RecoveryRequested

发起恢复请求事件

| 参数 | 类型 | 示例值 |
|------|------|---------|
| recoveryId | bytes32 indexed | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| user | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| dataHash | bytes32 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**示例**:
```
c.onRecoveryRequested(txReceipt)   ## DApp
IMPCGroupFeignService.onRecoveryRequested(txReceipt)  ## java
```

## 事件: RecoveryVerified

恢复验证通过事件

| 参数 | 类型 | 示例值 |
|------|------|---------|
| recoveryId | bytes32 indexed | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| verifier | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**示例**:
```
c.onRecoveryVerified(txReceipt)   ## DApp
IMPCGroupFeignService.onRecoveryVerified(txReceipt)  ## java
```

## 事件: RecoveryCompleted

恢复完成事件

| 参数 | 类型 | 示例值 |
|------|------|---------|
| recoveryId | bytes32 indexed | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| user | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| newPublicKey | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**示例**:
```
c.onRecoveryCompleted(txReceipt)   ## DApp
IMPCGroupFeignService.onRecoveryCompleted(txReceipt)  ## java
```

## 方法: requestRecovery

**功能说明**: 创建一个新的恢复请求

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| recoveryId | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| dataHash | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.requestRecovery(recoveryId, dataHash)   ## DApp
IMPCGroupFeignService.requestRecovery(recoveryId, dataHash)  ## java
```

## 方法: markVerified

**功能说明**: 验证恢复请求（链下验证完成后调用）

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| recoveryId | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.markVerified(recoveryId)   ## DApp
IMPCGroupFeignService.markVerified(recoveryId)  ## java
```

## 方法: completeRecovery

**功能说明**: 完成恢复（更新用户公钥）

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| recoveryId | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| newPublicKey | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.completeRecovery(recoveryId, newPublicKey)   ## DApp
IMPCGroupFeignService.completeRecovery(recoveryId, newPublicKey)  ## java
```

## 方法: getRecoveryStatus

**功能说明**: 查询恢复状态

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| recoveryId | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint8 | uint8 |  | 123 |

**示例**:
```
c.getRecoveryStatus(recoveryId)   ## DApp
IMPCGroupFeignService.getRecoveryStatus(recoveryId)  ## java
```

