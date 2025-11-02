# INftBasedVoting 接口文档

## 方法: voteOnPool

**功能说明**: 设备 NFT 治理投票

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| poolId | string calldata | 设备池ID | "示例文本" |
| option | uint256 | 投票选项编号 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.voteOnPool(poolId, option)   ## DApp
IMPCGroupFeignService.voteOnPool(poolId, option)  ## java
```

