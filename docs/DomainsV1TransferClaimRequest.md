# DomainsV1TransferClaimRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name | [default to undefined]
**auth_code** | **string** | Authorization code from the current registrar | [default to undefined]
**domain_contacts** | [**DomainsV1PortfolioClaimRequestDomainContacts**](DomainsV1PortfolioClaimRequestDomainContacts.md) |  | [optional] [default to undefined]
**should_keep_ns** | **boolean** | Keep the existing nameservers of the domain | [optional] [default to true]

## Example

```typescript
import { DomainsV1TransferClaimRequest } from 'hostinger-api-sdk';

const instance: DomainsV1TransferClaimRequest = {
    domain,
    auth_code,
    domain_contacts,
    should_keep_ns,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
