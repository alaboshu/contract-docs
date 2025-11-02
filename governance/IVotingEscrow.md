# IVotingEscrow 接口文档

## 方法: lock

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| amount | uint256 |  | 123 |
| unlockTime | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.lock(amount, unlockTime)   ## DApp
IMPCGroupFeignService.lock(amount, unlockTime)  ## java
```

## 方法: unlock

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| amount | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.unlock(amount)   ## DApp
IMPCGroupFeignService.unlock(amount)  ## java
```

## 方法: delegate

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
c.delegate(delegatee)   ## DApp
IMPCGroupFeignService.delegate(delegatee)  ## java
```

## 方法: undelegate

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.undelegate()   ## DApp
IMPCGroupFeignService.undelegate()  ## java
```

## 方法: getVotingPower

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| user | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| weight | uint256 |  | 123 |

**示例**:
```
c.getVotingPower(user)   ## DApp
IMPCGroupFeignService.getVotingPower(user)  ## java
```

## 方法: getPriorVotes

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| account | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| votes | uint256 |  | 123 |

**示例**:
```
c.getPriorVotes(account)   ## DApp
IMPCGroupFeignService.getPriorVotes(account)  ## java
```

## 方法: getTotalWeight

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.getTotalWeight()   ## DApp
IMPCGroupFeignService.getTotalWeight()  ## java
```

