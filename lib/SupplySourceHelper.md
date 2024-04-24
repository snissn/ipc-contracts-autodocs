# Solidity API

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

