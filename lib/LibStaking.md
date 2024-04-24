# Solidity API

## LibAddressStakingReleases

### push

```solidity
function push(struct AddressStakingReleases self, struct StakingRelease release) internal
```

Add new release to the storage. Caller makes sure the release.releasedAt is ordered
in ascending order. This method does not do checks on this.

### compact

```solidity
function compact(struct AddressStakingReleases self) internal returns (uint256, uint16)
```

Perform compaction on releases, i.e. aggregates the amount that can be released
and removes them from storage. Returns the total amount to release and the new
number of pending releases after compaction.

## LibStakingReleaseQueue

The util library for `StakingReleaseQueue`

### NewCollateralRelease

```solidity
event NewCollateralRelease(address validator, uint256 amount, uint256 releaseBlock)
```

### setLockDuration

```solidity
function setLockDuration(struct StakingReleaseQueue self, uint256 blocks) internal
```

### addNewRelease

```solidity
function addNewRelease(struct StakingReleaseQueue self, address validator, uint256 amount) internal
```

Set the amount and time for release collateral

### claim

```solidity
function claim(struct StakingReleaseQueue self, address validator) internal returns (uint256)
```

Validator claim the available collateral that are released

## LibValidatorSet

The util library for `ValidatorSet`

### ActiveValidatorCollateralUpdated

```solidity
event ActiveValidatorCollateralUpdated(address validator, uint256 newPower)
```

### WaitingValidatorCollateralUpdated

```solidity
event WaitingValidatorCollateralUpdated(address validator, uint256 newPower)
```

### NewActiveValidator

```solidity
event NewActiveValidator(address validator, uint256 power)
```

### NewWaitingValidator

```solidity
event NewWaitingValidator(address validator, uint256 power)
```

### ActiveValidatorReplaced

```solidity
event ActiveValidatorReplaced(address oldValidator, address newValidator)
```

### ActiveValidatorLeft

```solidity
event ActiveValidatorLeft(address validator)
```

### WaitingValidatorLeft

```solidity
event WaitingValidatorLeft(address validator)
```

### getPower

```solidity
function getPower(struct ValidatorSet validators, address validator) internal view returns (uint256 power)
```

Get the total voting power for the validator

### getTotalConfirmedCollateral

```solidity
function getTotalConfirmedCollateral(struct ValidatorSet validators) internal view returns (uint256 collateral)
```

Get the total confirmed collateral of the validators.

### totalActiveValidators

```solidity
function totalActiveValidators(struct ValidatorSet validators) internal view returns (uint16 total)
```

Get the total active validators.

### getConfirmedCollateral

```solidity
function getConfirmedCollateral(struct ValidatorSet validators, address validator) internal view returns (uint256 collateral)
```

Get the confirmed collateral of the validator.

### listActiveValidators

```solidity
function listActiveValidators(struct ValidatorSet validators) internal view returns (address[] addresses)
```

### getTotalActivePower

```solidity
function getTotalActivePower(struct ValidatorSet validators) internal view returns (uint256 collateral)
```

Get the total collateral of *active* validators.

### getTotalCollateral

```solidity
function getTotalCollateral(struct ValidatorSet validators) internal view returns (uint256 collateral)
```

Get the total collateral of the *waiting* and *active* validators.

### getTotalPowerOfValidators

```solidity
function getTotalPowerOfValidators(struct ValidatorSet validators, address[] addresses) internal view returns (uint256[])
```

Get the total power of the validators.
The function reverts if at least one validator is not in the active validator set.

### isActiveValidator

```solidity
function isActiveValidator(struct ValidatorSet self, address validator) internal view returns (bool)
```

### setMetadata

```solidity
function setMetadata(struct ValidatorSet validators, address validator, bytes metadata) internal
```

Set validator data

### recordDeposit

```solidity
function recordDeposit(struct ValidatorSet validators, address validator, uint256 amount) internal
```

Validator increases its total collateral by amount.

### recordWithdraw

```solidity
function recordWithdraw(struct ValidatorSet validators, address validator, uint256 amount) internal
```

Validator reduces its total collateral by amount.

### confirmFederatedPower

```solidity
function confirmFederatedPower(struct ValidatorSet self, address validator, uint256 power) internal
```

Validator's federated power was updated by admin

### confirmDeposit

```solidity
function confirmDeposit(struct ValidatorSet self, address validator, uint256 amount) internal
```

### confirmWithdraw

