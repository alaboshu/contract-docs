# ILightNodeBridge 接口文档

## 方法: send

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| assetId | string calldata |  | "示例文本" |
| _targetChainId | uint256 |  | 123 |
| to | address |  | 0xAbC1234567890abcdef1234567890ABCDEF1234 |
| amount | uint256 |  | 123 |
| payload | bytes calldata |  |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.send(assetId, _targetChainId, to, amount, payload)   ## DApp
IMPCGroupFeignService.send(assetId, _targetChainId, to, amount, payload)  ## java
```

## 方法: receive

**功能说明**: 验证并释放跨链消息

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| proof | bytes calldata | 跨链证明 |  |
| payload | bytes calldata | 消息负载 |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.receive(proof, payload)   ## DApp
IMPCGroupFeignService.receive(proof, payload)  ## java
```

