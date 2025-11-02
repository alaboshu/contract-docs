# IMPCWallet 接口文档

## 事件: Executed

| 参数 | 类型 | 示例值 |
|------|------|---------|
| to | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| value | uint256 | 123 |
| data | bytes |  |
| nonce | uint256 | 123 |
| txHash | bytes32 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**示例**:
```
c.onExecuted(txReceipt)   ## DApp
IMPCGroupFeignService.onExecuted(txReceipt)  ## java
```

## 事件: Received

| 参数 | 类型 | 示例值 |
|------|------|---------|
| from | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| value | uint256 | 123 |

**示例**:
```
c.onReceived(txReceipt)   ## DApp
IMPCGroupFeignService.onReceived(txReceipt)  ## java
```

## 事件: OwnerGroupChanged

| 参数 | 类型 | 示例值 |
|------|------|---------|
| oldGroup | bytes32 indexed | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| newGroup | bytes32 indexed | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**示例**:
```
c.onOwnerGroupChanged(txReceipt)   ## DApp
IMPCGroupFeignService.onOwnerGroupChanged(txReceipt)  ## java
```

## 方法: execute

**功能说明**: 执行一笔由 group 签名授权的交易

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| to | address | 目标地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| value | uint256 | 以 wei 为单位的 ETH 金额 | 123 |
| data | bytes calldata | 调用 calldata |  |
| nonce | uint256 | 防重放 nonce（由调用者与签名方约定） | 123 |
| sigs | bytes[] calldata | 签名数组（每个签名为标准 65 字节 r||s||v） |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.execute(to, value, data, nonce, sigs)   ## DApp
IMPCGroupFeignService.execute(to, value, data, nonce, sigs)  ## java
```

## 方法: changeOwnerGroup

**功能说明**: 更改该钱包关联的 groupId（仅 owner 可调用）

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| newGroup | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.changeOwnerGroup(newGroup)   ## DApp
IMPCGroupFeignService.changeOwnerGroup(newGroup)  ## java
```

