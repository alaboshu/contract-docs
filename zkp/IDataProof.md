# IDataProof 接口文档

## 方法: storeData

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| cid | string memory |  | "示例文本" |
| merkleRoot | bytes32 |  | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.storeData(cid, merkleRoot)   ## DApp
IMPCGroupFeignService.storeData(cid, merkleRoot)  ## java
```

## 方法: verifyData

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| input | uint[1] memory |  | 123 |
| proof | Verifier.Proof memory |  |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| bool | bool |  | true |

**示例**:
```
c.verifyData(input, proof)   ## DApp
IMPCGroupFeignService.verifyData(input, proof)  ## java
```

