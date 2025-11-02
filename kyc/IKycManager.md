# IKycManager 接口文档

## 方法: registerUser

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| kycHash | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.registerUser(user, kycHash)   ## DApp
IMPCGroupFeignService.registerUser(user, kycHash)  ## java
```

## 方法: isCompliant

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| bool | bool |  | true |

**示例**:
```
c.isCompliant(user)   ## DApp
IMPCGroupFeignService.isCompliant(user)  ## java
```

## 方法: modifyWhitelist

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| op | bool |  | true |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.modifyWhitelist(user, op)   ## DApp
IMPCGroupFeignService.modifyWhitelist(user, op)  ## java
```

## 方法: enforceKyc

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.enforceKyc(user)   ## DApp
IMPCGroupFeignService.enforceKyc(user)  ## java
```

## 方法: modifyBlacklist

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| op | bool |  | true |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.modifyBlacklist(user, op)   ## DApp
IMPCGroupFeignService.modifyBlacklist(user, op)  ## java
```

