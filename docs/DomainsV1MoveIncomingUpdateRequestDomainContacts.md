# DomainsV1MoveIncomingUpdateRequestDomainContacts

WHOIS profiles of the accepting account. Only the contact types required by the TLD are applied, but all four IDs must be provided.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**owner_id** | **number** | Owner contact WHOIS record ID | [default to undefined]
**admin_id** | **number** | Administrative contact WHOIS record ID | [default to undefined]
**billing_id** | **number** | Billing contact WHOIS record ID | [default to undefined]
**tech_id** | **number** | Technical contact WHOIS record ID | [default to undefined]

## Example

```typescript
import { DomainsV1MoveIncomingUpdateRequestDomainContacts } from '@hostinger/sdk';

const instance: DomainsV1MoveIncomingUpdateRequestDomainContacts = {
    owner_id,
    admin_id,
    billing_id,
    tech_id,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
