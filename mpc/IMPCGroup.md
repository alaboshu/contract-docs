# IMPCGroup 接口文档

## 结构体: MpcGroupInfo

| 字段 | 类型 | 示例值 |
|------|------|---------|
| groupId | bytes32 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| signers | address[] | ["0xAbC1234567890abcdef1234567890ABCDEF1234","0x1234567890abcdef1234567890abcdef12345678"] |
| threshold | uint256 | 123 |

## 事件: GroupRegistered

注册新签名组

| 参数 | 类型 | 示例值 |
|------|------|---------|
| groupId | bytes32 indexed | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**示例**:
```
c.onGroupRegistered(txReceipt)   ## DApp
IMPCGroupFeignService.onGroupRegistered(txReceipt)  ## java
```

## 事件: GroupUpdated

更新组成员或门限

| 参数 | 类型 | 示例值 |
|------|------|---------|
| groupId | bytes32 indexed | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**示例**:
```
c.onGroupUpdated(txReceipt)   ## DApp
IMPCGroupFeignService.onGroupUpdated(txReceipt)  ## java
```

## 事件: WalletCreated

钱包创建完成

| 参数 | 类型 | 示例值 |
|------|------|---------|
| groupId | bytes32 indexed | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| walletAddress | address | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**示例**:
```
c.onWalletCreated(txReceipt)   ## DApp
IMPCGroupFeignService.onWalletCreated(txReceipt)  ## java
```

## 方法: registerGroup

**功能说明**: 注册一个新的 MPC 签名组

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| groupId | bytes32 | 组唯一标识 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| signers | address[] calldata | 签名者列表 | ["0xAbC1234567890abcdef1234567890ABCDEF1234","0x1234567890abcdef1234567890abcdef12345678"] |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.registerGroup(groupId, signers)   ## DApp
IMPCGroupFeignService.registerGroup(groupId, signers)  ## java
```

## 方法: updateGroup

**功能说明**: 更新已有 MPC 签名组的信息（签名者或门限）

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| groupId | bytes32 | 组唯一标识 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| signers | address[] calldata | 新的签名者列表 | ["0xAbC1234567890abcdef1234567890ABCDEF1234","0x1234567890abcdef1234567890abcdef12345678"] |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.updateGroup(groupId, signers)   ## DApp
IMPCGroupFeignService.updateGroup(groupId, signers)  ## java
```

## 方法: createWallet

**功能说明**: 为指定组创建 MPC 钱包

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| groupId | bytes32 | 组唯一标识 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| txReceipt | TransactionReceipt | 交易回执对象 | {txHash: "...", status: true} |

**示例**:
```
c.createWallet(groupId)   ## DApp
IMPCGroupFeignService.createWallet(groupId)  ## java
```

## 方法: getGroup

**功能说明**: 获取单个组的详细信息（展开字段）

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| groupId | bytes32 | 组唯一标识 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| groupId_ | bytes32 | 组ID | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| memory | address[] |  | ["0xAbC1234567890abcdef1234567890ABCDEF1234","0x1234567890abcdef1234567890abcdef12345678"] |
| threshold_ | uint256 | 门限值 | 123 |

**示例**:
```
c.getGroup(groupId)   ## DApp
IMPCGroupFeignService.getGroup(groupId)  ## java
```

## 方法: verifyWalletInGroup

**功能说明**: 验证钱包是否属于指定组

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| groupId | bytes32 | 组唯一标识 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |
| walletAddress | address | 钱包地址 | 0xAbC1234567890abcdef1234567890ABCDEF1234 |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| isValid | bool | 如果钱包存在并且属于该组，返回 true，否则 false | true |

**示例**:
```
c.verifyWalletInGroup(groupId, walletAddress)   ## DApp
IMPCGroupFeignService.verifyWalletInGroup(groupId, walletAddress)  ## java
```

## 方法: getGroupWallets

**功能说明**: 获取某个组对应的所有钱包地址

**参数**:

| 参数 | 类型 | 描述 | 示例值 |
|------|------|------|---------|
| groupId | bytes32 | 组唯一标识 | 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef |

**返回值**:

| 返回值 | 类型 | 描述 | 示例值 |
|--------|------|------|---------|
| memory | address[] |  | ["0xAbC1234567890abcdef1234567890ABCDEF1234","0x1234567890abcdef1234567890abcdef12345678"] |

**示例**:
```
c.getGroupWallets(groupId)   ## DApp
IMPCGroupFeignService.getGroupWallets(groupId)  ## java
```

