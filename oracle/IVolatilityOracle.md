# IVolatilityOracle 接口文档

## 方法: calculateVolatility

**功能说明**: 计算资产波动率

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| token | address | 资产地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| period | uint256 | 时间周期（秒） | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| volatility | uint256 | 波动率值 | 123 |

**示例**:
```
c.calculateVolatility(token, period)   ## DApp
IMPCGroupFeignService.calculateVolatility(token, period)  ## java
```

