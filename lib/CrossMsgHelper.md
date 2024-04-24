# Solidity API

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

