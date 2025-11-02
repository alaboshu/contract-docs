# IRwaDAO 接口文档

## 方法: castVote

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| proposalId | uint256 |  | 123 |
| support | bool |  | true |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.castVote(proposalId, support)   ## DApp
IMPCGroupFeignService.castVote(proposalId, support)  ## java
```

## 方法: execute

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| proposalId | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.execute(proposalId)   ## DApp
IMPCGroupFeignService.execute(proposalId)  ## java
```

