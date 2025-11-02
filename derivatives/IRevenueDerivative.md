# IRevenueDerivative 接口文档

## 方法: exercise

**功能说明**: 行权获取收益

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| amount | uint256 | 行权数量 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.exercise(amount)   ## DApp
IMPCGroupFeignService.exercise(amount)  ## java
```

## 方法: settle

**功能说明**: 到期结算

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.settle()   ## DApp
IMPCGroupFeignService.settle()  ## java
```

