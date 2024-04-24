# Solidity API

## FunctionNotFound

```solidity
error FunctionNotFound(bytes4 _functionSelector)
```

## FEATURE_MULTILEVEL_CROSSMSG

```solidity
bool FEATURE_MULTILEVEL_CROSSMSG
```

## FEATURE_GENERAL_PUPRPOSE_CROSSMSG

```solidity
bool FEATURE_GENERAL_PUPRPOSE_CROSSMSG
```

## FEATURE_SUBNET_DEPTH

```solidity
uint8 FEATURE_SUBNET_DEPTH
```

## GatewayDiamond

### s

```solidity
struct GatewayActorStorage s
```

### ConstructorParams

```solidity
struct ConstructorParams {
  uint256 bottomUpCheckPeriod;
  uint16 activeValidatorsLimit;
  uint8 majorityPercentage;
  struct SubnetID networkName;
  struct Validator[] genesisValidators;
  bytes32 commitSha;
}
```

### constructor

```solidity
constructor(struct IDiamond.FacetCut[] _diamondCut, struct GatewayDiamond.ConstructorParams params) public
```

### _fallback

```solidity
function _fallback() internal
```

### fallback

```solidity
fallback() external payable
```

Will run when no functions matches call data

### receive

```solidity
receive() external payable
```

Same as fallback but called when calldata is empty

## BURNT_FUNDS_ACTOR

```solidity
address BURNT_FUNDS_ACTOR
```

## EMPTY_HASH

```solidity
bytes32 EMPTY_HASH
```

## EMPTY_BYTES

```solidity
bytes EMPTY_BYTES
```

## METHOD_SEND

```solidity
bytes4 METHOD_SEND
```

## VALIDATOR_SECP256K1_PUBLIC_KEY_LENGTH

```solidity
uint256 VALIDATOR_SECP256K1_PUBLIC_KEY_LENGTH
```

## ConsensusType

```solidity
enum ConsensusType {
  Fendermint
}
```

## IPCMsgType

```solidity
enum IPCMsgType {
  TopDown,
  BottomUp
}
```

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

## GatewayGetterFacet

### s

```solidity
struct GatewayActorStorage s
```

### getCommitSha

```solidity
function getCommitSha() external view returns (bytes32)
```

Returns code commit SHA where this contract is from.

### bottomUpNonce

```solidity
function bottomUpNonce() external view returns (uint64)
```

Returns the current nonce for bottom-up message processing.

### totalSubnets

```solidity
function totalSubnets() external view returns (uint64)
```

Returns the total number of the registered subnets.

### maxMsgsPerBottomUpBatch

```solidity
function maxMsgsPerBottomUpBatch() external view returns (uint64)
```

Returns the maximum number of messages per bottom-up batch.

### bottomUpCheckPeriod

```solidity
function bottomUpCheckPeriod() external view returns (uint256)
```

Returns the period for bottom-up checkpointing.

### getNetworkName

```solidity
function getNetworkName() external view returns (struct SubnetID)
```

Returns the subnet identifier of the network.

### bottomUpCheckpoint

```solidity
function bottomUpCheckpoint(uint256 e) external view returns (struct BottomUpCheckpoint)
```

Returns a specific bottom-up checkpoint based on an epoch number.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| e | uint256 | The epoch number of the checkpoint. |

### bottomUpMsgBatch

```solidity
function bottomUpMsgBatch(uint256 e) external view returns (struct BottomUpMsgBatch)
```

Returns a specific bottom-up message batch based on an index.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| e | uint256 | The epoch number of the batch. |

### getParentFinality

```solidity
function getParentFinality(uint256 blockNumber) external view returns (struct ParentFinality)
```

Returns the parent chain finality information for a given block number.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| blockNumber | uint256 | The block number for which to retrieve parent-finality information. |

### getLatestParentFinality

```solidity
function getLatestParentFinality() external view returns (struct ParentFinality)
```

Gets the most recent parent-finality information from the parent.

### getSubnet

```solidity
function getSubnet(struct SubnetID subnetId) external view returns (bool, struct Subnet)
```

Returns the subnet with the given id.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | the id of the subnet. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | found whether the subnet exists. |
| [1] | struct Subnet | subnet -  the subnet struct. |

### subnets

```solidity
function subnets(bytes32 h) external view returns (struct Subnet subnet)
```

Returns information about a specific subnet using its hash identifier.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| h | bytes32 | The hash identifier of the subnet to be queried. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnet | struct Subnet | The subnet information corresponding to the given hash. |

### getSubnetTopDownMsgsLength

```solidity
function getSubnetTopDownMsgsLength(struct SubnetID subnetId) external view returns (uint256)
```

Returns the length of the top-down message queue for a specified subnet.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | The identifier of the subnet for which the message queue length is queried. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | The current length of the top-down message queue, indicated by the subnet's top-down nonce. |

### getTopDownNonce

```solidity
function getTopDownNonce(struct SubnetID subnetId) external view returns (bool, uint64)
```

Returns the current applied top-down nonce for a specified subnet, indicating whether it's registered.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | The identifier of the subnet for which the top-down nonce is queried. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | A tuple containing a boolean indicating if the subnet is registered and the current top-down nonce. |
| [1] | uint64 |  |

### getAppliedBottomUpNonce

```solidity
function getAppliedBottomUpNonce(struct SubnetID subnetId) external view returns (bool, uint64)
```

Returns the current applied bottom-up nonce for a specified subnet, indicating whether it's registered.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | The identifier of the subnet for which the bottom-up nonce is queried. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | A tuple containing a boolean indicating if the subnet is registered and the current applied bottom-up nonce. |
| [1] | uint64 |  |

### appliedTopDownNonce

```solidity
function appliedTopDownNonce() external view returns (uint64)
```

Returns the current applied top-down nonce of the gateway.

### postbox

```solidity
function postbox(bytes32 id) external view returns (struct IpcEnvelope storableMsg)
```

Returns the storable message and its wrapped status from the postbox by a given identifier.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| id | bytes32 | The unique identifier of the message in the postbox. |

### majorityPercentage

```solidity
function majorityPercentage() external view returns (uint64)
```

Returns the majority percentage required for certain consensus or decision-making processes.

### listSubnets

```solidity
function listSubnets() external view returns (struct Subnet[])
```

Returns the list of registered subnets.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct Subnet[] | The list of the registered subnets. |

### getSubnetKeys

```solidity
function getSubnetKeys() external view returns (bytes32[])
```

Returns the subnet keys.

### getLastMembership

```solidity
function getLastMembership() external view returns (struct Membership)
```

Returns the last membership received from the parent.

### getLastConfigurationNumber

```solidity
function getLastConfigurationNumber() external view returns (uint64)
```

Returns the last configuration number received from the parent.

### getCurrentMembership

```solidity
function getCurrentMembership() external view returns (struct Membership)
```

Returns the current membership.

### getCurrentConfigurationNumber

```solidity
function getCurrentConfigurationNumber() external view returns (uint64)
```

Returns the current configuration number.

### getCheckpointInfo

```solidity
function getCheckpointInfo(uint256 h) external view returns (struct QuorumInfo)
```

Returns quorum information for a specific checkpoint based on its height.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| h | uint256 | The block height of the checkpoint. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct QuorumInfo | Quorum information associated with the given checkpoint height. |

### getCheckpointCurrentWeight

```solidity
function getCheckpointCurrentWeight(uint256 h) external view returns (uint256)
```

Returns the checkpoint current weight corresponding to the block height.

### getIncompleteCheckpointHeights

```solidity
function getIncompleteCheckpointHeights() external view returns (uint256[])
```

Returns the incomplete checkpoint heights.

### getIncompleteCheckpoints

```solidity
function getIncompleteCheckpoints() external view returns (struct BottomUpCheckpoint[])
```

Returns the incomplete checkpoints.

### getCheckpointRetentionHeight

```solidity
function getCheckpointRetentionHeight() external view returns (uint256)
```

Returns the bottom-up checkpoint retention index.

### getQuorumThreshold

```solidity
function getQuorumThreshold(uint256 totalWeight) external view returns (uint256)
```

Returns the threshold required for quorum in this subnet,
        based on the configured majority percentage and the total weight of the validators.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| totalWeight | uint256 | The total weight to consider for calculating the quorum threshold. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | The quorum threshold derived from the total weight and majority percentage. |

### getCheckpointSignatureBundle

```solidity
function getCheckpointSignatureBundle(uint256 h) external view returns (struct BottomUpCheckpoint ch, struct QuorumInfo info, address[] signatories, bytes[] signatures)
```

Retrieves a bundle of information and signatures for a specified bottom-up checkpoint.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| h | uint256 | The height of the checkpoint for which information is requested. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| ch | struct BottomUpCheckpoint | The checkpoint information at the specified height. |
| info | struct QuorumInfo | Quorum information related to the checkpoint. |
| signatories | address[] | An array of addresses of signatories who have signed the checkpoint. |
| signatures | bytes[] |  |

### getCurrentBottomUpCheckpoint

```solidity
function getCurrentBottomUpCheckpoint() external view returns (bool exists, uint256 epoch, struct BottomUpCheckpoint checkpoint)
```

