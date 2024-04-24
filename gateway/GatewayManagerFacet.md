# Solidity API

## ERR_CHILD_SUBNET_NOT_ALLOWED

```solidity
string ERR_CHILD_SUBNET_NOT_ALLOWED
```

## GatewayManagerFacet

### register

```solidity
function register(uint256 genesisCircSupply) external payable
```

register a subnet in the gateway. It is called by a subnet when it reaches the threshold stake

_The subnet can optionally pass a genesis circulating supply that would be pre-allocated in the
subnet from genesis (without having to wait for the subnet to be spawned to propagate the funds)._

### addStake

```solidity
function addStake() external payable
```

addStake - add collateral for an existing subnet

### releaseStake

```solidity
function releaseStake(uint256 amount) external
```

release collateral for an existing subnet.

_it can be used to release the stake or reward of the validator._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| amount | uint256 | The amount of stake to be released. |

### kill

```solidity
function kill() external
```

kill an existing subnet.

_The subnet's balance must be empty._

### fund

```solidity
function fund(struct SubnetID subnetId, struct FvmAddress to) external payable
```

credits the received value to the specified address in the specified child subnet.

_There may be an associated fee that gets distributed to validators in the subnet. Currently this fee is zero,
    i.e. funding a subnet is free._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID |  |
| to | struct FvmAddress |  |

### fundWithToken

```solidity
function fundWithToken(struct SubnetID subnetId, struct FvmAddress to, uint256 amount) external
```

Sends funds to a specified subnet receiver using ERC20 tokens.

_This function locks the amount of ERC20 tokens into custody and then mints the supply in the specified subnet.
    It checks if the subnet's supply strategy is ERC20 and if not, the operation is reverted.
    It allows for free injection of funds into a subnet and is protected against reentrancy._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | The ID of the subnet where the funds will be sent to. |
| to | struct FvmAddress | The funded address. |
| amount | uint256 | The amount of ERC20 tokens to be sent. |

### release

```solidity
function release(struct FvmAddress to) external payable
```

release() burns the received value locally in subnet and commits a bottom-up message to release the assets in the parent.
        The local supply of a subnet is always the native coin, so this method doesn't have to deal with tokens.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| to | struct FvmAddress |  |

