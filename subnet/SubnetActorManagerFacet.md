# Solidity API

## SubnetActorManagerFacet

### preFund

```solidity
function preFund() external payable
```

method to add some initial balance into a subnet that hasn't yet bootstrapped.

_This balance is added to user addresses in genesis, and becomes part of the genesis
circulating supply._

### preRelease

```solidity
function preRelease(uint256 amount) external
```

method to remove funds from the initial balance of a subnet.

_This method can be used by users looking to recover part of their
initial balance before the subnet bootstraps._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| amount | uint256 | The amount to remove. |

### setFederatedPower

```solidity
function setFederatedPower(address[] validators, bytes[] publicKeys, uint256[] powers) external
```

Sets the federated power of validators.

_method that allows the contract owner to set the validators' federated power._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validators | address[] | The addresses of validators. |
| publicKeys | bytes[] | The public keys of validators. |
| powers | uint256[] | The federated powers to be assigned to validators. |

### join

```solidity
function join(bytes publicKey) external payable
```

method that allows a validator to join the subnet.
        If the total confirmed collateral of the subnet is greater
        or equal to minimum activation collateral as a result of this operation,
        then  subnet will be registered.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| publicKey | bytes | The off-chain 65 byte public key that should be associated with the validator |

### stake

```solidity
function stake() external payable
```

method that allows a validator to increase its stake.
        If the total confirmed collateral of the subnet is greater
        or equal to minimum activation collateral as a result of this operation,
        then  subnet will be registered.

### unstake

```solidity
function unstake(uint256 amount) external
```

method that allows a validator to unstake a part of its collateral from a subnet.

_`leave` must be used to unstake the entire stake._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| amount | uint256 | The amount to unstake. |

### leave

```solidity
function leave() external
```

method that allows a validator to leave the subnet.

### kill

```solidity
function kill() external
```

method that allows to kill the subnet when all validators left.

_It is not a privileged operation._

### addBootstrapNode

```solidity
function addBootstrapNode(string netAddress) external
```

Add a bootstrap node.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| netAddress | string | The network address of the new bootstrap node. |