Returns the current bottom-up checkpoint.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| exists | bool | - whether the checkpoint exists |
| epoch | uint256 | - the epoch of the checkpoint |
| checkpoint | struct BottomUpCheckpoint | - the checkpoint struct |

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

## ERR_GENERAL_CROSS_MSG_DISABLED

```solidity
string ERR_GENERAL_CROSS_MSG_DISABLED
```

## ERR_MULTILEVEL_CROSS_MSG_DISABLED

```solidity
string ERR_MULTILEVEL_CROSS_MSG_DISABLED
```

## GatewayMessengerFacet

### sendContractXnetMessage

```solidity
function sendContractXnetMessage(struct IpcEnvelope envelope) external payable returns (struct IpcEnvelope committed)
```

_Sends a general-purpose cross-message from the local subnet to the destination subnet.
Any value in msg.value will be forwarded in the call.

IMPORTANT: Only smart contracts are allowed to trigger these cross-net messages. User wallets can send funds
from their address to the destination subnet and then run the transaction in the destination normally._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| envelope | struct IpcEnvelope | - the original envelope, which will be validated, stamped and committed during the send. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| committed | struct IpcEnvelope | envelope. |

### propagate

```solidity
function propagate(bytes32 msgCid) external payable
```

_propagates the populated cross net message for the given cid_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| msgCid | bytes32 | - the cid of the cross-net message |

## CheckpointingFacet

### commitCheckpoint

```solidity
function commitCheckpoint(struct BottomUpCheckpoint checkpoint) external
```

submit a verified checkpoint in the gateway to trigger side-effects.

_this method is called by the corresponding subnet actor.
    Called from a subnet actor if the checkpoint is cryptographically valid._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| checkpoint | struct BottomUpCheckpoint | The bottom-up checkpoint to be committed. |

### createBottomUpCheckpoint

```solidity
function createBottomUpCheckpoint(struct BottomUpCheckpoint checkpoint, bytes32 membershipRootHash, uint256 membershipWeight) external
```

creates a new bottom-up checkpoint

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| checkpoint | struct BottomUpCheckpoint | - a bottom-up checkpoint |
| membershipRootHash | bytes32 | - a root hash of the Merkle tree built from the validator public keys and their weight |
| membershipWeight | uint256 | - the total weight of the membership |

### pruneBottomUpCheckpoints

```solidity
function pruneBottomUpCheckpoints(uint256 newRetentionHeight) external
```

Set a new checkpoint retention height and garbage collect all checkpoints in range [`retentionHeight`, `newRetentionHeight`)

_`retentionHeight` is the height of the first incomplete checkpointswe must keep to implement checkpointing.
All checkpoints with a height less than `retentionHeight` are removed from the history, assuming they are committed to the parent._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| newRetentionHeight | uint256 | - the height of the oldest checkpoint to keep |

### addCheckpointSignature

```solidity
function addCheckpointSignature(uint256 height, bytes32[] membershipProof, uint256 weight, bytes signature) external
```

checks whether the provided checkpoint signature for the block at height `height` is valid and accumulates that it

_If adding the signature leads to reaching the threshold, then the checkpoint is removed from `incompleteCheckpoints`_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| height | uint256 | - the height of the block in the checkpoint |
| membershipProof | bytes32[] | - a Merkle proof that the validator was in the membership at height `height` with weight `weight` |
| weight | uint256 | - the weight of the validator |
| signature | bytes | - the signature of the checkpoint |

### execBottomUpMsgs

```solidity
function execBottomUpMsgs(struct IpcEnvelope[] msgs, struct Subnet subnet) internal
```

submit a batch of cross-net messages for execution.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| msgs | struct IpcEnvelope[] | The batch of bottom-up cross-network messages to be executed. |
| subnet | struct Subnet |  |

## TopDownFinalityFacet

### commitParentFinality

```solidity
function commitParentFinality(struct ParentFinality finality) external returns (bool hasCommittedBefore, struct ParentFinality previousFinality)
```

commit the ipc parent finality into storage and returns the previous committed finality
This is useful to understand if the finalities are consistent or if there have been reorgs.
If there are no previous committed fainality, it will be default to zero values, i.e. zero height and block hash.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| finality | struct ParentFinality | - the parent finality |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| hasCommittedBefore | bool | A flag that indicates if a finality record has been committed before. |
| previousFinality | struct ParentFinality | The previous finality information. |

### storeValidatorChanges

```solidity
function storeValidatorChanges(struct StakingChangeRequest[] changeRequests) external
```

Store the validator change requests from parent.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| changeRequests | struct StakingChangeRequest[] | - the validator changes |

### applyFinalityChanges

```solidity
function applyFinalityChanges() external returns (uint64)
```

Apply all changes committed through the commitment of parent finality.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint64 | configurationNumber The configuration number of the changes set that has been confirmed. |

## XnetMessagingFacet

### applyCrossMessages

```solidity
function applyCrossMessages(struct IpcEnvelope[] crossMsgs) external
```

Applies top-down cross-net messages locally. This is invoked by IPC nodes when drawing messages from
        their parent subnet for local execution. That's why the sender is restricted to the system sender,
        because this method is implicitly invoked by the node during block production.

_It requires the caller to be the system actor._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| crossMsgs | struct IpcEnvelope[] | The array of cross-network messages to be applied. |

## IDiamond

### FacetCutAction

```solidity
enum FacetCutAction {
  Add,
  Replace,
  Remove
}
```

### FacetCut

```solidity
struct FacetCut {
  address facetAddress;
  enum IDiamond.FacetCutAction action;
  bytes4[] functionSelectors;
}
```

### DiamondCut

```solidity
event DiamondCut(struct IDiamond.FacetCut[] _diamondCut, address _init, bytes _calldata)
```

## IDiamondCut

### diamondCut

```solidity
function diamondCut(struct IDiamond.FacetCut[] _diamondCut, address _init, bytes _calldata) external
```

Add/replace/remove any number of functions and optionally execute a function with delegatecall

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _diamondCut | struct IDiamond.FacetCut[] | Contains the facet addresses and function selectors |
| _init | address | The address of the contract or facet to execute _calldata |
| _calldata | bytes | A function call, including function selector and arguments _calldata is executed with delegatecall on `_init` |

## IDiamondLoupe

### Facet

These functions are expected to be called frequently
by tools.

```solidity
struct Facet {
  address facetAddress;
  bytes4[] functionSelectors;
}
```

### facets

```solidity
function facets() external view returns (struct IDiamondLoupe.Facet[] facets_)
```

Gets all facet addresses and their four byte function selectors.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| facets_ | struct IDiamondLoupe.Facet[] | Facet |

### facetFunctionSelectors

```solidity
function facetFunctionSelectors(address _facet) external view returns (bytes4[] facetFunctionSelectors_)
```

Gets all the function selectors supported by a specific facet.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _facet | address | The facet address. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| facetFunctionSelectors_ | bytes4[] |  |

### facetAddresses

```solidity
function facetAddresses() external view returns (address[] facetAddresses_)
```

Get all the facet addresses used by a diamond.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| facetAddresses_ | address[] |  |

### facetAddress

```solidity
function facetAddress(bytes4 _functionSelector) external view returns (address facetAddress_)
```

Gets the facet that supports the given selector.

_If facet is not found return address(0)._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _functionSelector | bytes4 | The function selector. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| facetAddress_ | address | The facet address. |

## IERC165

### supportsInterface

```solidity
function supportsInterface(bytes4 interfaceId) external view returns (bool)
```

Query if a contract implements an interface

_Interface identification is specified in ERC-165. This function
 uses less than 30,000 gas._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| interfaceId | bytes4 | The interface identifier, as specified in ERC-165 |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | `true` if the contract implements `interfaceID` and  `interfaceID` is not 0xffffffff, `false` otherwise |

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

## AccountHelper

### isSystemActor

```solidity
function isSystemActor(address _address) external pure returns (bool)
```

## CrossMsgHelper

### CannotExecuteEmptyEnvelope

```solidity
error CannotExecuteEmptyEnvelope()
```

### createTransferMsg

```solidity
function createTransferMsg(struct IPCAddress from, struct IPCAddress to, uint256 value) public pure returns (struct IpcEnvelope)
```

### createCallMsg

```solidity
function createCallMsg(struct IPCAddress from, struct IPCAddress to, uint256 value, bytes4 method, bytes params) public pure returns (struct IpcEnvelope)
```

### createResultMsg

```solidity
function createResultMsg(struct IpcEnvelope crossMsg, enum OutcomeType outcome, bytes ret) public pure returns (struct IpcEnvelope)
```

Creates a receipt message for the given envelope.
It reverts the from and to to return to the original sender
and identifies the receipt through the hash of the original message.

### createReleaseMsg

```solidity
function createReleaseMsg(struct SubnetID subnet, address signer, struct FvmAddress to, uint256 value) public pure returns (struct IpcEnvelope)
```

### createFundMsg

```solidity
function createFundMsg(struct SubnetID subnet, address signer, struct FvmAddress to, uint256 value) public pure returns (struct IpcEnvelope)
```

### applyType

```solidity
function applyType(struct IpcEnvelope message, struct SubnetID currentSubnet) public pure returns (enum IPCMsgType)
```

### toHash

