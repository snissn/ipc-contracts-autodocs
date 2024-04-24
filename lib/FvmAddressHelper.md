# Solidity API

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

