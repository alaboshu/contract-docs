# ISwapRouter 接口文档

## 结构体: ExactInputParams

| 字段 | 类型 | 示例值 |
|------|------|---------|
| tokenIn | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenOut | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| fee | uint24 | 123 |
| recipient | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amountIn | uint256 | 123 |
| amountOutMinimum | uint256 | 123 |

## 结构体: ExactOutputParams

| 字段 | 类型 | 示例值 |
|------|------|---------|
| tokenIn | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenOut | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| fee | uint24 | 123 |
| recipient | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amountOut | uint256 | 123 |
| amountInMaximum | uint256 | 123 |

## 方法: exactInput

**功能说明**: 通过路径精确输入执行交易

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| params | ExactInputParams calldata | ExactInputParams 参数 |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.exactInput(params)   ## DApp
IMPCGroupFeignService.exactInput(params)  ## java
```

## 方法: exactOutput

**功能说明**: 通过路径精确输出执行交易

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| params | ExactOutputParams calldata | ExactOutputParams 参数 |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.exactOutput(params)   ## DApp
IMPCGroupFeignService.exactOutput(params)  ## java
```