```solidity
function toHash(struct IpcEnvelope crossMsg) internal pure returns (bytes32)
```

### toHash

```solidity
function toHash(struct IpcEnvelope[] crossMsgs) public pure returns (bytes32)
```

### isEmpty

```solidity
function isEmpty(struct IpcEnvelope crossMsg) internal pure returns (bool)
```

### execute

```solidity
function execute(struct IpcEnvelope crossMsg, struct SupplySource supplySource) public returns (bool success, bytes ret)
```

Executes a cross message envelope.

This function doesn't revert except if the envelope is empty.
It returns a success flag and the return data for the success or
the error so it can be returned to the sender through a cross-message receipt.
NOTE: Execute assumes that the fund it is handling have already been
released for their use so they can be conveniently included in the
forwarded message, or the receipt in the case of failure.

### isSorted

```solidity
function isSorted(struct IpcEnvelope[] crossMsgs) external pure returns (bool)
```

## FvmAddressHelper

### SECP256K1

```solidity
uint8 SECP256K1
```

f1: SECP256K1 key address, 20 byte hash of PublicKey.

### PAYLOAD_HASH_LEN

```solidity
uint8 PAYLOAD_HASH_LEN
```

### DELEGATED

```solidity
uint8 DELEGATED
```

For delegated FIL address

### EAM_ACTOR

```solidity
uint64 EAM_ACTOR
```

### NotDelegatedEvmAddress

```solidity
error NotDelegatedEvmAddress()
```

### from

```solidity
function from(address addr) internal pure returns (struct FvmAddress fvmAddress)
```

Creates a FvmAddress from address type

### toHash

```solidity
function toHash(struct FvmAddress fvmAddress) internal pure returns (bytes32)
```

Obtains the hash of the fvm address

### equal

```solidity
function equal(struct FvmAddress a, struct FvmAddress b) internal pure returns (bool)
```

Checks if two fvm addresses are equal

### extractEvmAddress

```solidity
function extractEvmAddress(struct FvmAddress fvmAddress) internal pure returns (address addr)
```

## LibDiamond

### DIAMOND_STORAGE_POSITION

```solidity
bytes32 DIAMOND_STORAGE_POSITION
```

### InvalidAddress

```solidity
error InvalidAddress()
```

### NotOwner

```solidity
error NotOwner()
```

### NoBytecodeAtAddress

```solidity
error NoBytecodeAtAddress(address _contractAddress, string _message)
```

### IncorrectFacetCutAction

```solidity
error IncorrectFacetCutAction(enum IDiamond.FacetCutAction _action)
```

### NoSelectorsProvidedForFacetForCut

```solidity
error NoSelectorsProvidedForFacetForCut(address _facetAddress)
```

### CannotAddFunctionToDiamondThatAlreadyExists

```solidity
error CannotAddFunctionToDiamondThatAlreadyExists(bytes4 _selector)
```

### CannotAddSelectorsToZeroAddress

```solidity
error CannotAddSelectorsToZeroAddress(bytes4[] _selectors)
```

### InitializationFunctionReverted

```solidity
error InitializationFunctionReverted(address _initializationContractAddress, bytes _calldata)
```

### NoSelectorsGivenToAdd

```solidity
error NoSelectorsGivenToAdd()
```

### NotContractOwner

```solidity
error NotContractOwner(address _user, address _contractOwner)
```

### CannotReplaceFunctionsFromFacetWithZeroAddress

```solidity
error CannotReplaceFunctionsFromFacetWithZeroAddress(bytes4[] _selectors)
```

### CannotReplaceImmutableFunction

```solidity
error CannotReplaceImmutableFunction(bytes4 _selector)
```

### CannotReplaceFunctionWithTheSameFunctionFromTheSameFacet

```solidity
error CannotReplaceFunctionWithTheSameFunctionFromTheSameFacet(bytes4 _selector)
```

### CannotReplaceFunctionThatDoesNotExists

```solidity
error CannotReplaceFunctionThatDoesNotExists(bytes4 _selector)
```

### RemoveFacetAddressMustBeZeroAddress

```solidity
error RemoveFacetAddressMustBeZeroAddress(address _facetAddress)
```

### CannotRemoveFunctionThatDoesNotExist

```solidity
error CannotRemoveFunctionThatDoesNotExist(bytes4 _selector)
```

### CannotRemoveImmutableFunction

```solidity
error CannotRemoveImmutableFunction(bytes4 _selector)
```

### OwnershipTransferred

```solidity
event OwnershipTransferred(address oldOwner, address newOwner)
```

### FacetAddressAndSelectorPosition

```solidity
struct FacetAddressAndSelectorPosition {
  address facetAddress;
  uint16 selectorPosition;
}
```

### DiamondStorage

```solidity
struct DiamondStorage {
  mapping(bytes4 => struct LibDiamond.FacetAddressAndSelectorPosition) facetAddressAndSelectorPosition;
  bytes4[] selectors;
  mapping(bytes4 => bool) supportedInterfaces;
  address contractOwner;
}
```

### transferOwnership

```solidity
function transferOwnership(address newOwner) internal
```

_Transfers ownership of the contract to a new account (`newOwner`).
Can only be called by the current owner._

### diamondStorage

```solidity
function diamondStorage() internal pure returns (struct LibDiamond.DiamondStorage ds)
```

### setContractOwner

```solidity
function setContractOwner(address _newOwner) internal
```

### contractOwner

```solidity
function contractOwner() internal view returns (address contractOwner_)
```

### onlyOwner

```solidity
modifier onlyOwner()
```

### enforceIsContractOwner

```solidity
function enforceIsContractOwner() internal view
```

### diamondCut

```solidity
function diamondCut(struct IDiamond.FacetCut[] _diamondCut, address _init, bytes _calldata) internal
```

### addFunctions

```solidity
function addFunctions(address _facetAddress, bytes4[] _functionSelectors) internal
```

### replaceFunctions

```solidity
function replaceFunctions(address _facetAddress, bytes4[] _functionSelectors) internal
```

### removeFunctions

```solidity
function removeFunctions(address _facetAddress, bytes4[] _functionSelectors) internal
```

### initializeDiamondCut

```solidity
function initializeDiamondCut(address _init, bytes _calldata) internal
```

### enforceHasContractCode

```solidity
function enforceHasContractCode(address _contract, string _errorMessage) internal view
```

## LibGateway

### MembershipUpdated

```solidity
event MembershipUpdated(struct Membership)
```

### NewTopDownMessage

```solidity
event NewTopDownMessage(address subnet, struct IpcEnvelope message)
```

_subnet refers to the next "down" subnet that the `envelope.message.to` should be forwarded to._

### NewBottomUpMsgBatch

```solidity
event NewBottomUpMsgBatch(uint256 epoch)
```

_event emitted when there is a new bottom-up message batch to be signed._

### getCurrentBottomUpCheckpoint

```solidity
function getCurrentBottomUpCheckpoint() internal view returns (bool exists, uint256 epoch, struct BottomUpCheckpoint checkpoint)
```

returns the current bottom-up checkpoint

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| exists | bool | - whether the checkpoint exists |
| epoch | uint256 | - the epoch of the checkpoint |
| checkpoint | struct BottomUpCheckpoint | - the checkpoint struct |

### getBottomUpCheckpoint

```solidity
function getBottomUpCheckpoint(uint256 epoch) internal view returns (bool exists, struct BottomUpCheckpoint checkpoint)
```

returns the bottom-up checkpoint

### getBottomUpMsgBatch

```solidity
function getBottomUpMsgBatch(uint256 epoch) internal view returns (bool exists, struct BottomUpMsgBatch batch)
```

returns the bottom-up batch

### bottomUpCheckpointExists

```solidity
function bottomUpCheckpointExists(uint256 epoch) internal view returns (bool)
```

checks if the bottom-up checkpoint already exists at the target epoch

### bottomUpBatchMsgsExists

```solidity
function bottomUpBatchMsgsExists(uint256 epoch) internal view returns (bool)
```

checks if the bottom-up checkpoint already exists at the target epoch

### storeBottomUpCheckpoint

```solidity
function storeBottomUpCheckpoint(struct BottomUpCheckpoint checkpoint) internal
```

stores checkpoint

### storeBottomUpMsgBatch

```solidity
function storeBottomUpMsgBatch(struct BottomUpMsgBatch batch) internal
```

stores bottom-up batch

### getParentFinality

```solidity
function getParentFinality(uint256 blockNumber) internal view returns (struct ParentFinality)
```

obtain the ipc parent finality at certain block number

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| blockNumber | uint256 | - the block number to obtain the finality |

### getLatestParentFinality

```solidity
function getLatestParentFinality() internal view returns (struct ParentFinality)
```

obtain the latest committed ipc parent finality

### commitParentFinality

```solidity
function commitParentFinality(struct ParentFinality finality) internal returns (struct ParentFinality lastFinality)
```

commit the ipc parent finality into storage

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| finality | struct ParentFinality | - the finality to be committed |

### updateMembership

```solidity
function updateMembership(struct Membership membership) internal
```

set the next membership

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| membership | struct Membership | - new membership |

### membershipTotalWeight

```solidity
function membershipTotalWeight(struct Membership self) internal pure returns (uint256)
```

_- Computes total weight for a specific membership_

