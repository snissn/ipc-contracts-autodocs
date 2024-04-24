# Solidity API

## SubnetActorCheckpointingFacet

### submitCheckpoint

```solidity
function submitCheckpoint(struct BottomUpCheckpoint checkpoint, address[] signatories, bytes[] signatures) external
```

Submits a checkpoint commitment for execution.

_It triggers the commitment of the checkpoint and any other side-effects that
        need to be triggered by the checkpoint such as relayer reward book keeping._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| checkpoint | struct BottomUpCheckpoint | The executed bottom-up checkpoint. |
| signatories | address[] | The addresses of validators signing the checkpoint. |
| signatures | bytes[] | The signatures of validators on the checkpoint. |

### validateActiveQuorumSignatures

```solidity
function validateActiveQuorumSignatures(address[] signatories, bytes32 hash, bytes[] signatures) public view
```

Checks whether the signatures are valid for the provided signatories and hash within the current validator set.
        Reverts otherwise.

_Signatories in `signatories` and their signatures in `signatures` must be provided in the same order.
      Having it public allows external users to perform sanity-check verification if needed._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| signatories | address[] | The addresses of the signatories. |
| hash | bytes32 | The hash of the checkpoint. |
| signatures | bytes[] | The packed signatures of the checkpoint. |

### ensureValidCheckpoint

```solidity
function ensureValidCheckpoint(struct BottomUpCheckpoint checkpoint) internal view
```

Ensures the checkpoint is valid.

_The checkpoint block height must be equal to the last bottom-up checkpoint height or
the next one or the number of bottom up messages exceeds the max batch size._

