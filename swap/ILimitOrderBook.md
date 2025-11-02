# ILimitOrderBook 接口文档

## 结构体: Order

| 字段 | 类型 | 示例值 |
|------|------|---------|
| user | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenIn | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenOut | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amountIn | uint256 | 123 |
| amountOutMin | uint256 | 123 |
| active | bool | true |
| executed | bool | true |
| amountOut | uint256 | 123 |
| createAt | uint256 | 123 |

## 方法: executeLimitOrder

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| orderId | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.executeLimitOrder(orderId)   ## DApp
IMPCGroupFeignService.executeLimitOrder(orderId)  ## java
```

## 方法: cancelLimitOrder

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| orderId | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.cancelLimitOrder(orderId)   ## DApp
IMPCGroupFeignService.cancelLimitOrder(orderId)  ## java
```

## 方法: getOrder

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| orderId | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | Order |  |  |

**示例**:
```
c.getOrder(orderId)   ## DApp
IMPCGroupFeignService.getOrder(orderId)  ## java
```