### membershipEqual

```solidity
function membershipEqual(struct Membership mb1, struct Membership mb2) internal pure returns (bool)
```

_compares two memberships and returns true if they are equal_

### commitTopDownMsg

```solidity
function commitTopDownMsg(struct IpcEnvelope crossMessage) internal
```

commit topdown messages for their execution in the subnet. Adds the message to the subnet struct for future execution

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| crossMessage | struct IpcEnvelope | - the cross message to be committed |

### commitBottomUpMsg

```solidity
function commitBottomUpMsg(struct IpcEnvelope crossMessage) internal
```

Commits a new cross-net message to a message batch for execution

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| crossMessage | struct IpcEnvelope | - the cross message to be committed |

### getSubnet

```solidity
function getSubnet(address actor) internal view returns (bool found, struct Subnet subnet)
```

returns the subnet created by a validator

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| actor | address | the validator that created the subnet |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| found | bool | whether the subnet exists |
| subnet | struct Subnet | -  the subnet struct |

### getSubnet

```solidity
function getSubnet(struct SubnetID subnetId) internal view returns (bool found, struct Subnet subnet)
```

returns the subnet with the given id

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subnetId | struct SubnetID | the id of the subnet |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| found | bool | whether the subnet exists |
| subnet | struct Subnet | -  the subnet struct |

### getNextEpoch

```solidity
function getNextEpoch(uint256 blockNumber, uint256 checkPeriod) internal pure returns (uint256)
```

method that gives the epoch for a given block number and checkpoint period

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | epoch - the epoch for the given block number and checkpoint period |

### applyMessages

```solidity
function applyMessages(struct SubnetID arrivingFrom, struct IpcEnvelope[] crossMsgs) internal
```

applies a cross-net messages coming from some other subnet.
The forwarder argument determines the previous subnet that submitted the checkpoint triggering the cross-net message execution.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| arrivingFrom | struct SubnetID | - the immediate subnet from which this message is arriving |
| crossMsgs | struct IpcEnvelope[] | - the cross-net messages to apply |

### applyMsg

```solidity
function applyMsg(struct SubnetID arrivingFrom, struct IpcEnvelope crossMsg) internal
```

executes a cross message if its destination is the current network, otherwise adds it to the postbox to be propagated further
This function assumes that the relevant funds have been already minted or burnt
when the top-down or bottom-up messages have been queued for execution.
This function is not expected to revert. If a controlled failure happens, a new
cross-message receipt is propagated for execution to inform the sending contract.
`Call` cross-messages also trigger receipts if they are successful.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| arrivingFrom | struct SubnetID | - the immediate subnet from which this message is arriving |
| crossMsg | struct IpcEnvelope | - the cross message to be executed |

### executeCrossMsg

```solidity
function executeCrossMsg(struct IpcEnvelope crossMsg, struct SupplySource supplySource) internal returns (bool success, bytes result)
```

_Execute the cross message using low level `call` method. This way ipc will
     catch contract revert messages as well. We need this because in `CrossMsgHelper.execute`
     there are `require` and `revert` calls, without reflexive call, the execution will
     revert and block the checkpoint submission process._

### sendReceipt

```solidity
function sendReceipt(struct IpcEnvelope original, enum OutcomeType outcomeType, bytes ret) internal
```

Sends a receipt from the execution of a cross-message.
Only `Call` messages trigger a receipt. Transfer messages should be directly
handled by the peer client to return the funds to the from address in the
failing network.
(we could optionally trigger a receipt from `Transfer`s to, but without
multi-level execution it would be adding unnecessary overhead).

### commitCrossMessage

```solidity
function commitCrossMessage(struct IpcEnvelope crossMessage) internal returns (bool shouldBurn)
```

Commit the cross message to storage.

_It also validates that destination subnet ID is not empty
     and not equal to the current network.
     This function assumes that the funds inside `value` have been
     conveniently minted or burnt already and the message is free to
     use them (see execBottomUpMsgBatch for reference).
 @param crossMessage The cross-network message to commit.
 @return shouldBurn A Boolean that indicates if the input amount should be burned._

### crossMsgSideEffects

```solidity
function crossMsgSideEffects(uint256 v, bool shouldBurn) internal
```

_Performs transaction side-effects from the commitment of a cross-net message. Like
burning funds when bottom-up messages are propagated._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| v | uint256 | - the value of the committed cross-net message |
| shouldBurn | bool | - flag if the message should burn funds |

### checkMsgLength

```solidity
function checkMsgLength(struct IpcEnvelope[] msgs) internal view
```

Checks the length of a message batch, ensuring it is in (0, maxMsgsPerBottomUpBatch).

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| msgs | struct IpcEnvelope[] | The batch of messages to check. |

## GatewayActorStorage

```solidity
struct GatewayActorStorage {
  uint256 latestParentHeight;
  uint256 bottomUpCheckPeriod;
  uint256 bottomUpMsgBatchPeriod;
  uint64 bottomUpNonce;
  uint64 appliedTopDownNonce;
  uint64 totalSubnets;
  uint64 maxMsgsPerBottomUpBatch;
  uint8 majorityPercentage;
  bytes32 commitSha;
  uint8 maxTreeDepth;
  bool generalPurposeCrossMsg;
  bool multiLevelCrossMsg;
  struct Membership currentMembership;
  struct Membership lastMembership;
  struct QuorumMap checkpointQuorumMap;
  struct SubnetID networkName;
  struct ParentValidatorsTracker validatorsTracker;
  mapping(bytes32 => struct Subnet) subnets;
  mapping(uint256 => struct ParentFinality) finalitiesMap;
  mapping(bytes32 => struct IpcEnvelope) postbox;
  mapping(uint256 => struct BottomUpCheckpoint) bottomUpCheckpoints;
  mapping(uint256 => struct BottomUpMsgBatch) bottomUpMsgBatches;
  struct EnumerableSet.Bytes32Set subnetKeys;
}
```

## LibGatewayActorStorage

### appStorage

```solidity
function appStorage() internal pure returns (struct GatewayActorStorage ds)
```

## GatewayActorModifiers

### s

```solidity
struct GatewayActorStorage s
```

### systemActorOnly

```solidity
modifier systemActorOnly()
```

## MultisignatureChecker

### Error

```solidity
enum Error {
  Nil,
  InvalidArrayLength,
  EmptySignatures,
  InvalidSignatory,
  InvalidSignature,
  WeightsSumLessThanThreshold
}
```

### isValidWeightedMultiSignature

```solidity
function isValidWeightedMultiSignature(address[] signatories, uint256[] weights, uint256 threshold, bytes32 hash, bytes[] signatures) internal pure returns (bool, enum MultisignatureChecker.Error)
```

Checks if a weighted multi-signature is valid for a given message hash, set of signatories, set of weights, and set of signatures.

_Signatures are validated using `ECDSA.recover`.
     The multi-signature fails if the sum of the signatory weights is less than the threshold.
     Signatories in `signatories` and  signatures in `signatures` must have the same order._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| signatories | address[] | The addresses of the signatories. |
| weights | uint256[] | The weights of the signatories. |
| threshold | uint256 | The number that must be reach to consider `signatures` valid. |
| hash | bytes32 | of the verified data. |
| signatures | bytes[] | Packed signatures. Each signature is in `({bytes32 r}{bytes32 s}{uint8 v})` format. |

## Pausable

Abstract contract that enables contract to pause marked operations

### PausableStorage

```solidity
struct PausableStorage {
  bool paused;
}
```

### Paused

```solidity
event Paused(address account)
```

_Emitted when the pause is triggered by `account`._

### Unpaused

```solidity
event Unpaused(address account)
```

_Emitted when the unpause is triggered by `account`._

### EnforcedPause

```solidity
error EnforcedPause()
```

_The operation failed because the contract is paused._

### ExpectedPause

```solidity
error ExpectedPause()
```

_The operation failed because the contract is not paused._

### whenNotPaused

```solidity
modifier whenNotPaused()
```

_Modifier to make a function callable only when the contract is not paused.

Requirements:

- The contract must not be paused._

### whenPaused

```solidity
modifier whenPaused()
```

_Modifier to make a function callable only when the contract is paused.

Requirements:

- The contract must be paused._

### _requireNotPaused

```solidity
function _requireNotPaused() internal view
```

_Throws if the contract is paused._

### _requirePaused

```solidity
function _requirePaused() internal view
```

_Throws if the contract is not paused._

### _paused

```solidity
function _paused() internal view returns (bool)
```

returns true if the contract is paused

### _pause

```solidity
function _pause() internal
```

_Triggers stopped state.

Requirements:

- The contract must not be paused._

### _unpause

```solidity
function _unpause() internal
```

_Returns to normal state.

Requirements:

- The contract must be paused._

## LibQuorum

### QuorumReached

```solidity
event QuorumReached(enum QuorumObjKind objKind, uint256 height, bytes32 objHash, uint256 quorumWeight)
```

### QuorumWeightUpdated

```solidity
event QuorumWeightUpdated(enum QuorumObjKind objKind, uint256 height, bytes32 objHash, uint256 newWeight)
```

### addQuorumSignature

```solidity
function addQuorumSignature(struct QuorumMap self, uint256 height, bytes32[] membershipProof, uint256 weight, bytes signature) internal
```

