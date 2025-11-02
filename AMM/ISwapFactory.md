# ISwapFactory 接口文档

## 方法: createPair

**功能说明**: 创建一个新的交易对（Pool）

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenA | address | 交易对代币 A 地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenB | address | 交易对代币 B 地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| fee | uint24 | 手续费档位（单位：ppm，如 3000 = 0.3%） | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.createPair(tokenA, tokenB, fee)   ## DApp
IMPCGroupFeignService.createPair(tokenA, tokenB, fee)  ## java
```

## 方法: getPair

**功能说明**: 查询交易对合约地址

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| tokenA | address | 代币 A 地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| tokenB | address | 代币 B 地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| fee | uint24 | 手续费档位 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| pair | address | 交易对地址，如果不存在返回 0 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**示例**:
```
c.getPair(tokenA, tokenB, fee)   ## DApp
IMPCGroupFeignService.getPair(tokenA, tokenB, fee)  ## java
```

## 方法: setFeeTier

**功能说明**: 启用或禁用某个费率档

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| fee | uint24 | 手续费档位 | 123 |
| enabled | bool | 是否启用 | true |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.setFeeTier(fee, enabled)   ## DApp
IMPCGroupFeignService.setFeeTier(fee, enabled)  ## java
```

