# Solidity API

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

