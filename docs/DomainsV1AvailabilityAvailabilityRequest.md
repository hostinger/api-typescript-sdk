# DomainsV1AvailabilityAvailabilityRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name (without TLD) | [default to undefined]
**tlds** | **Array&lt;string&gt;** | TLDs list | [default to undefined]
**with_alternatives** | **boolean** | Should response include alternatives | [optional] [default to false]

## Example

```typescript
import { DomainsV1AvailabilityAvailabilityRequest } from 'hostinger-api-sdk';

const instance: DomainsV1AvailabilityAvailabilityRequest = {
    domain,
    tlds,
    with_alternatives,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
