# Solidity API

## SubnetActorGetterFacet

### s

```solidity
struct SubnetActorStorage s
```

### getParent

```solidity
function getParent() external view returns (struct SubnetID)
```

Returns the parent subnet id.

### permissionMode

```solidity
function permissionMode() external view returns (enum PermissionMode)
```

Returns the permission mode.

### ipcGatewayAddr

```solidity
function ipcGatewayAddr() external view returns (address)
```

Returns the gateway address.

### minValidators

```solidity
function minValidators() external view returns (uint64)
```

Returns the minimum validators number needed to activate the subnet.

### majorityPercentage

```solidity
function majorityPercentage() external view returns (uint8)
```

Returns the majority percentage required for consensus.

### activeValidatorsLimit

```solidity
function activeValidatorsLimit() external view returns (uint16)
```

Fetches the limit on the number of active validators.

### getConfigurationNumbers

```solidity
function getConfigurationNumbers() external view returns (uint64, uint64)
```

Returns the next and start configuration numbers related to the changes.

### genesisValidators

```solidity
function genesisValidators() external view returns (struct Validator[])
```

Returns the initial set of validators of the genesis block.

### genesisCircSupply

```solidity
function genesisCircSupply() external view returns (uint256)
```

### genesisBalances

```solidity
function genesisBalances() external view returns (address[], uint256[])
```

Retrieves initial balances and corresponding addresses of the genesis block.

### bottomUpCheckPeriod

```solidity
function bottomUpCheckPeriod() external view returns (uint256)
```

Returns the period for bottom-up checkpointing operations.

### lastBottomUpCheckpointHeight

```solidity
function lastBottomUpCheckpointHeight() external view returns (uint256)
```

Returns the block height of the last bottom-up checkpoint.

### consensus

```solidity
function consensus() external view returns (enum ConsensusType)
```

Returns the consensus protocol type used in the subnet.

### bootstrapped

```solidity
function bootstrapped() external view returns (bool)
```

Checks if the subnet has been bootstrapped.

### killed

```solidity
function killed() external view returns (bool)
```

Checks if the subnet has been terminated or "killed".

### minActivationCollateral

```solidity
function minActivationCollateral() external view returns (uint256)
```

Returns the minimum collateral required for subnet activation.

### getValidator

```solidity
function getValidator(address validatorAddress) external view returns (struct ValidatorInfo validator)
```

Returns detailed information about a specific validator.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validatorAddress | address | The address of the validator to query information for. |

### getTotalValidatorsNumber

```solidity
function getTotalValidatorsNumber() external view returns (uint16)
```

Returns the total number of validators (active and waiting).

### getActiveValidatorsNumber

```solidity
function getActiveValidatorsNumber() external view returns (uint16)
```

Returns the number of active validators.

### getTotalConfirmedCollateral

```solidity
function getTotalConfirmedCollateral() external view returns (uint256)
```

Returns the total amount of confirmed collateral across all validators.

### getTotalCollateral

```solidity
function getTotalCollateral() external view returns (uint256)
```

Returns the total collateral held by all validators.

### getTotalValidatorCollateral

```solidity
function getTotalValidatorCollateral(address validator) external view returns (uint256)
```

Returns the total collateral amount for a specific validator.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validator | address | The address of the validator for which collateral is queried. |

### getPower

```solidity
function getPower(address validator) external view returns (uint256)
```

Checks if the validator address is in an active state.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validator | address | The address of the checked validator |

### isActiveValidator

```solidity
function isActiveValidator(address validator) external view returns (bool)
```

Checks if the validator address is an active validator

### isWaitingValidator

```solidity
function isWaitingValidator(address validator) external view returns (bool)
```

Checks if the validator is in a waiting state.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validator | address | The address of the checked validator. |

### bottomUpCheckpointAtEpoch

```solidity
function bottomUpCheckpointAtEpoch(uint256 epoch) public view returns (bool exists, struct BottomUpCheckpoint checkpoint)
```

returns the committed bottom-up checkpoint at specific epoch.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| epoch | uint256 | - the epoch to check. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| exists | bool | - whether the checkpoint exists. |
| checkpoint | struct BottomUpCheckpoint | - the checkpoint struct. |

### bottomUpCheckpointHashAtEpoch

```solidity
function bottomUpCheckpointHashAtEpoch(uint256 epoch) external view returns (bool, bytes32)
```

returns the historical committed bottom-up checkpoint hash.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| epoch | uint256 | - the epoch to check |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | exists - whether the checkpoint exists |
| [1] | bytes32 | hash - the hash of the checkpoint |

### powerScale

```solidity
function powerScale() external view returns (int8)
```

Returns the power scale in number of decimals from whole FIL.

### getBootstrapNodes

```solidity
function getBootstrapNodes() external view returns (string[])
```

Returns the bootstrap nodes addresses.

### crossMsgsHash

```solidity
function crossMsgsHash(struct IpcEnvelope[] messages) external pure returns (bytes32)
```

Computes a hash of an array of IpcEnvelopes.

_This exists for testing purposes._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| messages | struct IpcEnvelope[] | An array of cross-chain envelopes to be hashed. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bytes32 | The keccak256 hash of the encoded cross-chain messages. |

### supplySource

```solidity
function supplySource() external view returns (struct SupplySource supply)
```

Returns the supply strategy for the subnet.

