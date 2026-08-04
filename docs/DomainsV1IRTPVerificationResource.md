# DomainsV1IRTPVerificationResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name | [optional] [default to undefined]
**status** | **string** | IRTP verification status | [optional] [default to undefined]
**old_confirmed_at** | **string** | When the old registrant confirmed the change | [optional] [default to undefined]
**new_confirmed_at** | **string** | When the new registrant confirmed the change | [optional] [default to undefined]
**old_whois_profile_email** | **string** | Email the old registrant confirmation was sent to | [optional] [default to undefined]
**new_whois_profile_email** | **string** | Email the new registrant confirmation was sent to | [optional] [default to undefined]
**expires_at** | **string** | When the verification auto-cancels if unconfirmed | [optional] [default to undefined]

## Example

```typescript
import { DomainsV1IRTPVerificationResource } from 'hostinger-api-sdk';

const instance: DomainsV1IRTPVerificationResource = {
    domain,
    status,
    old_confirmed_at,
    new_confirmed_at,
    old_whois_profile_email,
    new_whois_profile_email,
    expires_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
