# Solidity API

## LibQuorum

### QuorumReached

```solidity
event QuorumReached(enum QuorumObjKind objKind, uint256 height, bytes32 objHash, uint256 quorumWeight)
```

### QuorumWeightUpdated

```solidity
event QuorumWeightUpdated(enum QuorumObjKind objKind, uint256 height, bytes32 objHash, uint256 newWeight)
```

### addQuorumSignature

```solidity
function addQuorumSignature(struct QuorumMap self, uint256 height, bytes32[] membershipProof, uint256 weight, bytes signature) internal
```

checks whether the provided quorum signature for the block at height `height` is valid and accumulates that it

_If adding the signature leads to reaching the threshold, then the info is removed from `incompleteQuorums`_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| self | struct QuorumMap |  |
| height | uint256 | - the height of the block in the checkpoint |
| membershipProof | bytes32[] | - a Merkle proof that the validator was in the membership at height `height` with weight `weight` |
| weight | uint256 | - the weight of the validator |
| signature | bytes | - the signature of the object we are agreen on |

### createQuorumInfo

```solidity
function createQuorumInfo(struct QuorumMap self, uint256 objHeight, bytes32 objHash, bytes32 membershipRootHash, uint256 membershipWeight, uint256 majorityPercentage) internal
```

creates the quorum info from a quorum object.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| self | struct QuorumMap |  |
| objHeight | uint256 | - height of the quorum object |
| objHash | bytes32 | - hash of the object |
| membershipRootHash | bytes32 | - a root hash of the Merkle tree built from the validator public keys and their weight |
| membershipWeight | uint256 | - the total weight of the membership |
| majorityPercentage | uint256 | - the majorityPercentage required to reach quorum |

### pruneQuorums

```solidity
function pruneQuorums(struct QuorumMap self, uint256 newRetentionHeight) internal
```

Sets a new  retention height and garbage collects all checkpoints in range [`retentionHeight`, `newRetentionHeight`)

_`retentionHeight` is the height of the first incomplete checkpointswe must keep to implement checkpointing.
All checkpoints with a height less than `retentionHeight` are removed from the history, assuming they are committed to the parent._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| self | struct QuorumMap |  |
| newRetentionHeight | uint256 | - the height of the oldest checkpoint to keep |

### isHeightAlreadyProcessed

```solidity
function isHeightAlreadyProcessed(struct QuorumMap self, uint256 height) internal view
```

### weightNeeded

```solidity
function weightNeeded(uint256 weight, uint256 majorityPercentage) internal pure returns (uint256)
```

returns the needed weight value corresponding to the majority percentage

_`majorityPercentage` must be a valid number_

### getSignatureBundle

```solidity
function getSignatureBundle(struct QuorumMap self, uint256 h) external view returns (struct QuorumInfo info, address[] signatories, bytes[] signatures)
```

get quorum signature bundle consisting of the info, signatories and the corresponding signatures.