checks whether the provided quorum signature for the block at height `height` is valid and accumulates that it

_If adding the signature leads to reaching the threshold, then the info is removed from `incompleteQuorums`_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| self | struct QuorumMap |  |
| height | uint256 | - the height of the block in the checkpoint |
| membershipProof | bytes32[] | - a Merkle proof that the validator was in the membership at height `height` with weight `weight` |
| weight | uint256 | - the weight of the validator |
| signature | bytes | - the signature of the object we are agreen on |

### createQuorumInfo

```solidity
function createQuorumInfo(struct QuorumMap self, uint256 objHeight, bytes32 objHash, bytes32 membershipRootHash, uint256 membershipWeight, uint256 majorityPercentage) internal
```

creates the quorum info from a quorum object.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| self | struct QuorumMap |  |
| objHeight | uint256 | - height of the quorum object |
| objHash | bytes32 | - hash of the object |
| membershipRootHash | bytes32 | - a root hash of the Merkle tree built from the validator public keys and their weight |
| membershipWeight | uint256 | - the total weight of the membership |
| majorityPercentage | uint256 | - the majorityPercentage required to reach quorum |

### pruneQuorums

```solidity
function pruneQuorums(struct QuorumMap self, uint256 newRetentionHeight) internal
```

Sets a new  retention height and garbage collects all checkpoints in range [`retentionHeight`, `newRetentionHeight`)

_`retentionHeight` is the height of the first incomplete checkpointswe must keep to implement checkpointing.
All checkpoints with a height less than `retentionHeight` are removed from the history, assuming they are committed to the parent._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| self | struct QuorumMap |  |
| newRetentionHeight | uint256 | - the height of the oldest checkpoint to keep |

### isHeightAlreadyProcessed

```solidity
function isHeightAlreadyProcessed(struct QuorumMap self, uint256 height) internal view
```

### weightNeeded

```solidity
function weightNeeded(uint256 weight, uint256 majorityPercentage) internal pure returns (uint256)
```

returns the needed weight value corresponding to the majority percentage

_`majorityPercentage` must be a valid number_

### getSignatureBundle

```solidity
function getSignatureBundle(struct QuorumMap self, uint256 h) external view returns (struct QuorumInfo info, address[] signatories, bytes[] signatures)
```

get quorum signature bundle consisting of the info, signatories and the corresponding signatures.

## ReentrancyGuard

Abstract contract to provide protection against reentrancy

### ReentrancyStorage

```solidity
struct ReentrancyStorage {
  uint256 status;
}
```

### ReentrancyError

```solidity
error ReentrancyError()
```

### nonReentrant

```solidity
modifier nonReentrant()
```

## LibAddressStakingReleases

### push

```solidity
function push(struct AddressStakingReleases self, struct StakingRelease release) internal
```

Add new release to the storage. Caller makes sure the release.releasedAt is ordered
in ascending order. This method does not do checks on this.

### compact

```solidity
function compact(struct AddressStakingReleases self) internal returns (uint256, uint16)
```

Perform compaction on releases, i.e. aggregates the amount that can be released
and removes them from storage. Returns the total amount to release and the new
number of pending releases after compaction.

## LibStakingReleaseQueue

The util library for `StakingReleaseQueue`

### NewCollateralRelease

```solidity
event NewCollateralRelease(address validator, uint256 amount, uint256 releaseBlock)
```

### setLockDuration

```solidity
function setLockDuration(struct StakingReleaseQueue self, uint256 blocks) internal
```

### addNewRelease

```solidity
function addNewRelease(struct StakingReleaseQueue self, address validator, uint256 amount) internal
```

Set the amount and time for release collateral

### claim

```solidity
function claim(struct StakingReleaseQueue self, address validator) internal returns (uint256)
```

Validator claim the available collateral that are released

## LibValidatorSet

The util library for `ValidatorSet`

### ActiveValidatorCollateralUpdated

```solidity
event ActiveValidatorCollateralUpdated(address validator, uint256 newPower)
```

### WaitingValidatorCollateralUpdated

```solidity
event WaitingValidatorCollateralUpdated(address validator, uint256 newPower)
```

### NewActiveValidator

```solidity
event NewActiveValidator(address validator, uint256 power)
```

### NewWaitingValidator

```solidity
event NewWaitingValidator(address validator, uint256 power)
```

### ActiveValidatorReplaced

```solidity
event ActiveValidatorReplaced(address oldValidator, address newValidator)
```

### ActiveValidatorLeft

```solidity
event ActiveValidatorLeft(address validator)
```

### WaitingValidatorLeft

```solidity
event WaitingValidatorLeft(address validator)
```

### getPower

```solidity
function getPower(struct ValidatorSet validators, address validator) internal view returns (uint256 power)
```

Get the total voting power for the validator

### getTotalConfirmedCollateral

```solidity
function getTotalConfirmedCollateral(struct ValidatorSet validators) internal view returns (uint256 collateral)
```

Get the total confirmed collateral of the validators.

### totalActiveValidators

```solidity
function totalActiveValidators(struct ValidatorSet validators) internal view returns (uint16 total)
```

Get the total active validators.

### getConfirmedCollateral

```solidity
function getConfirmedCollateral(struct ValidatorSet validators, address validator) internal view returns (uint256 collateral)
```

Get the confirmed collateral of the validator.

### listActiveValidators

```solidity
function listActiveValidators(struct ValidatorSet validators) internal view returns (address[] addresses)
```

### getTotalActivePower

```solidity
function getTotalActivePower(struct ValidatorSet validators) internal view returns (uint256 collateral)
```

Get the total collateral of *active* validators.

### getTotalCollateral

```solidity
function getTotalCollateral(struct ValidatorSet validators) internal view returns (uint256 collateral)
```

Get the total collateral of the *waiting* and *active* validators.

### getTotalPowerOfValidators

```solidity
function getTotalPowerOfValidators(struct ValidatorSet validators, address[] addresses) internal view returns (uint256[])
```

Get the total power of the validators.
The function reverts if at least one validator is not in the active validator set.

### isActiveValidator

```solidity
function isActiveValidator(struct ValidatorSet self, address validator) internal view returns (bool)
```

### setMetadata

```solidity
function setMetadata(struct ValidatorSet validators, address validator, bytes metadata) internal
```

Set validator data

### recordDeposit

```solidity
function recordDeposit(struct ValidatorSet validators, address validator, uint256 amount) internal
```

Validator increases its total collateral by amount.

### recordWithdraw

```solidity
function recordWithdraw(struct ValidatorSet validators, address validator, uint256 amount) internal
```

Validator reduces its total collateral by amount.

### confirmFederatedPower

```solidity
function confirmFederatedPower(struct ValidatorSet self, address validator, uint256 power) internal
```

Validator's federated power was updated by admin

### confirmDeposit

```solidity
function confirmDeposit(struct ValidatorSet self, address validator, uint256 amount) internal
```

### confirmWithdraw

```solidity
function confirmWithdraw(struct ValidatorSet self, address validator, uint256 amount) internal
```

### increaseReshuffle

```solidity
function increaseReshuffle(struct ValidatorSet self, address maybeActive, uint256 newPower) internal
```

Reshuffles the active and waiting validators when an increase in power is confirmed

### reduceReshuffle

```solidity
function reduceReshuffle(struct ValidatorSet self, address validator, uint256 newPower) internal
```

Reshuffles the active and waiting validators when a power reduction is confirmed

## LibStaking

### INITIAL_CONFIGURATION_NUMBER

```solidity
uint64 INITIAL_CONFIGURATION_NUMBER
```

### ConfigurationNumberConfirmed

```solidity
event ConfigurationNumberConfirmed(uint64 number)
```

### CollateralClaimed

```solidity
event CollateralClaimed(address validator, uint256 amount)
```

### getPower

```solidity
function getPower(address validator) internal view returns (uint256 power)
```

### isActiveValidator

```solidity
function isActiveValidator(address validator) internal view returns (bool)
```

Checks if the validator is an active validator

### isWaitingValidator

```solidity
function isWaitingValidator(address validator) internal view returns (bool)
```

Checks if the validator is a waiting validator

### isValidator

```solidity
function isValidator(address addr) internal view returns (bool)
```

Checks if the provided address is a validator (active or waiting) based on its total collateral.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| addr | address | The address to check for validator status. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | A boolean indicating whether the address is a validator. |

### hasStaked

```solidity
function hasStaked(address validator) internal view returns (bool)
```

Checks if the validator has staked before.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| validator | address | The address to check for staking status. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | A boolean indicating whether the validator has staked. |

### totalActiveValidators

```solidity
function totalActiveValidators() internal view returns (uint16)
```

### totalValidators

```solidity
function totalValidators() internal view returns (uint16)
```

Gets the total number of validators, including active and waiting

### getTotalConfirmedCollateral

```solidity
function getTotalConfirmedCollateral() internal view returns (uint256)
```

### getTotalCollateral

```solidity
function getTotalCollateral() internal view returns (uint256)
```

### totalValidatorCollateral

```solidity
function totalValidatorCollateral(address validator) internal view returns (uint256)
```

Gets the total collateral the validators has staked.

### setFederatedPowerWithConfirm

