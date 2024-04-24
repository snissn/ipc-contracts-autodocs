# Solidity API

## LibGateway

### MembershipUpdated

```solidity
event MembershipUpdated(struct Membership)
```

### NewTopDownMessage

```solidity
event NewTopDownMessage(address subnet, struct IpcEnvelope message)
```

_subnet refers to the next "down" subnet that the `envelope.message.to` should be forwarded to._

### NewBottomUpMsgBatch

```solidity
event NewBottomUpMsgBatch(uint256 epoch)
```

_event emitted when there is a new bottom-up message batch to be signed._

### getCurrentBottomUpCheckpoint

```solidity
function getCurrentBottomUpCheckpoint() internal view returns (bool exists, uint256 epoch, struct BottomUpCheckpoint checkpoint)
```

returns the current bottom-up checkpoint

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| exists | bool | - whether the checkpoint exists |
| epoch | uint256 | - the epoch of the checkpoint |
| checkpoint | struct BottomUpCheckpoint | - the checkpoint struct |

### getBottomUpCheckpoint

```solidity
function getBottomUpCheckpoint(uint256 epoch) internal view returns (bool exists, struct BottomUpCheckpoint checkpoint)
```

returns the bottom-up checkpoint

### getBottomUpMsgBatch

```solidity
function getBottomUpMsgBatch(uint256 epoch) internal view returns (bool exists, struct BottomUpMsgBatch batch)
```

returns the bottom-up batch

### bottomUpCheckpointExists

```solidity
function bottomUpCheckpointExists(uint256 epoch) internal view returns (bool)
```

checks if the bottom-up checkpoint already exists at the target epoch

### bottomUpBatchMsgsExists

```solidity
function bottomUpBatchMsgsExists(uint256 epoch) internal view returns (bool)
```

checks if the bottom-up checkpoint already exists at the target epoch

### storeBottomUpCheckpoint

```solidity
function storeBottomUpCheckpoint(struct BottomUpCheckpoint checkpoint) internal
```

stores checkpoint

### storeBottomUpMsgBatch

```solidity
function storeBottomUpMsgBatch(struct BottomUpMsgBatch batch) internal
```

stores bottom-up batch

### getParentFinality

```solidity
function getParentFinality(uint256 blockNumber) internal view returns (struct ParentFinality)
```

obtain the ipc parent finality at certain block number

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| blockNumber | uint256 | - the block number to obtain the finality |

### getLatestParentFinality

```solidity
function getLatestParentFinality() internal view returns (struct ParentFinality)
```

obtain the latest committed ipc parent finality

### commitParentFinality

```solidity
function commitParentFinality(struct ParentFinality finality) internal returns (struct ParentFinality lastFinality)
```

commit the ipc parent finality into storage

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| finality | struct ParentFinality | - the finality to be committed |

### updateMembership

```solidity
function updateMembership(struct Membership membership) internal
```

set the next membership

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| membership | struct Membership | - new membership |

### membershipTotalWeight

```solidity
function membershipTotalWeight(struct Membership self) internal pure returns (uint256)
```

_- Computes total weight for a specific membership_

### membershipEqual

```solidity
function membershipEqual(struct Membership mb1, struct Membership mb2) internal pure returns (bool)
```

_compares two memberships and returns true if they are equal_

### commitTopDownMsg

```solidity
function commitTopDownMsg(struct IpcEnvelope crossMessage) internal
```

commit topdown messages for their execution in the subnet. Adds the message to the subnet struct for future execution

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| crossMessage | struct IpcEnvelope | - the cross message to be committed |

### commitBottomUpMsg

```solidity
function commitBottomUpMsg(struct IpcEnvelope crossMessage) internal
```

Commits a new cross-net message to a message batch for execution

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| crossMessage | struct IpcEnvelope | - the cross message to be committed |

### getSubnet

```solidity
function getSubnet(address actor) internal view returns (bool found, struct Subnet subnet)
```

