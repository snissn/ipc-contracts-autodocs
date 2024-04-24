# Solidity API

## SubnetRegistryActorStorage

```solidity
struct SubnetRegistryActorStorage {
  address GATEWAY;
  address SUBNET_ACTOR_GETTER_FACET;
  address SUBNET_ACTOR_MANAGER_FACET;
  address SUBNET_ACTOR_REWARD_FACET;
  address SUBNET_ACTOR_CHECKPOINTING_FACET;
  address SUBNET_ACTOR_PAUSE_FACET;
  address SUBNET_ACTOR_DIAMOND_CUT_FACET;
  address SUBNET_ACTOR_LOUPE_FACET;
  address SUBNET_ACTOR_OWNERSHIP_FACET;
  bytes4[] subnetActorGetterSelectors;
  bytes4[] subnetActorManagerSelectors;
  bytes4[] subnetActorRewarderSelectors;
  bytes4[] subnetActorCheckpointerSelectors;
  bytes4[] subnetActorPauserSelectors;
  bytes4[] subnetActorDiamondCutSelectors;
  bytes4[] subnetActorDiamondLoupeSelectors;
  bytes4[] subnetActorOwnershipSelectors;
  mapping(address => mapping(uint64 => address)) subnets;
  mapping(address => uint64) userNonces;
  enum SubnetCreationPrivileges creationPrivileges;
}
```

