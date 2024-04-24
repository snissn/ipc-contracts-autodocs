# Solidity API

## SubnetGetterFacet

### s

```solidity
struct SubnetRegistryActorStorage s
```

### latestSubnetDeployed

```solidity
function latestSubnetDeployed(address owner) external view returns (address subnet)
```

Returns the address of the latest subnet actor deployed by a user.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| owner | address | The address of the user whose latest subnet deployment is queried. |

### getSubnetDeployedByNonce

```solidity
function getSubnetDeployedByNonce(address owner, uint64 nonce) external view returns (address subnet)
```

Returns the address of a subnet actor deployed for a specific nonce by a user.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| owner | address | The address of the user whose subnet deployment is queried. |
| nonce | uint64 | The specific nonce associated with the subnet deployment. |

### getUserLastNonce

```solidity
function getUserLastNonce(address user) external view returns (uint64 nonce)
```

Returns the last nonce used by the owner.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| user | address | The address of the user whose last nonce is being queried. |

### getGateway

```solidity
function getGateway() external view returns (address)
```

Returns the gateway.

### getSubnetActorGetterFacet

```solidity
function getSubnetActorGetterFacet() external view returns (address)
```

Returns the address of the SUBNET_GETTER_FACET.

### getSubnetActorManagerFacet

```solidity
function getSubnetActorManagerFacet() external view returns (address)
```

Returns the address of the SUBNET_MANAGER_FACET.

### getSubnetActorRewarderFacet

```solidity
function getSubnetActorRewarderFacet() external view returns (address)
```

Returns the address of the SUBNET_ACTOR_REWARDER_FACET.

### getSubnetActorCheckpointerFacet

```solidity
function getSubnetActorCheckpointerFacet() external view returns (address)
```

Returns the address of the SUBNET_ACTOR_CHECKPOINTER_FACET.

### getSubnetActorPauserFacet

```solidity
function getSubnetActorPauserFacet() external view returns (address)
```

Returns the address of the SUBNET_ACTOR_PAUSER_FACET.

### getSubnetActorGetterSelectors

```solidity
function getSubnetActorGetterSelectors() external view returns (bytes4[])
```

Returns the subnet actor getter selectors.

### getSubnetActorManagerSelectors

```solidity
function getSubnetActorManagerSelectors() external view returns (bytes4[])
```

Returns the subnet actor manager selectors.

### getSubnetActorRewarderSelectors

```solidity
function getSubnetActorRewarderSelectors() external view returns (bytes4[])
```

Returns the subnet actor rewarder selectors.

### getSubnetActorCheckpointerSelectors

```solidity
function getSubnetActorCheckpointerSelectors() external view returns (bytes4[])
```

Returns the subnet actor checkpointer selectors.

### getSubnetActorPauserSelectors

```solidity
function getSubnetActorPauserSelectors() external view returns (bytes4[])
```

Returns the subnet actor pauser selectors.

### updateReferenceSubnetContract

```solidity
function updateReferenceSubnetContract(address newGetterFacet, address newManagerFacet, bytes4[] newSubnetGetterSelectors, bytes4[] newSubnetManagerSelectors) external
```

Updates references to the subnet contract components, including facets and selector sets.
Only callable by the contract owner.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| newGetterFacet | address | The address of the new subnet getter facet. |
| newManagerFacet | address | The address of the new subnet manager facet. |
| newSubnetGetterSelectors | bytes4[] | An array of function selectors for the new subnet getter facet. |
| newSubnetManagerSelectors | bytes4[] | An array of function selectors for the new subnet manager facet. |

