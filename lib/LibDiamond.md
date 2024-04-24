# Solidity API

## LibDiamond

### DIAMOND_STORAGE_POSITION

```solidity
bytes32 DIAMOND_STORAGE_POSITION
```

### InvalidAddress

```solidity
error InvalidAddress()
```

### NotOwner

```solidity
error NotOwner()
```

### NoBytecodeAtAddress

```solidity
error NoBytecodeAtAddress(address _contractAddress, string _message)
```

### IncorrectFacetCutAction

```solidity
error IncorrectFacetCutAction(enum IDiamond.FacetCutAction _action)
```

### NoSelectorsProvidedForFacetForCut

```solidity
error NoSelectorsProvidedForFacetForCut(address _facetAddress)
```

### CannotAddFunctionToDiamondThatAlreadyExists

```solidity
error CannotAddFunctionToDiamondThatAlreadyExists(bytes4 _selector)
```

### CannotAddSelectorsToZeroAddress

```solidity
error CannotAddSelectorsToZeroAddress(bytes4[] _selectors)
```

### InitializationFunctionReverted

```solidity
error InitializationFunctionReverted(address _initializationContractAddress, bytes _calldata)
```

### NoSelectorsGivenToAdd

```solidity
error NoSelectorsGivenToAdd()
```

### NotContractOwner

```solidity
error NotContractOwner(address _user, address _contractOwner)
```

### CannotReplaceFunctionsFromFacetWithZeroAddress

```solidity
error CannotReplaceFunctionsFromFacetWithZeroAddress(bytes4[] _selectors)
```

### CannotReplaceImmutableFunction

```solidity
error CannotReplaceImmutableFunction(bytes4 _selector)
```

### CannotReplaceFunctionWithTheSameFunctionFromTheSameFacet

```solidity
error CannotReplaceFunctionWithTheSameFunctionFromTheSameFacet(bytes4 _selector)
```

### CannotReplaceFunctionThatDoesNotExists

```solidity
error CannotReplaceFunctionThatDoesNotExists(bytes4 _selector)
```

### RemoveFacetAddressMustBeZeroAddress

```solidity
error RemoveFacetAddressMustBeZeroAddress(address _facetAddress)
```

### CannotRemoveFunctionThatDoesNotExist

```solidity
error CannotRemoveFunctionThatDoesNotExist(bytes4 _selector)
```

### CannotRemoveImmutableFunction

```solidity
error CannotRemoveImmutableFunction(bytes4 _selector)
```

### OwnershipTransferred

```solidity
event OwnershipTransferred(address oldOwner, address newOwner)
```

### FacetAddressAndSelectorPosition

```solidity
struct FacetAddressAndSelectorPosition {
  address facetAddress;
  uint16 selectorPosition;
}
```

### DiamondStorage

```solidity
struct DiamondStorage {
  mapping(bytes4 => struct LibDiamond.FacetAddressAndSelectorPosition) facetAddressAndSelectorPosition;
  bytes4[] selectors;
  mapping(bytes4 => bool) supportedInterfaces;
  address contractOwner;
}
```

### transferOwnership

```solidity
function transferOwnership(address newOwner) internal
```

_Transfers ownership of the contract to a new account (`newOwner`).
Can only be called by the current owner._

### diamondStorage

```solidity
function diamondStorage() internal pure returns (struct LibDiamond.DiamondStorage ds)
```

### setContractOwner

```solidity
function setContractOwner(address _newOwner) internal
```

### contractOwner

```solidity
function contractOwner() internal view returns (address contractOwner_)
```

### onlyOwner

```solidity
modifier onlyOwner()
```

### enforceIsContractOwner

```solidity
function enforceIsContractOwner() internal view
```

### diamondCut

```solidity
function diamondCut(struct IDiamond.FacetCut[] _diamondCut, address _init, bytes _calldata) internal
```

### addFunctions

```solidity
function addFunctions(address _facetAddress, bytes4[] _functionSelectors) internal
```

### replaceFunctions

```solidity
function replaceFunctions(address _facetAddress, bytes4[] _functionSelectors) internal
```

### removeFunctions

```solidity
function removeFunctions(address _facetAddress, bytes4[] _functionSelectors) internal
```

### initializeDiamondCut

```solidity
function initializeDiamondCut(address _init, bytes _calldata) internal
```

### enforceHasContractCode

```solidity
function enforceHasContractCode(address _contract, string _errorMessage) internal view
```

