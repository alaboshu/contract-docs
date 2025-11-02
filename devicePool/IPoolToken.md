# IPoolToken 接口文档

## 方法: name

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | string |  | "示例文本" |

**示例**:
```
c.name()   ## DApp
IMPCGroupFeignService.name()  ## java
```

## 方法: symbol

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | string |  | "示例文本" |

**示例**:
```
c.symbol()   ## DApp
IMPCGroupFeignService.symbol()  ## java
```

## 方法: totalSupply

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.totalSupply()   ## DApp
IMPCGroupFeignService.totalSupply()  ## java
```

## 方法: balanceOf

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| account | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint256 | uint256 |  | 123 |

**示例**:
```
c.balanceOf(account)   ## DApp
IMPCGroupFeignService.balanceOf(account)  ## java
```

## 方法: transfer

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| to | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| value | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.transfer(to, value)   ## DApp
IMPCGroupFeignService.transfer(to, value)  ## java
```

## 方法: transferFrom

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| from | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| to | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| value | uint256 |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.transferFrom(from, to, value)   ## DApp
IMPCGroupFeignService.transferFrom(from, to, value)  ## java
```

