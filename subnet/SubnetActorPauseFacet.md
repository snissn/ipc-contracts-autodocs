# Solidity API

## SubnetActorPauseFacet

### pause

```solidity
function pause() external
```

Pauses all contract functions with the `whenNotPaused` modifier.

### unpause

```solidity
function unpause() external
```

Unpauses all contract functions with the `whenNotPaused` modifier.

### paused

```solidity
function paused() external view returns (bool)
```

Returns true if the SubnetActor contract is paused.

