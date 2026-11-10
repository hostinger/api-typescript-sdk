# DomainsV1WHOISStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tld** | **string** | TLD of the domain (without leading dot) | [default to undefined]
**country** | **string** | ISO 3166 2-letter country code | [default to undefined]
**entity_type** | **string** | Legal entity type | [default to undefined]
**tld_details** | **object** | TLD-specific details. The required keys depend on the TLD, country and entity type. | [optional] [default to undefined]
**whois_details** | **object** | WHOIS contact details. The required keys depend on the TLD, country and entity type, and can be country-specific (e.g. &#x60;state_lt&#x60; and &#x60;zip_lt&#x60; instead of &#x60;state&#x60; and &#x60;zip&#x60; for Lithuania). | [default to undefined]

## Example

```typescript
import { DomainsV1WHOISStoreRequest } from '@hostinger/sdk';

const instance: DomainsV1WHOISStoreRequest = {
    tld,
    country,
    entity_type,
    tld_details,
    whois_details,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
