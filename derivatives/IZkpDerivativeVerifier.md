# IZkpDerivativeVerifier 接口文档

## 方法: verifyYieldProof

**功能说明**: 验证收益真实性

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| root | bytes32 | Merkle 根 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| proof | bytes32[] calldata | ZKP 证明数组 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| amount | uint256 | 收益数值 | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| bool | bool |  | true |

**示例**:
```
c.verifyYieldProof(root, proof, amount)   ## DApp
IMPCGroupFeignService.verifyYieldProof(root, proof, amount)  ## java
```

