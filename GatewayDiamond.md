# Solidity API

## FunctionNotFound

```solidity
error FunctionNotFound(bytes4 _functionSelector)
```

## FEATURE_MULTILEVEL_CROSSMSG

```solidity
bool FEATURE_MULTILEVEL_CROSSMSG
```

## FEATURE_GENERAL_PUPRPOSE_CROSSMSG

```solidity
bool FEATURE_GENERAL_PUPRPOSE_CROSSMSG
```

## FEATURE_SUBNET_DEPTH

```solidity
uint8 FEATURE_SUBNET_DEPTH
```

## GatewayDiamond

### s

```solidity
struct GatewayActorStorage s
```

### ConstructorParams

```solidity
struct ConstructorParams {
  uint256 bottomUpCheckPeriod;
  uint16 activeValidatorsLimit;
  uint8 majorityPercentage;
  struct SubnetID networkName;
  struct Validator[] genesisValidators;
  bytes32 commitSha;
}
```

### constructor

```solidity
constructor(struct IDiamond.FacetCut[] _diamondCut, struct GatewayDiamond.ConstructorParams params) public
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

