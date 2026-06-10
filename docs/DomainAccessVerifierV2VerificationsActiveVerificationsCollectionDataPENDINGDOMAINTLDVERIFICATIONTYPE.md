# DomainAccessVerifierV2VerificationsActiveVerificationsCollectionDataPENDINGDOMAINTLDVERIFICATIONTYPE

Verification type (\"NAMESERVERS\" or \"TXT\"). Only verification types that exist for this domain will be present.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**records** | **Array&lt;string&gt;** | Verification records | [optional] [default to undefined]
**last_verification_attempt** | **string** | Datetime when last verification attempt occurred | [optional] [default to undefined]
**next_verification_attempt** | **string** | Datetime when next verification attempt will occur | [optional] [default to undefined]
**verification_expiration** | **string** | Datetime when verification expires | [optional] [default to undefined]

## Example

```typescript
import { DomainAccessVerifierV2VerificationsActiveVerificationsCollectionDataPENDINGDOMAINTLDVERIFICATIONTYPE } from 'hostinger-api-sdk';

const instance: DomainAccessVerifierV2VerificationsActiveVerificationsCollectionDataPENDINGDOMAINTLDVERIFICATIONTYPE = {
    records,
    last_verification_attempt,
    next_verification_attempt,
    verification_expiration,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
