# Solidity API

## PQ

The inner data structure for both min and max priority queue

```solidity
struct PQ {
  uint16 size;
  mapping(address => uint16) addressToPos;
  mapping(uint16 => address) posToAddress;
}
```

## LibPQ

### isEmpty

```solidity
function isEmpty(struct PQ self) internal view returns (bool)
```

### requireNotEmpty

```solidity
function requireNotEmpty(struct PQ self) internal view
```

### getSize

```solidity
function getSize(struct PQ self) internal view returns (uint16)
```

### contains

```solidity
function contains(struct PQ self, address validator) internal view returns (bool)
```

### getPosOrRevert

```solidity
function getPosOrRevert(struct PQ self, address validator) internal view returns (uint16 pos)
```

### del

```solidity
function del(struct PQ self, uint16 pos) internal
```

### getPower

```solidity
function getPower(struct PQ self, struct ValidatorSet validators, uint16 pos) internal view returns (uint256)
```

### getConfirmedCollateral

```solidity
function getConfirmedCollateral(struct PQ self, struct ValidatorSet validators, uint16 pos) internal view returns (uint256)
```

### exchange

```solidity
function exchange(struct PQ self, uint16 pos1, uint16 pos2) internal
```