```solidity
function setFederatedPowerWithConfirm(address validator, uint256 power) internal
```

Set the validator federated power directly without queueing the request

### setMetadataWithConfirm

```solidity
function setMetadataWithConfirm(address validator, bytes metadata) internal
```

Set the validator metadata directly without queueing the request

### depositWithConfirm

```solidity
function depositWithConfirm(address validator, uint256 amount) internal
```

Confirm the deposit directly without going through the confirmation process

### withdrawWithConfirm

```solidity
function withdrawWithConfirm(address validator, uint256 amount) internal
```

Confirm the withdraw directly without going through the confirmation process
and releasing from the gateway.

_only use for non-bootstrapped subnets_

### setFederatedPower

```solidity
function setFederatedPower(address validator, bytes metadata, uint256 amount) internal
```

Set the federated power of the validator

### setValidatorMetadata

```solidity
function setValidatorMetadata(address validator, bytes metadata) internal
```

Set the validator metadata

### deposit

```solidity
function deposit(address validator, uint256 amount) internal
```

Deposit the collateral

### withdraw

```solidity
function withdraw(address validator, uint256 amount) internal
```

Withdraw the collateral

### claimCollateral

```solidity
function claimCollateral(address validator) internal
```

Claim the released collateral

### getConfigurationNumbers

```solidity
function getConfigurationNumbers() internal view returns (uint64, uint64)
```

### confirmChange

```solidity
function confirmChange(uint64 configurationNumber) internal
```

Confirm the changes in bottom up checkpoint submission, only call this in bottom up checkpoint execution.

## LibValidatorTracking

The library for tracking validator changes coming from the parent.
Should be used in the child gateway to store changes until they can be applied.

### storeChange

```solidity
function storeChange(struct ParentValidatorsTracker self, struct StakingChangeRequest changeRequest) internal
```

### batchStoreChange

```solidity
function batchStoreChange(struct ParentValidatorsTracker self, struct StakingChangeRequest[] changeRequests) internal
```

### confirmChange

```solidity
function confirmChange(struct ParentValidatorsTracker self, uint64 configurationNumber) internal
```

Confirm the changes in for a finality commitment

## LibStakingChangeLog

The util library for `StakingChangeLog`

### NewStakingChangeRequest

```solidity
event NewStakingChangeRequest(enum StakingOperation op, address validator, bytes payload, uint64 configurationNumber)
```

### metadataRequest

```solidity
function metadataRequest(struct StakingChangeLog changes, address validator, bytes metadata) internal
```

Validator request to update its metadata

### federatedPowerRequest

```solidity
function federatedPowerRequest(struct StakingChangeLog changes, address validator, bytes metadata, uint256 power) internal
```

Records a request to update the federated power of a validator

### withdrawRequest

```solidity
function withdrawRequest(struct StakingChangeLog changes, address validator, uint256 amount) internal
```

Perform upsert operation to the withdraw changes, return total value to withdraw
of the validator.
Each insert will increment the configuration number by 1, update will not.

### depositRequest

```solidity
function depositRequest(struct StakingChangeLog changes, address validator, uint256 amount) internal
```

Perform upsert operation to the deposit changes

### recordChange

```solidity
function recordChange(struct StakingChangeLog changes, address validator, enum StakingOperation op, bytes payload) internal returns (uint64 configurationNumber)
```

Perform upsert operation to the deposit changes

### getChange

```solidity
function getChange(struct StakingChangeLog changes, uint64 configurationNumber) internal view returns (struct StakingChange)
```

Get the change at configuration number

### purgeChange

```solidity
function purgeChange(struct StakingChangeLog changes, uint64 configurationNumber) internal
```

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

## SubnetActorStorage

```solidity
struct SubnetActorStorage {
  uint256 genesisCircSupply;
  uint256 lastBottomUpCheckpointHeight;
  uint256 minActivationCollateral;
  uint256 bottomUpCheckPeriod;
  bytes32 currentSubnetHash;
  address ipcGatewayAddr;
  uint64 maxMsgsPerBottomUpBatch;
  uint8 majorityPercentage;
  int8 powerScale;
  enum ConsensusType consensus;
  bool bootstrapped;
  uint64 minValidators;
  bool killed;
  struct SupplySource supplySource;
  struct SubnetID parentId;
  struct ValidatorSet validatorSet;
  struct StakingChangeLog changeSet;
  struct StakingReleaseQueue releaseQueue;
  mapping(address => string) bootstrapNodes;
  struct EnumerableSet.AddressSet bootstrapOwners;
  mapping(uint256 => struct BottomUpCheckpoint) committedCheckpoints;
  struct Validator[] genesisValidators;
  mapping(address => uint256) genesisBalance;
  address[] genesisBalanceKeys;
}
```

## LibSubnetActorStorage

### appStorage

```solidity
function appStorage() internal pure returns (struct SubnetActorStorage ds)
```

## SubnetActorModifiers

### s

```solidity
struct SubnetActorStorage s
```

### onlyGateway

```solidity
modifier onlyGateway()
```

### notKilled

```solidity
modifier notKilled()
```

## SubnetIDHelper

### NoParentForSubnet

```solidity
error NoParentForSubnet()
```

### NoAddressForRoot

```solidity
error NoAddressForRoot()
```

### EmptySubnet

```solidity
error EmptySubnet()
```

### DifferentRootNetwork

```solidity
error DifferentRootNetwork()
```

### InvalidRoute

```solidity
error InvalidRoute()
```

### getAddress

```solidity
function getAddress(struct SubnetID subnet) public pure returns (address)
```

### getParentSubnet

```solidity
function getParentSubnet(struct SubnetID subnet) public pure returns (struct SubnetID)
```

### toString

```solidity
function toString(struct SubnetID subnet) public pure returns (string)
```

### toHash

```solidity
function toHash(struct SubnetID subnet) public pure returns (bytes32)
```

### createSubnetId

```solidity
function createSubnetId(struct SubnetID subnet, address actor) public pure returns (struct SubnetID newSubnet)
```

### getActor

```solidity
function getActor(struct SubnetID subnet) public pure returns (address)
```

### isRoot

```solidity
function isRoot(struct SubnetID subnet) public pure returns (bool)
```

### equals

```solidity
function equals(struct SubnetID subnet1, struct SubnetID subnet2) public pure returns (bool)
```

### commonParent

```solidity
function commonParent(struct SubnetID subnet1, struct SubnetID subnet2) public pure returns (struct SubnetID)
```

Computes the common parent of the current subnet and the one given as argument

### down

```solidity
function down(struct SubnetID subnet1, struct SubnetID subnet2) public pure returns (struct SubnetID)
```

In the path determined by the current subnet id, it moves
down in the path from the subnet id given as argument.
subnet2 needs to be a prefix of the subnet1.
If subnet1 is /a/b/c/d and subnet2 is /a/b, then the returned ID should be /a/b/c.

_Revert will be triggered if subnet2 is an invalid input._

### isEmpty

```solidity
function isEmpty(struct SubnetID subnetId) public pure returns (bool)
```

## SupplySourceHelper

Helpers to deal with a supply source.

### InvalidERC20Address

```solidity
error InvalidERC20Address()
```

### NoBalanceIncrease

```solidity
error NoBalanceIncrease()
```

### UnexpectedSupplySource

```solidity
error UnexpectedSupplySource()
```

### UnknownSupplySource

```solidity
error UnknownSupplySource()
```

### hasSupplyOfKind

```solidity
function hasSupplyOfKind(address subnetActor, enum SupplyKind compare) internal view returns (bool)
```

Assumes that the address provided belongs to a subnet rooted on this network,
        and checks if its supply kind matches the provided one.
        It reverts if the address does not correspond to a subnet actor.

### validate

```solidity
function validate(struct SupplySource supplySource) internal view
```

Checks that a given supply strategy is correctly formed and its preconditions are met.
        It reverts if conditions are not met.

### expect

```solidity
function expect(struct SupplySource supplySource, enum SupplyKind kind) internal pure
```

Asserts that the supply strategy is of the given kind. If not, it reverts.

### lock

```solidity
function lock(struct SupplySource supplySource, uint256 value) internal returns (uint256)
```

Locks the specified amount from msg.sender into custody.
        Reverts with NoBalanceIncrease if the token balance does not increase.
        May return more than requested for inflationary tokens due to balance rise.

### transferFunds

```solidity
function transferFunds(struct SupplySource supplySource, address payable recipient, uint256 value) internal returns (bool success, bytes ret)
```

Transfers the specified amount out of our treasury to the recipient address.

### ierc20Transfer

```solidity
function ierc20Transfer(struct SupplySource supplySource, address recipient, uint256 value) internal returns (bool success, bytes ret)
```

Wrapper for an IERC20 transfer that bubbles up the success or failure
and the return value instead of reverting so a cross-message receipt can be
triggered from the execution.
This function the `safeTransfer` function used before.

### performCall

```solidity
function performCall(struct SupplySource supplySource, address payable target, bytes data, uint256 value) internal returns (bool success, bytes ret)
```

Calls the target with the specified data, ensuring it receives the specified value.

### functionCallWithERC20Value

```solidity
function functionCallWithERC20Value(struct SupplySource supplySource, address target, bytes data, uint256 value) internal returns (bool success, bytes ret)
```

