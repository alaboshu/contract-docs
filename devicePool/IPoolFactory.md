# IPoolFactory 接口文档

## 方法: setOracle

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| newOracle | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.setOracle(newOracle)   ## DApp
IMPCGroupFeignService.setOracle(newOracle)  ## java
```