returns the subnet created by a validator

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | address | the validator that created the subnet |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| found | bool | whether the subnet exists |
| subnet | struct Subnet | -  the subnet struct |

### getSubnet

```solidity
function getSubnet(struct SubnetID subnetId) internal view returns (bool found, struct Subnet subnet)
```

returns the subnet with the given id

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | the id of the subnet |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| found | bool | whether the subnet exists |
| subnet | struct Subnet | -  the subnet struct |

### getNextEpoch

```solidity
function getNextEpoch(uint256 blockNumber, uint256 checkPeriod) internal pure returns (uint256)
```

method that gives the epoch for a given block number and checkpoint period

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | epoch - the epoch for the given block number and checkpoint period |

### applyMessages

```solidity
function applyMessages(struct SubnetID arrivingFrom, struct IpcEnvelope[] crossMsgs) internal
```

applies a cross-net messages coming from some other subnet.
The forwarder argument determines the previous subnet that submitted the checkpoint triggering the cross-net message execution.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| arrivingFrom | struct SubnetID | - the immediate subnet from which this message is arriving |
| crossMsgs | struct IpcEnvelope[] | - the cross-net messages to apply |

### applyMsg

```solidity
function applyMsg(struct SubnetID arrivingFrom, struct IpcEnvelope crossMsg) internal
```

executes a cross message if its destination is the current network, otherwise adds it to the postbox to be propagated further
This function assumes that the relevant funds have been already minted or burnt
when the top-down or bottom-up messages have been queued for execution.
This function is not expected to revert. If a controlled failure happens, a new
cross-message receipt is propagated for execution to inform the sending contract.
`Call` cross-messages also trigger receipts if they are successful.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| arrivingFrom | struct SubnetID | - the immediate subnet from which this message is arriving |
| crossMsg | struct IpcEnvelope | - the cross message to be executed |

### executeCrossMsg

```solidity
function executeCrossMsg(struct IpcEnvelope crossMsg, struct SupplySource supplySource) internal returns (bool success, bytes result)
```

_Execute the cross message using low level `call` method. This way ipc will
     catch contract revert messages as well. We need this because in `CrossMsgHelper.execute`
     there are `require` and `revert` calls, without reflexive call, the execution will
     revert and block the checkpoint submission process._

### sendReceipt

```solidity
function sendReceipt(struct IpcEnvelope original, enum OutcomeType outcomeType, bytes ret) internal
```

Sends a receipt from the execution of a cross-message.
Only `Call` messages trigger a receipt. Transfer messages should be directly
handled by the peer client to return the funds to the from address in the
failing network.
(we could optionally trigger a receipt from `Transfer`s to, but without
multi-level execution it would be adding unnecessary overhead).

### commitCrossMessage

```solidity
function commitCrossMessage(struct IpcEnvelope crossMessage) internal returns (bool shouldBurn)
```

Commit the cross message to storage.

_It also validates that destination subnet ID is not empty
     and not equal to the current network.
     This function assumes that the funds inside `value` have been
     conveniently minted or burnt already and the message is free to
     use them (see execBottomUpMsgBatch for reference).
 @param crossMessage The cross-network message to commit.
 @return shouldBurn A Boolean that indicates if the input amount should be burned._

### crossMsgSideEffects

```solidity
function crossMsgSideEffects(uint256 v, bool shouldBurn) internal
```

_Performs transaction side-effects from the commitment of a cross-net message. Like
burning funds when bottom-up messages are propagated._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| v | uint256 | - the value of the committed cross-net message |
| shouldBurn | bool | - flag if the message should burn funds |

### checkMsgLength

```solidity
function checkMsgLength(struct IpcEnvelope[] msgs) internal view
```

Checks the length of a message batch, ensuring it is in (0, maxMsgsPerBottomUpBatch).

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| msgs | struct IpcEnvelope[] | The batch of messages to check. |

