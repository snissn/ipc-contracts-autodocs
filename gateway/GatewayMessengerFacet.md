# Solidity API

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

