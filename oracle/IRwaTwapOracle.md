# IRwaTwapOracle 接口文档

## 方法: consult

**功能说明**: 获取 TWAP 价格

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address | 资产地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amountIn | uint256 | 输入数量 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| amountOut | uint256 | TWAP 价格对应数量 | 123 |

**示例**:
```
c.consult(token, amountIn)   ## DApp
IMPCGroupFeignService.consult(token, amountIn)  ## java
```

