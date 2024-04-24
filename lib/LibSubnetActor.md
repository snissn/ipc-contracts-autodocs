# Solidity API

## LibSubnetActor

### SubnetBootstrapped

```solidity
event SubnetBootstrapped(struct Validator[])
```

### enforceCollateralValidation

```solidity
function enforceCollateralValidation() internal view
```

Ensures that the subnet is operating under Collateral-based permission mode.

_Reverts if the subnet is not in Collateral mode._

### enforceFederatedValidation

```solidity
function enforceFederatedValidation() internal view
```

Ensures that the subnet is operating under Federated permission mode.

_Reverts if the subnet is not in Federated mode._

### bootstrapSubnetIfNeeded

```solidity
function bootstrapSubnetIfNeeded() internal
```

_This function is used to bootstrap the subnet,
    if its total collateral is greater than minimum activation collateral._

### publicKeyToAddress

```solidity
function publicKeyToAddress(bytes publicKey) internal pure returns (address)
```

Converts a 65-byte public key to its corresponding address.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| publicKey | bytes | The 65-byte public key to be converted. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | address | The address derived from the given public key. |

### preBootstrapSetFederatedPower

```solidity
function preBootstrapSetFederatedPower(address[] validators, bytes[] publicKeys, uint256[] powers) internal
```

method that allows the contract owner to set the validators' federated power before.
subnet has already been bootstrapped.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validators | address[] | The list of validators' addresses. |
| publicKeys | bytes[] | The list of validators' public keys. |
| powers | uint256[] | The list of power values of the validators. |

### postBootstrapSetFederatedPower

```solidity
function postBootstrapSetFederatedPower(address[] validators, bytes[] publicKeys, uint256[] powers) internal
```

method that allows the contract owner to set the validators' federated power after

_subnet has already been bootstrapped._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validators | address[] | The list of validators' addresses. |
| publicKeys | bytes[] | The list of validators' public keys. |
| powers | uint256[] | The list of power values of the validators. |

### rmAddressFromBalanceKey

```solidity
function rmAddressFromBalanceKey(address addr) internal
```

Removes an address from the initial balance keys.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| addr | address | The address to be removed from the genesis balance keys. |

