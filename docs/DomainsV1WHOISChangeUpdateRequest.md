# DomainsV1WHOISChangeUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**new_whois_id** | **number** | WHOIS profile ID to assign to the domain | [default to undefined]
**domain** | **string** | Domain name | [default to undefined]
**change_for** | **Array&lt;string&gt;** | Contact roles to repoint to the new WHOIS profile | [default to undefined]

## Example

```typescript
import { DomainsV1WHOISChangeUpdateRequest } from '@hostinger/sdk';

const instance: DomainsV1WHOISChangeUpdateRequest = {
    new_whois_id,
    domain,
    change_for,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
