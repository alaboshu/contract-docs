# ISwapPair 接口文档

## 方法: initialize

**功能说明**: 初始化交易对

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token0 | address | 代币0地址（通常按地址排序） | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| token1 | address | 代币1地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| fee | uint24 | 手续费档位 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.initialize(token0, token1, fee)   ## DApp
IMPCGroupFeignService.initialize(token0, token1, fee)  ## java
```

