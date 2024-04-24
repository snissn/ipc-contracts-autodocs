# Solidity API

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

