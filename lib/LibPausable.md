# Solidity API

## Pausable

Abstract contract that enables contract to pause marked operations

### PausableStorage

```solidity
struct PausableStorage {
  bool paused;
}
```

### Paused

```solidity
event Paused(address account)
```

_Emitted when the pause is triggered by `account`._

### Unpaused

```solidity
event Unpaused(address account)
```

_Emitted when the unpause is triggered by `account`._

### EnforcedPause

```solidity
error EnforcedPause()
```

_The operation failed because the contract is paused._

### ExpectedPause

```solidity
error ExpectedPause()
```

_The operation failed because the contract is not paused._

### whenNotPaused

```solidity
modifier whenNotPaused()
```

_Modifier to make a function callable only when the contract is not paused.

Requirements:

- The contract must not be paused._

### whenPaused

```solidity
modifier whenPaused()
```

_Modifier to make a function callable only when the contract is paused.

Requirements:

- The contract must be paused._

### _requireNotPaused

```solidity
function _requireNotPaused() internal view
```

_Throws if the contract is paused._

### _requirePaused

```solidity
function _requirePaused() internal view
```

_Throws if the contract is not paused._

### _paused

```solidity
function _paused() internal view returns (bool)
```

returns true if the contract is paused

### _pause

```solidity
function _pause() internal
```

_Triggers stopped state.

Requirements:

- The contract must not be paused._

### _unpause

```solidity
function _unpause() internal
```

_Returns to normal state.

Requirements:

- The contract must be paused._

