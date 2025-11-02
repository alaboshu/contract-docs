# ITokenSwap 接口文档

## 方法: getQuoteWithTokenIn

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenIn | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenOut | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amountIn | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.getQuoteWithTokenIn(tokenIn, tokenOut, amountIn)   ## DApp
IMPCGroupFeignService.getQuoteWithTokenIn(tokenIn, tokenOut, amountIn)  ## java
```

## 方法: getQuoteWithTokenOut

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenIn | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenOut | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amountOut | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.getQuoteWithTokenOut(tokenIn, tokenOut, amountOut)   ## DApp
IMPCGroupFeignService.getQuoteWithTokenOut(tokenIn, tokenOut, amountOut)  ## java
```

## 方法: swapExactInputSingle

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenIn | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenOut | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amountIn | uint256 |  | 123 |
| recipient | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.swapExactInputSingle(tokenIn, tokenOut, amountIn, recipient)   ## DApp
IMPCGroupFeignService.swapExactInputSingle(tokenIn, tokenOut, amountIn, recipient)  ## java
```

## 方法: swapExactOutputSingle

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenIn | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenOut | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amountOut | uint256 |  | 123 |
| recipient | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.swapExactOutputSingle(tokenIn, tokenOut, amountOut, recipient)   ## DApp
IMPCGroupFeignService.swapExactOutputSingle(tokenIn, tokenOut, amountOut, recipient)  ## java
```

