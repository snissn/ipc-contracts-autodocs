# Solidity API

## ReentrancyGuard

Abstract contract to provide protection against reentrancy

### ReentrancyStorage

```solidity
struct ReentrancyStorage {
  uint256 status;
}
```

### ReentrancyError

```solidity
error ReentrancyError()
```

### nonReentrant

```solidity
modifier nonReentrant()
```

