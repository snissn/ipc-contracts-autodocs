# Solidity API

## QuorumObjKind

A kind of quorum.

```solidity
enum QuorumObjKind {
  Checkpoint,
  BottomUpMsgBatch
}
```

## QuorumInfo

Checkpoint quorum information.

```solidity
struct QuorumInfo {
  bytes32 hash;
  bytes32 rootHash;
  uint256 threshold;
  uint256 currentWeight;
  bool reached;
}
```

## QuorumMap

A type aggregating quorum related information.

```solidity
struct QuorumMap {
  enum QuorumObjKind quorumObjKind;
  uint256 retentionHeight;
  mapping(uint256 => struct QuorumInfo) quorumInfo;
  struct EnumerableSet.UintSet incompleteQuorums;
  mapping(uint256 => struct EnumerableSet.AddressSet) quorumSignatureSenders;
  mapping(uint256 => mapping(address => bytes)) quorumSignatures;
}
```

