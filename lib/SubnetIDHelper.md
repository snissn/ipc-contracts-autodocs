# Solidity API

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

