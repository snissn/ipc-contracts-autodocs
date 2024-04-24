# Solidity API

## MinPQ

```solidity
struct MinPQ {
  struct PQ inner;
}
```

## LibMinPQ

The min index priority queue for staking

### getSize

```solidity
function getSize(struct MinPQ self) internal view returns (uint16)
```

### getAddress

```solidity
function getAddress(struct MinPQ self, uint16 i) internal view returns (address)
```

### contains

```solidity
function contains(struct MinPQ self, address validator) internal view returns (bool)
```

### insert

```solidity
function insert(struct MinPQ self, struct ValidatorSet validators, address validator) internal
```

Insert the validator address into this PQ.
NOTE that caller should ensure the validator is not already in the queue.

### pop

```solidity
function pop(struct MinPQ self, struct ValidatorSet validators) internal
```

Pop the minimal value in the priority queue.

### deleteReheapify

```solidity
function deleteReheapify(struct MinPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the validator is deleted.

### increaseReheapify

```solidity
function increaseReheapify(struct MinPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the collateral of a key has increased.

### decreaseReheapify

```solidity
function decreaseReheapify(struct MinPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the collateral of a key has decreased.

### min

```solidity
function min(struct MinPQ self, struct ValidatorSet validators) internal view returns (address, uint256)
```

Get the minimal value in the priority queue.
NOTE that caller should ensure the queue is not empty!

### swim

```solidity
function swim(struct MinPQ self, struct ValidatorSet validators, uint16 pos, uint256 value) internal
```

### sink

```solidity
function sink(struct MinPQ self, struct ValidatorSet validators, uint16 pos, uint256 value) internal
```

### smallerPosition

```solidity
function smallerPosition(struct MinPQ self, struct ValidatorSet validators, uint16 pos1, uint16 pos2) internal view returns (uint16, uint256)
```

Get the smaller index of pos1 and pos2.

### firstValueLarger

```solidity
function firstValueLarger(uint256 v1, uint256 v2) internal pure returns (bool)
```

