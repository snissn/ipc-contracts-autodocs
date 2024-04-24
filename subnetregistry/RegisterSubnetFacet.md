# Solidity API

## RegisterSubnetFacet

### s

```solidity
struct SubnetRegistryActorStorage s
```

### SubnetDeployed

```solidity
event SubnetDeployed(address subnetAddr)
```

Event emitted when a new subnet is deployed.

### newSubnetActor

```solidity
function newSubnetActor(struct SubnetActorDiamond.ConstructorParams _params) external returns (address subnetAddr)
```

Deploys a new subnet actor.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _params | struct SubnetActorDiamond.ConstructorParams | The constructor params for Subnet Actor Diamond. |

### ensurePrivileges

```solidity
function ensurePrivileges() internal view
```

