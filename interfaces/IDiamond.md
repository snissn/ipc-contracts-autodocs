# Solidity API

## IDiamond

### FacetCutAction

```solidity
enum FacetCutAction {
  Add,
  Replace,
  Remove
}
```

### FacetCut

```solidity
struct FacetCut {
  address facetAddress;
  enum IDiamond.FacetCutAction action;
  bytes4[] functionSelectors;
}
```

### DiamondCut

```solidity
event DiamondCut(struct IDiamond.FacetCut[] _diamondCut, address _init, bytes _calldata)
```

