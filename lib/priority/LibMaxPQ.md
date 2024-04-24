# Solidity API

## MaxPQ

```solidity
struct MaxPQ {
  struct PQ inner;
}
```

## LibMaxPQ

The max index priority queue for staking. The same implementation as LibMinPQ, just order compare
is reversed.

### getSize

```solidity
function getSize(struct MaxPQ self) internal view returns (uint16)
```

### getAddress

```solidity
function getAddress(struct MaxPQ self, uint16 i) internal view returns (address)
```

### contains

```solidity
function contains(struct MaxPQ self, address validator) internal view returns (bool)
```

### insert

```solidity
function insert(struct MaxPQ self, struct ValidatorSet validators, address validator) internal
```

Insert the validator address into this PQ.
NOTE that caller should ensure the valdiator is not already in the queue.

### pop

```solidity
function pop(struct MaxPQ self, struct ValidatorSet validators) internal
```

Pop the maximum value in the priority queue.
NOTE that caller should ensure the queue is not empty!

### deleteReheapify

```solidity
function deleteReheapify(struct MaxPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the validator is deleted.
NOTE that caller should ensure the queue is not empty.

### increaseReheapify

```solidity
function increaseReheapify(struct MaxPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the collateral of a key has increased.
NOTE that caller should ensure the queue is not empty.

### decreaseReheapify

```solidity
function decreaseReheapify(struct MaxPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the collateral of a key has decreased.
NOTE that caller should ensure the queue is not empty.

### max

```solidity
function max(struct MaxPQ self, struct ValidatorSet validators) internal view returns (address, uint256)
```

Get the maximum value in the priority queue.
NOTE that caller should ensure the queue is not empty!

### swim

```solidity
function swim(struct MaxPQ self, struct ValidatorSet validators, uint16 pos, uint256 value) internal
```

### sink

```solidity
function sink(struct MaxPQ self, struct ValidatorSet validators, uint16 pos, uint256 value) internal
```

### largerPosition

```solidity
function largerPosition(struct MaxPQ self, struct ValidatorSet validators, uint16 pos1, uint16 pos2) internal view returns (uint16, uint256)
```

Get the larger index of pos1 and pos2.

### firstValueSmaller

```solidity
function firstValueSmaller(uint256 v1, uint256 v2) internal pure returns (bool)
```

