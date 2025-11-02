# IFeeManager 接口文档

## 方法: setFeeRecipient

**功能说明**: 设置手续费接收方

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| recipient | address | 接收手续费地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.setFeeRecipient(recipient)   ## DApp
IMPCGroupFeignService.setFeeRecipient(recipient)  ## java
```

## 方法: distributeFees

**功能说明**: 分配手续费

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address | 代币地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 分配金额 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.distributeFees(token, amount)   ## DApp
IMPCGroupFeignService.distributeFees(token, amount)  ## java
```

