# Solidity API

## MultisignatureChecker

### Error

```solidity
enum Error {
  Nil,
  InvalidArrayLength,
  EmptySignatures,
  InvalidSignatory,
  InvalidSignature,
  WeightsSumLessThanThreshold
}
```

### isValidWeightedMultiSignature

```solidity
function isValidWeightedMultiSignature(address[] signatories, uint256[] weights, uint256 threshold, bytes32 hash, bytes[] signatures) internal pure returns (bool, enum MultisignatureChecker.Error)
```

Checks if a weighted multi-signature is valid for a given message hash, set of signatories, set of weights, and set of signatures.

_Signatures are validated using `ECDSA.recover`.
     The multi-signature fails if the sum of the signatory weights is less than the threshold.
     Signatories in `signatories` and  signatures in `signatures` must have the same order._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| signatories | address[] | The addresses of the signatories. |
| weights | uint256[] | The weights of the signatories. |
| threshold | uint256 | The number that must be reach to consider `signatures` valid. |
| hash | bytes32 | of the verified data. |
| signatures | bytes[] | Packed signatures. Each signature is in `({bytes32 r}{bytes32 s}{uint8 v})` format. |

