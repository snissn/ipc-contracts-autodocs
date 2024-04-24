# Solidity API

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

