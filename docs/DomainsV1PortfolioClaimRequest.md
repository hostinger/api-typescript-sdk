# DomainsV1PortfolioClaimRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name | [default to undefined]
**domain_contacts** | [**DomainsV1PortfolioClaimRequestDomainContacts**](DomainsV1PortfolioClaimRequestDomainContacts.md) |  | [optional] [default to undefined]
**additional_details** | **object** | Additional registration data, possible values depends on TLD | [optional] [default to undefined]

## Example

```typescript
import { DomainsV1PortfolioClaimRequest } from '@hostinger/sdk';

const instance: DomainsV1PortfolioClaimRequest = {
    domain,
    domain_contacts,
    additional_details,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
