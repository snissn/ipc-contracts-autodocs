# Solidity API

## FunctionNotFound

```solidity
error FunctionNotFound(bytes4 _functionSelector)
```

## SubnetRegistryDiamond

### s

```solidity
struct SubnetRegistryActorStorage s
```

### ConstructorParams

```solidity
struct ConstructorParams {
  address gateway;
  address getterFacet;
  address managerFacet;
  address rewarderFacet;
  address checkpointerFacet;
  address pauserFacet;
  address diamondCutFacet;
  address diamondLoupeFacet;
  address ownershipFacet;
  bytes4[] subnetActorGetterSelectors;
  bytes4[] subnetActorManagerSelectors;
  bytes4[] subnetActorRewarderSelectors;
  bytes4[] subnetActorCheckpointerSelectors;
  bytes4[] subnetActorPauserSelectors;
  bytes4[] subnetActorDiamondCutSelectors;
  bytes4[] subnetActorDiamondLoupeSelectors;
  bytes4[] subnetActorOwnershipSelectors;
  enum SubnetCreationPrivileges creationPrivileges;
}
```

### constructor

```solidity
constructor(struct IDiamond.FacetCut[] _diamondCut, struct SubnetRegistryDiamond.ConstructorParams params) public
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

