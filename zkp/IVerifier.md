# IVerifier 接口文档

## 结构体: Proof

| 字段 | 类型 | 示例值 |
|------|------|---------|
| a | uint[2] | 123 |
| b | uint[2][2] | 123 |
| c | uint[2] | 123 |

## 方法: verify

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| input | uint[] memory |  | 123 |
| proof | Proof memory |  |  |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| uint | uint |  | 123 |

**示例**:
```
c.verify(input, proof)   ## DApp
IMPCGroupFeignService.verify(input, proof)  ## java
```

## 方法: verifyTx

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| proof | Proof memory |  |  |
| input | uint[1] memory |  | 123 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| bool | bool |  | true |

**示例**:
```
c.verifyTx(proof, input)   ## DApp
IMPCGroupFeignService.verifyTx(proof, input)  ## java
```

