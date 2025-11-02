# IPoolRevenueVault 接口文档

## 方法: deposit

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| pool | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.deposit(pool, amount)   ## DApp
IMPCGroupFeignService.deposit(pool, amount)  ## java
```

## 方法: withdraw

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| to | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.withdraw(to, amount)   ## DApp
IMPCGroupFeignService.withdraw(to, amount)  ## java
```

## 方法: getVaultBalance

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| pool | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.getVaultBalance(pool)   ## DApp
IMPCGroupFeignService.getVaultBalance(pool)  ## java
```

## 事件: VaultDeposit

| 参数 | 类型 | 示例值 |
|------|------|---------|
| pool | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 123 |

**示例**:
```
c.onVaultDeposit(txReceipt)   ## DApp
IMPCGroupFeignService.onVaultDeposit(txReceipt)  ## java
```

## 事件: VaultWithdraw

| 参数 | 类型 | 示例值 |
|------|------|---------|
| to | address indexed | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 | 123 |

**示例**:
```
c.onVaultWithdraw(txReceipt)   ## DApp
IMPCGroupFeignService.onVaultWithdraw(txReceipt)  ## java
```