_Performs the function call with ERC20 value atomically_

### functionCallWithValue

```solidity
function functionCallWithValue(address target, bytes data, uint256 value) internal returns (bool success, bytes)
```

_Adaptation from implementation `openzeppelin-contracts/utils/Address.sol`
that doesn't revert immediately in case of failure and merely notifies of the outcome._

### sendValue

```solidity
function sendValue(address payable recipient, uint256 value) internal returns (bool)
```

_Adaptation from implementation `openzeppelin-contracts/utils/Address.sol`
so it doesn't revert immediately and bubbles up the success of the call

Replacement for Solidity's `transfer`: sends `value` wei to
`recipient`, forwarding all available gas and reverting on errors.

https://eips.ethereum.org/EIPS/eip-1884[EIP1884] increases the gas cost
of certain opcodes, possibly making contracts go over the 2300 gas limit
imposed by `transfer`, making them unable to receive funds via
`transfer`. {sendValue} removes this limitation.

https://diligence.consensys.net/posts/2019/09/stop-using-soliditys-transfer-now/[Learn more].

IMPORTANT: because control is transferred to `recipient`, care must be
taken to not create reentrancy vulnerabilities. Consider using
{ReentrancyGuard} or the
https://solidity.readthedocs.io/en/v0.5.11/security-considerations.html#use-the-checks-effects-interactions-pattern[checks-effects-interactions pattern]._

### balance

```solidity
function balance(struct SupplySource supplySource) internal view returns (uint256 ret)
```

Gets the balance in our treasury.

### native

```solidity
function native() internal pure returns (struct SupplySource)
```

## MaxPQ

```solidity
struct MaxPQ {
  struct PQ inner;
}
```

## LibMaxPQ

The max index priority queue for staking. The same implementation as LibMinPQ, just order compare
is reversed.

### getSize

```solidity
function getSize(struct MaxPQ self) internal view returns (uint16)
```

### getAddress

```solidity
function getAddress(struct MaxPQ self, uint16 i) internal view returns (address)
```

### contains

```solidity
function contains(struct MaxPQ self, address validator) internal view returns (bool)
```

### insert

```solidity
function insert(struct MaxPQ self, struct ValidatorSet validators, address validator) internal
```

Insert the validator address into this PQ.
NOTE that caller should ensure the valdiator is not already in the queue.

### pop

```solidity
function pop(struct MaxPQ self, struct ValidatorSet validators) internal
```

Pop the maximum value in the priority queue.
NOTE that caller should ensure the queue is not empty!

### deleteReheapify

