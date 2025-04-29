# DomainsV1WHOISStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tld** | **string** | TLD of the domain (without trailing dot) | [default to undefined]
**country** | **string** | ISO 3166 2-letter country code | [default to undefined]
**entity_type** | **string** | Legal entity type | [default to undefined]
**tld_details** | **object** | TLD details | [optional] [default to undefined]
**whois_details** | **object** | WHOIS details | [default to undefined]

## Example

```typescript
import { DomainsV1WHOISStoreRequest } from 'hostinger-api-sdk';

const instance: DomainsV1WHOISStoreRequest = {
    tld,
    country,
    entity_type,
    tld_details,
    whois_details,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
