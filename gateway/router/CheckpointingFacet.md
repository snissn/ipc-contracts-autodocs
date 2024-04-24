# Solidity API

## CheckpointingFacet

### commitCheckpoint

```solidity
function commitCheckpoint(struct BottomUpCheckpoint checkpoint) external
```

submit a verified checkpoint in the gateway to trigger side-effects.

_this method is called by the corresponding subnet actor.
    Called from a subnet actor if the checkpoint is cryptographically valid._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| checkpoint | struct BottomUpCheckpoint | The bottom-up checkpoint to be committed. |

### createBottomUpCheckpoint

```solidity
function createBottomUpCheckpoint(struct BottomUpCheckpoint checkpoint, bytes32 membershipRootHash, uint256 membershipWeight) external
```

creates a new bottom-up checkpoint

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| checkpoint | struct BottomUpCheckpoint | - a bottom-up checkpoint |
| membershipRootHash | bytes32 | - a root hash of the Merkle tree built from the validator public keys and their weight |
| membershipWeight | uint256 | - the total weight of the membership |

### pruneBottomUpCheckpoints

```solidity
function pruneBottomUpCheckpoints(uint256 newRetentionHeight) external
```

Set a new checkpoint retention height and garbage collect all checkpoints in range [`retentionHeight`, `newRetentionHeight`)

_`retentionHeight` is the height of the first incomplete checkpointswe must keep to implement checkpointing.
All checkpoints with a height less than `retentionHeight` are removed from the history, assuming they are committed to the parent._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| newRetentionHeight | uint256 | - the height of the oldest checkpoint to keep |

### addCheckpointSignature

```solidity
function addCheckpointSignature(uint256 height, bytes32[] membershipProof, uint256 weight, bytes signature) external
```

checks whether the provided checkpoint signature for the block at height `height` is valid and accumulates that it

_If adding the signature leads to reaching the threshold, then the checkpoint is removed from `incompleteCheckpoints`_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| height | uint256 | - the height of the block in the checkpoint |
| membershipProof | bytes32[] | - a Merkle proof that the validator was in the membership at height `height` with weight `weight` |
| weight | uint256 | - the weight of the validator |
| signature | bytes | - the signature of the checkpoint |

### execBottomUpMsgs

```solidity
function execBottomUpMsgs(struct IpcEnvelope[] msgs, struct Subnet subnet) internal
```

submit a batch of cross-net messages for execution.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| msgs | struct IpcEnvelope[] | The batch of bottom-up cross-network messages to be executed. |
| subnet | struct Subnet |  |

