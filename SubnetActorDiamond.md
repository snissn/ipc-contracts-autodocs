# Solidity API

## FunctionNotFound

```solidity
error FunctionNotFound(bytes4 _functionSelector)
```

## SubnetActorDiamond

### s

```solidity
struct SubnetActorStorage s
```

### ConstructorParams

```solidity
struct ConstructorParams {
  uint256 minActivationCollateral;
  uint64 minValidators;
  uint64 bottomUpCheckPeriod;
  address ipcGatewayAddr;
  uint16 activeValidatorsLimit;
  uint8 majorityPercentage;
  enum ConsensusType consensus;
  int8 powerScale;
  enum PermissionMode permissionMode;
  struct SupplySource supplySource;
  struct SubnetID parentId;
}
```

### constructor

```solidity
constructor(struct IDiamond.FacetCut[] _diamondCut, struct SubnetActorDiamond.ConstructorParams params, address owner) public
```

### _fallback

```solidity
function _fallback() internal
```

### fallback

```solidity
fallback() external payable
```

Will run when no functions matches call data

### receive

```solidity
receive() external payable
```

Same as fallback but called when calldata is empty

### onlyGateway

```solidity
modifier onlyGateway()
```

