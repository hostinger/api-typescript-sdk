# DomainsV1WHOISProfileResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | WHOIS Profile ID | [optional] [default to undefined]
**tld** | **string** | TLD to which contact profile can be applied to | [optional] [default to undefined]
**country** | **string** | ISO 3166 2-letter country code | [optional] [default to undefined]
**entity_type** | **string** | WHOIS profile entity type | [optional] [default to undefined]
**whois_details** | **object** | WHOIS profile details | [optional] [default to undefined]
**tld_details** | **object** | TLD details | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { DomainsV1WHOISProfileResource } from 'hostinger-api-sdk';

const instance: DomainsV1WHOISProfileResource = {
    id,
    tld,
    country,
    entity_type,
    whois_details,
    tld_details,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
