# IMultiSourceOracle 接口文档

## 方法: getPrice

**功能说明**: 获取指定资产综合报价

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| asset | address | 资产地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| price | uint256 | 综合报价（精度可定义为 1e18） | 123 |

**示例**:
```
c.getPrice(asset)   ## DApp
IMPCGroupFeignService.getPrice(asset)  ## java
```

## 方法: setSource

**功能说明**: 设置价格数据源

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| asset | address | 资产地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| oracle | address | 数据源地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.setSource(asset, oracle)   ## DApp
IMPCGroupFeignService.setSource(asset, oracle)  ## java
```

