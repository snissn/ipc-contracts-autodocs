# Solidity API

## GatewayActorStorage

```solidity
struct GatewayActorStorage {
  uint256 latestParentHeight;
  uint256 bottomUpCheckPeriod;
  uint256 bottomUpMsgBatchPeriod;
  uint64 bottomUpNonce;
  uint64 appliedTopDownNonce;
  uint64 totalSubnets;
  uint64 maxMsgsPerBottomUpBatch;
  uint8 majorityPercentage;
  bytes32 commitSha;
  uint8 maxTreeDepth;
  bool generalPurposeCrossMsg;
  bool multiLevelCrossMsg;
  struct Membership currentMembership;
  struct Membership lastMembership;
  struct QuorumMap checkpointQuorumMap;
  struct SubnetID networkName;
  struct ParentValidatorsTracker validatorsTracker;
  mapping(bytes32 => struct Subnet) subnets;
  mapping(uint256 => struct ParentFinality) finalitiesMap;
  mapping(bytes32 => struct IpcEnvelope) postbox;
  mapping(uint256 => struct BottomUpCheckpoint) bottomUpCheckpoints;
  mapping(uint256 => struct BottomUpMsgBatch) bottomUpMsgBatches;
  struct EnumerableSet.Bytes32Set subnetKeys;
}
```

## LibGatewayActorStorage

### appStorage

```solidity
function appStorage() internal pure returns (struct GatewayActorStorage ds)
```

## GatewayActorModifiers

### s

```solidity
struct GatewayActorStorage s
```

### systemActorOnly

```solidity
modifier systemActorOnly()
```

