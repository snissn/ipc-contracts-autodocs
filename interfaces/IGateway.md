# Solidity API

## IGateway

### register

```solidity
function register(uint256 genesisCircSupply) external payable
```

Register is called by subnet actors to put the required collateral
and register the subnet to the hierarchy.

### addStake

```solidity
function addStake() external payable
```

AddStake adds stake to the collateral of a subnet.

### releaseStake

```solidity
function releaseStake(uint256 amount) external
```

Release stake recovers some collateral of the subnet

### kill

```solidity
function kill() external
```

Kill propagates the kill signal from a subnet actor to unregister it from th
hierarchy.

### commitCheckpoint

```solidity
function commitCheckpoint(struct BottomUpCheckpoint bottomUpCheckpoint) external
```

commitCheckpoint propagates the commitment of a checkpoint from a child

### fund

```solidity
function fund(struct SubnetID subnetId, struct FvmAddress to) external payable
```

fund locks the received funds —denominated in the native coin— and moves the value down the hierarchy,
crediting the funds to the specified address in the destination network.

This functions ends up minting supply in the subnet equal to the value of the transaction. It does so by
committing the relevant top-down message, updating the top-down nonce along the way.

Calling this method on a subnet whose supply source is not 'native' will revert with UnexpectedSupplySource().

### fundWithToken

```solidity
function fundWithToken(struct SubnetID subnetId, struct FvmAddress to, uint256 amount) external
```

fundWithToken locks the specified amount of tokens in the ERC20 contract linked to the subnet, and
moves the value down the hierarchy, crediting the funds as native coins to the specified address
in the destination network.

This method expects the caller to have approved the gateway to spend `amount` tokens on their behalf
(usually done through IERC20#approve). Tokens are locked by calling IERC20#transferFrom(caller, address(this), amount).
A failure in transferring tokens to the gateway will revert the call.

It's possible to call this method from an EOA or a contract. Regardless, it's recommended to approve strictly
the amount that will subsequently be deposited into the subnet. Keeping outstanding approvals is not recommended.

Calling this method on a subnet whose supply source is not 'ERC20' will revert with UnexpectedSupplySource().

### release

```solidity
function release(struct FvmAddress to) external payable
```

Release creates a new check message to release funds in parent chain

This function burns the funds that will be released in the current subnet
and propagates a new checkpoint message to the parent chain to signal
the amount of funds that can be released for a specific address.

### sendContractXnetMessage

```solidity
function sendContractXnetMessage(struct IpcEnvelope envelope) external payable returns (struct IpcEnvelope committed)
```

sendContractXnetMessage sends an arbitrary cross-message to other subnet in the hierarchy.

### propagate

```solidity
function propagate(bytes32 msgCid) external payable
```

Propagates the stored postbox item for the given cid

### commitParentFinality

```solidity
function commitParentFinality(struct ParentFinality finality) external
```

commit the ipc parent finality into storage

### createBottomUpCheckpoint

```solidity
function createBottomUpCheckpoint(struct BottomUpCheckpoint checkpoint, bytes32 membershipRootHash, uint256 membershipWeight) external
```

creates a new bottom-up checkpoint

