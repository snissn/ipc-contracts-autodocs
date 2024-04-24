# Solidity API

## LibStakingChangeLog

The util library for `StakingChangeLog`

### NewStakingChangeRequest

```solidity
event NewStakingChangeRequest(enum StakingOperation op, address validator, bytes payload, uint64 configurationNumber)
```

### metadataRequest

```solidity
function metadataRequest(struct StakingChangeLog changes, address validator, bytes metadata) internal
```

Validator request to update its metadata

### federatedPowerRequest

```solidity
function federatedPowerRequest(struct StakingChangeLog changes, address validator, bytes metadata, uint256 power) internal
```

Records a request to update the federated power of a validator

### withdrawRequest

```solidity
function withdrawRequest(struct StakingChangeLog changes, address validator, uint256 amount) internal
```

Perform upsert operation to the withdraw changes, return total value to withdraw
of the validator.
Each insert will increment the configuration number by 1, update will not.

### depositRequest

```solidity
function depositRequest(struct StakingChangeLog changes, address validator, uint256 amount) internal
```

Perform upsert operation to the deposit changes

### recordChange

```solidity
function recordChange(struct StakingChangeLog changes, address validator, enum StakingOperation op, bytes payload) internal returns (uint64 configurationNumber)
```

Perform upsert operation to the deposit changes

### getChange

```solidity
function getChange(struct StakingChangeLog changes, uint64 configurationNumber) internal view returns (struct StakingChange)
```

Get the change at configuration number

### purgeChange

```solidity
function purgeChange(struct StakingChangeLog changes, uint64 configurationNumber) internal
```

