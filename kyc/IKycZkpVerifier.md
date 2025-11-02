# IKycZkpVerifier 接口文档

## 方法: verifyKycProof

**功能说明**: 验证 KYC 零知识证明

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| root | bytes32 | Merkle 树根 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| proof | bytes32[] calldata | Merkle 证明数组 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| valid | bool | 验证结果 | true |

**示例**:
```
c.verifyKycProof(root, proof)   ## DApp
IMPCGroupFeignService.verifyKycProof(root, proof)  ## java
```