```solidity
function deleteReheapify(struct MaxPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the validator is deleted.
NOTE that caller should ensure the queue is not empty.

### increaseReheapify

```solidity
function increaseReheapify(struct MaxPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the collateral of a key has increased.
NOTE that caller should ensure the queue is not empty.

### decreaseReheapify

```solidity
function decreaseReheapify(struct MaxPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the collateral of a key has decreased.
NOTE that caller should ensure the queue is not empty.

### max

```solidity
function max(struct MaxPQ self, struct ValidatorSet validators) internal view returns (address, uint256)
```

Get the maximum value in the priority queue.
NOTE that caller should ensure the queue is not empty!

### swim

```solidity
function swim(struct MaxPQ self, struct ValidatorSet validators, uint16 pos, uint256 value) internal
```

### sink

```solidity
function sink(struct MaxPQ self, struct ValidatorSet validators, uint16 pos, uint256 value) internal
```

### largerPosition

```solidity
function largerPosition(struct MaxPQ self, struct ValidatorSet validators, uint16 pos1, uint16 pos2) internal view returns (uint16, uint256)
```

Get the larger index of pos1 and pos2.

### firstValueSmaller

```solidity
function firstValueSmaller(uint256 v1, uint256 v2) internal pure returns (bool)
```

## MinPQ

```solidity
struct MinPQ {
  struct PQ inner;
}
```

## LibMinPQ

The min index priority queue for staking

### getSize

```solidity
function getSize(struct MinPQ self) internal view returns (uint16)
```

### getAddress

```solidity
function getAddress(struct MinPQ self, uint16 i) internal view returns (address)
```

### contains

```solidity
function contains(struct MinPQ self, address validator) internal view returns (bool)
```

### insert

```solidity
function insert(struct MinPQ self, struct ValidatorSet validators, address validator) internal
```

Insert the validator address into this PQ.
NOTE that caller should ensure the validator is not already in the queue.

### pop

```solidity
function pop(struct MinPQ self, struct ValidatorSet validators) internal
```

Pop the minimal value in the priority queue.

### deleteReheapify

```solidity
function deleteReheapify(struct MinPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the validator is deleted.

### increaseReheapify

```solidity
function increaseReheapify(struct MinPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the collateral of a key has increased.

### decreaseReheapify

```solidity
function decreaseReheapify(struct MinPQ self, struct ValidatorSet validators, address validator) internal
```

Reheapify the heap when the collateral of a key has decreased.

### min

```solidity
function min(struct MinPQ self, struct ValidatorSet validators) internal view returns (address, uint256)
```

Get the minimal value in the priority queue.
NOTE that caller should ensure the queue is not empty!

### swim

```solidity
function swim(struct MinPQ self, struct ValidatorSet validators, uint16 pos, uint256 value) internal
```

### sink

```solidity
function sink(struct MinPQ self, struct ValidatorSet validators, uint16 pos, uint256 value) internal
```

### smallerPosition

```solidity
function smallerPosition(struct MinPQ self, struct ValidatorSet validators, uint16 pos1, uint16 pos2) internal view returns (uint16, uint256)
```

Get the smaller index of pos1 and pos2.

### firstValueLarger

```solidity
function firstValueLarger(uint256 v1, uint256 v2) internal pure returns (bool)
```

## PQ

The inner data structure for both min and max priority queue

```solidity
struct PQ {
  uint16 size;
  mapping(address => uint16) addressToPos;
  mapping(uint16 => address) posToAddress;
}
```

## LibPQ

### isEmpty

```solidity
function isEmpty(struct PQ self) internal view returns (bool)
```

### requireNotEmpty

```solidity
function requireNotEmpty(struct PQ self) internal view
```

### getSize

```solidity
function getSize(struct PQ self) internal view returns (uint16)
```

### contains

```solidity
function contains(struct PQ self, address validator) internal view returns (bool)
```

### getPosOrRevert

```solidity
function getPosOrRevert(struct PQ self, address validator) internal view returns (uint16 pos)
```

### del

```solidity
function del(struct PQ self, uint16 pos) internal
```

### getPower

```solidity
function getPower(struct PQ self, struct ValidatorSet validators, uint16 pos) internal view returns (uint256)
```

### getConfirmedCollateral

```solidity
function getConfirmedCollateral(struct PQ self, struct ValidatorSet validators, uint16 pos) internal view returns (uint256)
```

### exchange

```solidity
function exchange(struct PQ self, uint16 pos1, uint16 pos2) internal
```

## IpcExchange

### gatewayAddr

```solidity
address gatewayAddr
```

### inflightMsgs

```solidity
mapping(bytes32 => struct IpcEnvelope) inflightMsgs
```

### constructor

```solidity
constructor(address gatewayAddr_) internal
```

### handleIpcMessage

```solidity
function handleIpcMessage(struct IpcEnvelope envelope) external payable returns (bytes)
```

Entrypoint for IPC-enabled contracts. This function is always called by
the gateway when a `Call` or `Receipt` cross-net messages is targeted to
a specific address in the subnet.

### _handleIpcCall

```solidity
function _handleIpcCall(struct IpcEnvelope envelope, struct CallMsg callMsg) internal virtual returns (bytes)
```

Function to be overridden by the child contract to handle incoming IPC calls.

NOTE: It's fine for this method to revert. If that happens, IPC will carry the error to the caller.

### _handleIpcResult

```solidity
function _handleIpcResult(struct IpcEnvelope original, struct IpcEnvelope result, struct ResultMsg resultMsg) internal virtual
```

Function to be overridden by the child contract to handle results from previously performed IPC calls.

NOTE: This must not revert as doing so will leave the correlation map in an inconsistent state.
(IPC will consider the result delivery attempted, and will not repeat it again).

### performIpcCall

```solidity
function performIpcCall(struct IPCAddress to, struct CallMsg callMsg, uint256 value) internal returns (struct IpcEnvelope envelope)
```

Method the implementation of this contract can invoke to perform an IPC call.

### dropMessages

```solidity
function dropMessages(bytes32[] ids) public
```

### onlyGateway

```solidity
modifier onlyGateway()
```

## IIpcHandler

### CallerIsNotGateway

```solidity
error CallerIsNotGateway()
```

### UnsupportedMsgKind

```solidity
error UnsupportedMsgKind()
```

### UnrecognizedResult

```solidity
error UnrecognizedResult()
```

### handleIpcMessage

```solidity
function handleIpcMessage(struct IpcEnvelope envelope) external payable returns (bytes ret)
```

Entrypoint for handling xnet messages in IPC-aware contracts.

## MAX_MSGS_PER_BATCH

```solidity
uint64 MAX_MSGS_PER_BATCH
```

## BATCH_PERIOD

```solidity
uint256 BATCH_PERIOD
```

## ParentFinality

The parent finality for IPC parent at certain height.

```solidity
struct ParentFinality {
  uint256 height;
  bytes32 blockHash;
}
```

## BottomUpCheckpoint

A bottom-up checkpoint type.

```solidity
struct BottomUpCheckpoint {
  struct SubnetID subnetID;
  uint256 blockHeight;
  bytes32 blockHash;
  uint64 nextConfigurationNumber;
  struct IpcEnvelope[] msgs;
}
```

## BottomUpMsgBatch

A batch of bottom-up messages for execution.

```solidity
struct BottomUpMsgBatch {
  struct SubnetID subnetID;
  uint256 blockHeight;
  struct IpcEnvelope[] msgs;
}
```

## BottomUpMsgBatchInfo

Tracks information about the last batch executed.

```solidity
struct BottomUpMsgBatchInfo {
  uint256 blockHeight;
  bytes32 hash;
}
```

## IpcMsgKind

Type of cross-net messages currently supported

```solidity
enum IpcMsgKind {
  Transfer,
  Call,
  Result
}
```

## IpcEnvelope

Envelope used to propagate IPC cross-net messages

```solidity
struct IpcEnvelope {
  enum IpcMsgKind kind;
  struct IPCAddress to;
  struct IPCAddress from;
  uint64 nonce;
  uint256 value;
  bytes message;
}
```

## CallMsg

Message format used for `Transfer` and `Call` messages.

```solidity
struct CallMsg {
  bytes method;
  bytes params;
}
```

## OutcomeType

This struct indicates if the cross message execution is sucess, IPC system error or from the invoked
        contract

```solidity
enum OutcomeType {
  Ok,
  SystemErr,
  ActorErr
}
```

## ResultMsg

```solidity
struct ResultMsg {
  bytes32 id;
  enum OutcomeType outcome;
  bytes ret;
}
```

## FvmAddress

```solidity
struct FvmAddress {
  uint8 addrType;
  bytes payload;
}
```

## DelegatedAddress

```solidity
struct DelegatedAddress {
  uint64 namespace;
  uint128 length;
  bytes buffer;
}
```

## QuorumObjKind

A kind of quorum.

```solidity
enum QuorumObjKind {
  Checkpoint,
  BottomUpMsgBatch
}
```

## QuorumInfo

Checkpoint quorum information.

```solidity
struct QuorumInfo {
  bytes32 hash;
  bytes32 rootHash;
  uint256 threshold;
  uint256 currentWeight;
  bool reached;
}
```

## QuorumMap

A type aggregating quorum related information.

```solidity
struct QuorumMap {
  enum QuorumObjKind quorumObjKind;
  uint256 retentionHeight;
  mapping(uint256 => struct QuorumInfo) quorumInfo;
  struct EnumerableSet.UintSet incompleteQuorums;
  mapping(uint256 => struct EnumerableSet.AddressSet) quorumSignatureSenders;
  mapping(uint256 => mapping(address => bytes)) quorumSignatures;
}
```

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

## SubnetActorCheckpointingFacet

### submitCheckpoint

```solidity
function submitCheckpoint(struct BottomUpCheckpoint checkpoint, address[] signatories, bytes[] signatures) external
```

Submits a checkpoint commitment for execution.

_It triggers the commitment of the checkpoint and any other side-effects that
        need to be triggered by the checkpoint such as relayer reward book keeping._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| checkpoint | struct BottomUpCheckpoint | The executed bottom-up checkpoint. |
| signatories | address[] | The addresses of validators signing the checkpoint. |
| signatures | bytes[] | The signatures of validators on the checkpoint. |

### validateActiveQuorumSignatures

```solidity
function validateActiveQuorumSignatures(address[] signatories, bytes32 hash, bytes[] signatures) public view
```

Checks whether the signatures are valid for the provided signatories and hash within the current validator set.
        Reverts otherwise.

_Signatories in `signatories` and their signatures in `signatures` must be provided in the same order.
      Having it public allows external users to perform sanity-check verification if needed._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| signatories | address[] | The addresses of the signatories. |
| hash | bytes32 | The hash of the checkpoint. |
| signatures | bytes[] | The packed signatures of the checkpoint. |

### ensureValidCheckpoint

```solidity
function ensureValidCheckpoint(struct BottomUpCheckpoint checkpoint) internal view
```

Ensures the checkpoint is valid.

_The checkpoint block height must be equal to the last bottom-up checkpoint height or
the next one or the number of bottom up messages exceeds the max batch size._

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

## OwnershipFacet

### transferOwnership

```solidity
function transferOwnership(address _newOwner) external
```

### owner

```solidity
function owner() external view returns (address owner_)
```

## FunctionNotFound

```solidity
error FunctionNotFound(bytes4 _functionSelector)
```

## SubnetActorDiamond

### s

```solidity
struct SubnetActorStorage s
```

### ConstructorParams

```solidity
struct ConstructorParams {
  uint256 minActivationCollateral;
  uint64 minValidators;
  uint64 bottomUpCheckPeriod;
  address ipcGatewayAddr;
  uint16 activeValidatorsLimit;
  uint8 majorityPercentage;
  enum ConsensusType consensus;
  int8 powerScale;
  enum PermissionMode permissionMode;
  struct SupplySource supplySource;
  struct SubnetID parentId;
}
```

### constructor

```solidity
constructor(struct IDiamond.FacetCut[] _diamondCut, struct SubnetActorDiamond.ConstructorParams params, address owner) public
```

### _fallback

```solidity
function _fallback() internal
```

### fallback

```solidity
fallback() external payable
```

Will run when no functions matches call data

### receive

```solidity
receive() external payable
```

Same as fallback but called when calldata is empty

### onlyGateway

```solidity
modifier onlyGateway()
```

## FunctionNotFound

```solidity
error FunctionNotFound(bytes4 _functionSelector)
```

## SubnetRegistryDiamond

### s

```solidity
struct SubnetRegistryActorStorage s
```

### ConstructorParams

```solidity
struct ConstructorParams {
  address gateway;
  address getterFacet;
  address managerFacet;
  address rewarderFacet;
  address checkpointerFacet;
  address pauserFacet;
  address diamondCutFacet;
  address diamondLoupeFacet;
  address ownershipFacet;
  bytes4[] subnetActorGetterSelectors;
  bytes4[] subnetActorManagerSelectors;
  bytes4[] subnetActorRewarderSelectors;
  bytes4[] subnetActorCheckpointerSelectors;
  bytes4[] subnetActorPauserSelectors;
  bytes4[] subnetActorDiamondCutSelectors;
  bytes4[] subnetActorDiamondLoupeSelectors;
  bytes4[] subnetActorOwnershipSelectors;
  enum SubnetCreationPrivileges creationPrivileges;
}
```

### constructor

```solidity
constructor(struct IDiamond.FacetCut[] _diamondCut, struct SubnetRegistryDiamond.ConstructorParams params) public
```

### _fallback

```solidity
function _fallback() internal
```

### fallback

```solidity
fallback() external payable
```

Will run when no functions matches call data

### receive

```solidity
receive() external payable
```

Same as fallback but called when calldata is empty

## DiamondCutFacet

### diamondCut

```solidity
function diamondCut(struct IDiamond.FacetCut[] _diamondCut, address _init, bytes _calldata) external
```

Add/replace/remove any number of functions and optionally execute
        a function with delegatecall

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _diamondCut | struct IDiamond.FacetCut[] | Contains the facet addresses and function selectors |
| _init | address | The address of the contract or facet to execute _calldata |
| _calldata | bytes | A function call, including function selector and arguments                  _calldata is executed with delegatecall on _init |

## DiamondLoupeFacet

### facets

```solidity
function facets() external view returns (struct IDiamondLoupe.Facet[] facets_)
```

Gets all facets and their selectors.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| facets_ | struct IDiamondLoupe.Facet[] | Facet |

### facetFunctionSelectors

```solidity
function facetFunctionSelectors(address _facet) external view returns (bytes4[] _facetFunctionSelectors)
```

Gets all the function selectors supported by a specific facet.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _facet | address | The facet address. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| _facetFunctionSelectors | bytes4[] | The selectors associated with a facet address. |

### facetAddresses

```solidity
function facetAddresses() external view returns (address[] facetAddresses_)
```

Get all the facet addresses used by a diamond.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| facetAddresses_ | address[] |  |

### facetAddress

```solidity
function facetAddress(bytes4 _functionSelector) external view returns (address facetAddress_)
```

Gets the facet address that supports the given selector.

_If facet is not found return address(0)._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _functionSelector | bytes4 | The function selector. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| facetAddress_ | address | The facet address. |

### supportsInterface

```solidity
function supportsInterface(bytes4 _interfaceId) external view returns (bool)
```

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

## SubnetActorPauseFacet

### pause

```solidity
function pause() external
```

Pauses all contract functions with the `whenNotPaused` modifier.

### unpause

```solidity
function unpause() external
```

Unpauses all contract functions with the `whenNotPaused` modifier.

### paused

```solidity
function paused() external view returns (bool)
```

Returns true if the SubnetActor contract is paused.

## SubnetActorRewardFacet

### claim

```solidity
function claim() external
```

Validator claims their released collateral.

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

