# Solidity API

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

