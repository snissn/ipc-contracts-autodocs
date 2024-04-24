# Solidity API

## SubnetActorStorage

```solidity
struct SubnetActorStorage {
  uint256 genesisCircSupply;
  uint256 lastBottomUpCheckpointHeight;
  uint256 minActivationCollateral;
  uint256 bottomUpCheckPeriod;
  bytes32 currentSubnetHash;
  address ipcGatewayAddr;
  uint64 maxMsgsPerBottomUpBatch;
  uint8 majorityPercentage;
  int8 powerScale;
  enum ConsensusType consensus;
  bool bootstrapped;
  uint64 minValidators;
  bool killed;
  struct SupplySource supplySource;
  struct SubnetID parentId;
  struct ValidatorSet validatorSet;
  struct StakingChangeLog changeSet;
  struct StakingReleaseQueue releaseQueue;
  mapping(address => string) bootstrapNodes;
  struct EnumerableSet.AddressSet bootstrapOwners;
  mapping(uint256 => struct BottomUpCheckpoint) committedCheckpoints;
  struct Validator[] genesisValidators;
  mapping(address => uint256) genesisBalance;
  address[] genesisBalanceKeys;
}
```

## LibSubnetActorStorage

### appStorage

```solidity
function appStorage() internal pure returns (struct SubnetActorStorage ds)
```

## SubnetActorModifiers

### s

```solidity
struct SubnetActorStorage s
```

### onlyGateway

```solidity
modifier onlyGateway()
```

### notKilled

```solidity
modifier notKilled()
```

