# Solidity API

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

