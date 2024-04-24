# Solidity API

## MAX_MSGS_PER_BATCH

```solidity
uint64 MAX_MSGS_PER_BATCH
```

## BATCH_PERIOD

```solidity
uint256 BATCH_PERIOD
```

## ParentFinality

The parent finality for IPC parent at certain height.

```solidity
struct ParentFinality {
  uint256 height;
  bytes32 blockHash;
}
```

## BottomUpCheckpoint

A bottom-up checkpoint type.

```solidity
struct BottomUpCheckpoint {
  struct SubnetID subnetID;
  uint256 blockHeight;
  bytes32 blockHash;
  uint64 nextConfigurationNumber;
  struct IpcEnvelope[] msgs;
}
```

## BottomUpMsgBatch

A batch of bottom-up messages for execution.

```solidity
struct BottomUpMsgBatch {
  struct SubnetID subnetID;
  uint256 blockHeight;
  struct IpcEnvelope[] msgs;
}
```

## BottomUpMsgBatchInfo

Tracks information about the last batch executed.

```solidity
struct BottomUpMsgBatchInfo {
  uint256 blockHeight;
  bytes32 hash;
}
```

## IpcMsgKind

Type of cross-net messages currently supported

```solidity
enum IpcMsgKind {
  Transfer,
  Call,
  Result
}
```

## IpcEnvelope

Envelope used to propagate IPC cross-net messages

```solidity
struct IpcEnvelope {
  enum IpcMsgKind kind;
  struct IPCAddress to;
  struct IPCAddress from;
  uint64 nonce;
  uint256 value;
  bytes message;
}
```

## CallMsg

Message format used for `Transfer` and `Call` messages.

```solidity
struct CallMsg {
  bytes method;
  bytes params;
}
```

## OutcomeType

This struct indicates if the cross message execution is sucess, IPC system error or from the invoked
        contract

```solidity
enum OutcomeType {
  Ok,
  SystemErr,
  ActorErr
}
```

## ResultMsg

```solidity
struct ResultMsg {
  bytes32 id;
  enum OutcomeType outcome;
  bytes ret;
}
```

