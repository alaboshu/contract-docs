# ICrossChainOracle 接口文档

## 方法: syncPriceFromChain

**功能说明**: 同步外链价格

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| chainId | uint256 | 链ID | 123 |
| asset | address | 资产地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.syncPriceFromChain(chainId, asset)   ## DApp
IMPCGroupFeignService.syncPriceFromChain(chainId, asset)  ## java
```

