# Solidity API

## AddressShouldBeValidator

```solidity
error AddressShouldBeValidator()
```

## AlreadyRegisteredSubnet

```solidity
error AlreadyRegisteredSubnet()
```

## AlreadyInSet

```solidity
error AlreadyInSet()
```

## CannotConfirmFutureChanges

```solidity
error CannotConfirmFutureChanges()
```

## CannotReleaseZero

```solidity
error CannotReleaseZero()
```

## CannotSendCrossMsgToItself

```solidity
error CannotSendCrossMsgToItself()
```

## CheckpointAlreadyExists

```solidity
error CheckpointAlreadyExists()
```

## BatchAlreadyExists

```solidity
error BatchAlreadyExists()
```

## MaxMsgsPerBatchExceeded

```solidity
error MaxMsgsPerBatchExceeded()
```

## QuorumAlreadyProcessed

```solidity
error QuorumAlreadyProcessed()
```

## CheckpointNotCreated

```solidity
error CheckpointNotCreated()
```

## BottomUpCheckpointAlreadySubmitted

```solidity
error BottomUpCheckpointAlreadySubmitted()
```

## BatchNotCreated

```solidity
error BatchNotCreated()
```

## CollateralIsZero

```solidity
error CollateralIsZero()
```

## EmptyAddress

```solidity
error EmptyAddress()
```

## FailedAddIncompleteQuorum

```solidity
error FailedAddIncompleteQuorum()
```

## FailedAddSignatory

```solidity
error FailedAddSignatory()
```

## FailedRemoveIncompleteQuorum

```solidity
error FailedRemoveIncompleteQuorum()
```

## GatewayCannotBeZero

```solidity
error GatewayCannotBeZero()
```

## InvalidActorAddress

```solidity
error InvalidActorAddress()
```

## InvalidCheckpointEpoch

```solidity
error InvalidCheckpointEpoch()
```

## CannotSubmitFutureCheckpoint

```solidity
error CannotSubmitFutureCheckpoint()
```

## InvalidBatchEpoch

```solidity
error InvalidBatchEpoch()
```

## InvalidCheckpointSource

```solidity
error InvalidCheckpointSource()
```

## InvalidBatchSource

```solidity
error InvalidBatchSource()
```

## InvalidSubnetActor

```solidity
error InvalidSubnetActor()
```

## InvalidCollateral

```solidity
error InvalidCollateral()
```

## InvalidConfigurationNumber

```solidity
error InvalidConfigurationNumber()
```

## InvalidXnetMessage

```solidity
error InvalidXnetMessage(enum InvalidXnetMessageReason reason)
```

## InvalidMajorityPercentage

```solidity
error InvalidMajorityPercentage()
```

## InvalidPowerScale

```solidity
error InvalidPowerScale()
```

## InvalidRetentionHeight

```solidity
error InvalidRetentionHeight()
```

## InvalidSignature

```solidity
error InvalidSignature()
```

## InvalidSignatureErr

```solidity
error InvalidSignatureErr(uint8)
```

## InvalidSignatureLength

```solidity
error InvalidSignatureLength()
```

## InvalidPublicKeyLength

```solidity
error InvalidPublicKeyLength()
```

## InvalidSubmissionPeriod

```solidity
error InvalidSubmissionPeriod()
```

## InvalidSubnet

```solidity
error InvalidSubnet()
```

## NoCollateralToWithdraw

```solidity
error NoCollateralToWithdraw()
```

## NoValidatorsInSubnet

```solidity
error NoValidatorsInSubnet()
```

## NotAllValidatorsHaveLeft

```solidity
error NotAllValidatorsHaveLeft()
```

## NotAuthorized

```solidity
error NotAuthorized(address)
```

## NotEmptySubnetCircSupply

```solidity
error NotEmptySubnetCircSupply()
```

## NotEnoughBalance

```solidity
error NotEnoughBalance()
```

## NotEnoughBalanceForRewards

```solidity
error NotEnoughBalanceForRewards()
```

## NotEnoughCollateral

```solidity
error NotEnoughCollateral()
```

## NotEnoughFunds

```solidity
error NotEnoughFunds()
```

## NotEnoughFundsToRelease

```solidity
error NotEnoughFundsToRelease()
```

## NotEnoughSubnetCircSupply

```solidity
error NotEnoughSubnetCircSupply()
```

## NotEnoughValidatorsInSubnet

```solidity
error NotEnoughValidatorsInSubnet()
```

## NotGateway

```solidity
error NotGateway()
```

## NotInSet

```solidity
error NotInSet()
```

## NotOwnerOfPublicKey

```solidity
error NotOwnerOfPublicKey()
```

## NotRegisteredSubnet

```solidity
error NotRegisteredSubnet()
```

## NotStakedBefore

```solidity
error NotStakedBefore()
```

## NotSystemActor

```solidity
error NotSystemActor()
```

## NotValidator

```solidity
error NotValidator(address)
```

## OldConfigurationNumber

```solidity
error OldConfigurationNumber()
```

## PQDoesNotContainAddress

```solidity
error PQDoesNotContainAddress()
```

## PQEmpty

```solidity
error PQEmpty()
```

## ParentFinalityAlreadyCommitted

```solidity
error ParentFinalityAlreadyCommitted()
```

## PostboxNotExist

```solidity
error PostboxNotExist()
```

## SignatureReplay

```solidity
error SignatureReplay()
```

## SubnetAlreadyKilled

```solidity
error SubnetAlreadyKilled()
```

## SubnetNotActive

```solidity
error SubnetNotActive()
```

## SubnetNotFound

```solidity
error SubnetNotFound()
```

## WithdrawExceedingCollateral

```solidity
error WithdrawExceedingCollateral()
```

## ZeroMembershipWeight

```solidity
error ZeroMembershipWeight()
```

## SubnetAlreadyBootstrapped

```solidity
error SubnetAlreadyBootstrapped()
```

## SubnetNotBootstrapped

```solidity
error SubnetNotBootstrapped()
```

## FacetCannotBeZero

```solidity
error FacetCannotBeZero()
```

## WrongGateway

```solidity
error WrongGateway()
```

## CannotFindSubnet

```solidity
error CannotFindSubnet()
```

## UnknownSubnet

```solidity
error UnknownSubnet()
```

## MethodNotAllowed

```solidity
error MethodNotAllowed(string reason)
```

## InvalidFederationPayload

```solidity
error InvalidFederationPayload()
```

## DuplicatedGenesisValidator

```solidity
error DuplicatedGenesisValidator()
```

## NotEnoughGenesisValidators

```solidity
error NotEnoughGenesisValidators()
```

## InvalidXnetMessageReason

```solidity
enum InvalidXnetMessageReason {
  Sender,
  DstSubnet,
  Nonce,
  Value,
  Kind
}
```

## ERR_PERMISSIONED_AND_BOOTSTRAPPED

```solidity
string ERR_PERMISSIONED_AND_BOOTSTRAPPED
```

## ERR_VALIDATOR_JOINED

```solidity
string ERR_VALIDATOR_JOINED
```

## ERR_VALIDATOR_NOT_JOINED

```solidity
string ERR_VALIDATOR_NOT_JOINED
```

