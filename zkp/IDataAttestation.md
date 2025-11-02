# IDataAttestation 接口文档

## 方法: anchor

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| _root | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| _proofs | bytes32[] calldata |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.anchor(_root, _proofs)   ## DApp
IMPCGroupFeignService.anchor(_root, _proofs)  ## java
```

## 方法: verify

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| _root | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| _proofs | bytes32[] calldata |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| bool | bool |  | true |

**示例**:
```
c.verify(_root, _proofs)   ## DApp
IMPCGroupFeignService.verify(_root, _proofs)  ## java
```

## 方法: getBatch

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| _root | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | DataAttestation.Batch |  |  |

**示例**:
```
c.getBatch(_root)   ## DApp
IMPCGroupFeignService.getBatch(_root)  ## java
```

