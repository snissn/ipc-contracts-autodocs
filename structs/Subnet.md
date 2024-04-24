# Solidity API

## SubnetID

A subnet identity type.

```solidity
struct SubnetID {
  uint64 root;
  address[] route;
}
```

## Subnet

A Subnet type.

```solidity
struct Subnet {
  uint256 stake;
  uint256 genesisEpoch;
  uint256 circSupply;
  uint64 topDownNonce;
  uint64 appliedBottomUpNonce;
  struct SubnetID id;
}
```

## StakingOperation

Subnet staking operations.

```solidity
enum StakingOperation {
  Deposit,
  Withdraw,
  SetMetadata,
  SetFederatedPower
}
```

## StakingChange

The change request to validator staking.

```solidity
struct StakingChange {
  enum StakingOperation op;
  bytes payload;
  address validator;
}
```

## StakingChangeRequest

The change associated with its corresponding configuration number.

```solidity
struct StakingChangeRequest {
  struct StakingChange change;
  uint64 configurationNumber;
}
```

## StakingChangeLog

The collection of staking changes.

```solidity
struct StakingChangeLog {
  uint64 nextConfigurationNumber;
  uint64 startConfigurationNumber;
  mapping(uint64 => struct StakingChange) changes;
}
```

## StakingRelease

Each staking release amount and time.

```solidity
struct StakingRelease {
  uint256 releaseAt;
  uint256 amount;
}
```

## AddressStakingReleases

Tracks the staking releases of an address.

_Mimics the implementation of array in solidity,
        this way is more aligned with our use case._

```solidity
struct AddressStakingReleases {
  uint16 length;
  uint16 startIdx;
  mapping(uint16 => struct StakingRelease) releases;
}
```

## StakingReleaseQueue

Manages the staking release queue.

```solidity
struct StakingReleaseQueue {
  uint256 lockingDuration;
  mapping(address => struct AddressStakingReleases) releases;
}
```

## ValidatorInfo

Keeping track of the validator information.

_There are two types of collaterals:
    - Confirmed: The amount of collateral actually confirmed in child subnet;
    - Total: Aside from Confirmed, there is also the collateral has been supplied, but not yet confirmed in child._

```solidity
struct ValidatorInfo {
  uint256 federatedPower;
  uint256 confirmedCollateral;
  uint256 totalCollateral;
  bytes metadata;
}
```

## PermissionMode

Determines the permission mode for validators.

```solidity
enum PermissionMode {
  Collateral,
  Federated,
  Static
}
```

## SubnetCreationPrivileges

Determines the permission mode for who can create subet

```solidity
enum SubnetCreationPrivileges {
  Unrestricted,
  Owner
}
```

## ValidatorSet

Keeping track of the list of validators.

_There are two types of validators:
    - Active
    - Waiting
Active validators are those that are producing blocks in the child subnet.
Waiting validators are those that do no have as high collateral as Active validators.

The max number of active validators is limited by `activeLimit` and the size of waiting
validators is not bounded.

With each validator staking change, waiting validators can be promoted to active validators
and active validators can be knocked off._

```solidity
struct ValidatorSet {
  enum PermissionMode permissionMode;
  uint16 activeLimit;
  uint256 totalConfirmedCollateral;
  mapping(address => struct ValidatorInfo) validators;
  struct MinPQ activeValidators;
  struct MaxPQ waitingValidators;
}
```

## ParentValidatorsTracker

Tracks the parent validator changes and apply them in the child.

```solidity
struct ParentValidatorsTracker {
  struct ValidatorSet validators;
  struct StakingChangeLog changes;
}
```

## IPCAddress

An IPC address type.

```solidity
struct IPCAddress {
  struct SubnetID subnetId;
  struct FvmAddress rawAddress;
}
```

## Validator

Validator struct stored in the gateway.

```solidity
struct Validator {
  uint256 weight;
  address addr;
  bytes metadata;
}
```

## Membership

Membership information stored in the gateway.

```solidity
struct Membership {
  struct Validator[] validators;
  uint64 configurationNumber;
}
```

## SupplySource

Defines the supply source of a subnet on its parent subnet.

```solidity
struct SupplySource {
  enum SupplyKind kind;
  address tokenAddress;
}
```

## SupplyKind

Determines the type of supply used by the subnet.

```solidity
enum SupplyKind {
  Native,
  ERC20
}
```

