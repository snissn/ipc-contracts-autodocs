# Solidity API

## GatewayGetterFacet

### s

```solidity
struct GatewayActorStorage s
```

### getCommitSha

```solidity
function getCommitSha() external view returns (bytes32)
```

Returns code commit SHA where this contract is from.

### bottomUpNonce

```solidity
function bottomUpNonce() external view returns (uint64)
```

Returns the current nonce for bottom-up message processing.

### totalSubnets

```solidity
function totalSubnets() external view returns (uint64)
```

Returns the total number of the registered subnets.

### maxMsgsPerBottomUpBatch

```solidity
function maxMsgsPerBottomUpBatch() external view returns (uint64)
```

Returns the maximum number of messages per bottom-up batch.

### bottomUpCheckPeriod

```solidity
function bottomUpCheckPeriod() external view returns (uint256)
```

Returns the period for bottom-up checkpointing.

### getNetworkName

```solidity
function getNetworkName() external view returns (struct SubnetID)
```

Returns the subnet identifier of the network.

### bottomUpCheckpoint

```solidity
function bottomUpCheckpoint(uint256 e) external view returns (struct BottomUpCheckpoint)
```

Returns a specific bottom-up checkpoint based on an epoch number.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| e | uint256 | The epoch number of the checkpoint. |

### bottomUpMsgBatch

```solidity
function bottomUpMsgBatch(uint256 e) external view returns (struct BottomUpMsgBatch)
```

Returns a specific bottom-up message batch based on an index.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| e | uint256 | The epoch number of the batch. |

### getParentFinality

```solidity
function getParentFinality(uint256 blockNumber) external view returns (struct ParentFinality)
```

Returns the parent chain finality information for a given block number.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| blockNumber | uint256 | The block number for which to retrieve parent-finality information. |

### getLatestParentFinality

```solidity
function getLatestParentFinality() external view returns (struct ParentFinality)
```

Gets the most recent parent-finality information from the parent.

### getSubnet

```solidity
function getSubnet(struct SubnetID subnetId) external view returns (bool, struct Subnet)
```

Returns the subnet with the given id.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | the id of the subnet. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | found whether the subnet exists. |
| [1] | struct Subnet | subnet -  the subnet struct. |

### subnets

```solidity
function subnets(bytes32 h) external view returns (struct Subnet subnet)
```

Returns information about a specific subnet using its hash identifier.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| h | bytes32 | The hash identifier of the subnet to be queried. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnet | struct Subnet | The subnet information corresponding to the given hash. |

### getSubnetTopDownMsgsLength

```solidity
function getSubnetTopDownMsgsLength(struct SubnetID subnetId) external view returns (uint256)
```

Returns the length of the top-down message queue for a specified subnet.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | The identifier of the subnet for which the message queue length is queried. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | The current length of the top-down message queue, indicated by the subnet's top-down nonce. |

### getTopDownNonce

```solidity
function getTopDownNonce(struct SubnetID subnetId) external view returns (bool, uint64)
```

Returns the current applied top-down nonce for a specified subnet, indicating whether it's registered.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | The identifier of the subnet for which the top-down nonce is queried. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | A tuple containing a boolean indicating if the subnet is registered and the current top-down nonce. |
| [1] | uint64 |  |

### getAppliedBottomUpNonce

```solidity
function getAppliedBottomUpNonce(struct SubnetID subnetId) external view returns (bool, uint64)
```

Returns the current applied bottom-up nonce for a specified subnet, indicating whether it's registered.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | The identifier of the subnet for which the bottom-up nonce is queried. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | A tuple containing a boolean indicating if the subnet is registered and the current applied bottom-up nonce. |
| [1] | uint64 |  |

### appliedTopDownNonce

```solidity
function appliedTopDownNonce() external view returns (uint64)
```

Returns the current applied top-down nonce of the gateway.

### postbox

```solidity
function postbox(bytes32 id) external view returns (struct IpcEnvelope storableMsg)
```

Returns the storable message and its wrapped status from the postbox by a given identifier.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| id | bytes32 | The unique identifier of the message in the postbox. |

### majorityPercentage

```solidity
function majorityPercentage() external view returns (uint64)
```

Returns the majority percentage required for certain consensus or decision-making processes.

### listSubnets

```solidity
function listSubnets() external view returns (struct Subnet[])
```

Returns the list of registered subnets.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct Subnet[] | The list of the registered subnets. |

### getSubnetKeys

```solidity
function getSubnetKeys() external view returns (bytes32[])
```

Returns the subnet keys.

### getLastMembership

```solidity
function getLastMembership() external view returns (struct Membership)
```

Returns the last membership received from the parent.

### getLastConfigurationNumber

```solidity
function getLastConfigurationNumber() external view returns (uint64)
```

Returns the last configuration number received from the parent.

### getCurrentMembership

```solidity
function getCurrentMembership() external view returns (struct Membership)
```

Returns the current membership.

### getCurrentConfigurationNumber

```solidity
function getCurrentConfigurationNumber() external view returns (uint64)
```

Returns the current configuration number.

### getCheckpointInfo

```solidity
function getCheckpointInfo(uint256 h) external view returns (struct QuorumInfo)
```

Returns quorum information for a specific checkpoint based on its height.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| h | uint256 | The block height of the checkpoint. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct QuorumInfo | Quorum information associated with the given checkpoint height. |

### getCheckpointCurrentWeight

```solidity
function getCheckpointCurrentWeight(uint256 h) external view returns (uint256)
```

Returns the checkpoint current weight corresponding to the block height.

### getIncompleteCheckpointHeights

```solidity
function getIncompleteCheckpointHeights() external view returns (uint256[])
```

Returns the incomplete checkpoint heights.

### getIncompleteCheckpoints

```solidity
function getIncompleteCheckpoints() external view returns (struct BottomUpCheckpoint[])
```

Returns the incomplete checkpoints.

### getCheckpointRetentionHeight

```solidity
function getCheckpointRetentionHeight() external view returns (uint256)
```

Returns the bottom-up checkpoint retention index.

### getQuorumThreshold

```solidity
function getQuorumThreshold(uint256 totalWeight) external view returns (uint256)
```

Returns the threshold required for quorum in this subnet,
        based on the configured majority percentage and the total weight of the validators.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| totalWeight | uint256 | The total weight to consider for calculating the quorum threshold. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | The quorum threshold derived from the total weight and majority percentage. |

### getCheckpointSignatureBundle

```solidity
function getCheckpointSignatureBundle(uint256 h) external view returns (struct BottomUpCheckpoint ch, struct QuorumInfo info, address[] signatories, bytes[] signatures)
```

Retrieves a bundle of information and signatures for a specified bottom-up checkpoint.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| h | uint256 | The height of the checkpoint for which information is requested. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| ch | struct BottomUpCheckpoint | The checkpoint information at the specified height. |
| info | struct QuorumInfo | Quorum information related to the checkpoint. |
| signatories | address[] | An array of addresses of signatories who have signed the checkpoint. |
| signatures | bytes[] |  |

### getCurrentBottomUpCheckpoint

```solidity
function getCurrentBottomUpCheckpoint() external view returns (bool exists, uint256 epoch, struct BottomUpCheckpoint checkpoint)
```

Returns the current bottom-up checkpoint.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| exists | bool | - whether the checkpoint exists |
| epoch | uint256 | - the epoch of the checkpoint |
| checkpoint | struct BottomUpCheckpoint | - the checkpoint struct |