```solidity
function confirmWithdraw(struct ValidatorSet self, address validator, uint256 amount) internal
```

### increaseReshuffle

```solidity
function increaseReshuffle(struct ValidatorSet self, address maybeActive, uint256 newPower) internal
```

Reshuffles the active and waiting validators when an increase in power is confirmed

### reduceReshuffle

```solidity
function reduceReshuffle(struct ValidatorSet self, address validator, uint256 newPower) internal
```

Reshuffles the active and waiting validators when a power reduction is confirmed

## LibStaking

### INITIAL_CONFIGURATION_NUMBER

```solidity
uint64 INITIAL_CONFIGURATION_NUMBER
```

### ConfigurationNumberConfirmed

```solidity
event ConfigurationNumberConfirmed(uint64 number)
```

### CollateralClaimed

```solidity
event CollateralClaimed(address validator, uint256 amount)
```

### getPower

```solidity
function getPower(address validator) internal view returns (uint256 power)
```

### isActiveValidator

```solidity
function isActiveValidator(address validator) internal view returns (bool)
```

Checks if the validator is an active validator

### isWaitingValidator

```solidity
function isWaitingValidator(address validator) internal view returns (bool)
```

Checks if the validator is a waiting validator

### isValidator

```solidity
function isValidator(address addr) internal view returns (bool)
```

Checks if the provided address is a validator (active or waiting) based on its total collateral.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| addr | address | The address to check for validator status. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | A boolean indicating whether the address is a validator. |

### hasStaked

```solidity
function hasStaked(address validator) internal view returns (bool)
```

Checks if the validator has staked before.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validator | address | The address to check for staking status. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | A boolean indicating whether the validator has staked. |

### totalActiveValidators

```solidity
function totalActiveValidators() internal view returns (uint16)
```

### totalValidators

```solidity
function totalValidators() internal view returns (uint16)
```

Gets the total number of validators, including active and waiting

### getTotalConfirmedCollateral

```solidity
function getTotalConfirmedCollateral() internal view returns (uint256)
```

### getTotalCollateral

```solidity
function getTotalCollateral() internal view returns (uint256)
```

### totalValidatorCollateral

```solidity
function totalValidatorCollateral(address validator) internal view returns (uint256)
```

Gets the total collateral the validators has staked.

### setFederatedPowerWithConfirm

```solidity
function setFederatedPowerWithConfirm(address validator, uint256 power) internal
```

Set the validator federated power directly without queueing the request

### setMetadataWithConfirm

```solidity
function setMetadataWithConfirm(address validator, bytes metadata) internal
```

Set the validator metadata directly without queueing the request

### depositWithConfirm

```solidity
function depositWithConfirm(address validator, uint256 amount) internal
```

Confirm the deposit directly without going through the confirmation process

### withdrawWithConfirm

```solidity
function withdrawWithConfirm(address validator, uint256 amount) internal
```

Confirm the withdraw directly without going through the confirmation process
and releasing from the gateway.

_only use for non-bootstrapped subnets_

### setFederatedPower

```solidity
function setFederatedPower(address validator, bytes metadata, uint256 amount) internal
```

Set the federated power of the validator

### setValidatorMetadata

```solidity
function setValidatorMetadata(address validator, bytes metadata) internal
```

Set the validator metadata

### deposit

```solidity
function deposit(address validator, uint256 amount) internal
```

Deposit the collateral

### withdraw

```solidity
function withdraw(address validator, uint256 amount) internal
```

Withdraw the collateral

### claimCollateral

```solidity
function claimCollateral(address validator) internal
```

Claim the released collateral

### getConfigurationNumbers

```solidity
function getConfigurationNumbers() internal view returns (uint64, uint64)
```

### confirmChange

```solidity
function confirmChange(uint64 configurationNumber) internal
```

Confirm the changes in bottom up checkpoint submission, only call this in bottom up checkpoint execution.

## LibValidatorTracking

The library for tracking validator changes coming from the parent.
Should be used in the child gateway to store changes until they can be applied.

### storeChange

```solidity
function storeChange(struct ParentValidatorsTracker self, struct StakingChangeRequest changeRequest) internal
```

### batchStoreChange

```solidity
function batchStoreChange(struct ParentValidatorsTracker self, struct StakingChangeRequest[] changeRequests) internal
```

### confirmChange

```solidity
function confirmChange(struct ParentValidatorsTracker self, uint64 configurationNumber) internal
```

Confirm the changes in for a finality commitment

