# DomainsV1PortfolioRenewalRenewalInformationResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name | [optional] [default to undefined]
**status** | **string** | Domain status | [optional] [default to undefined]
**expires_at** | **string** | Domain expiration date | [optional] [default to undefined]
**is_grace_period** | **boolean** | Whether the domain is in its post-expiration grace period | [optional] [default to undefined]
**grace_period_ends_at** | **string** | When the grace period ends, set even when the domain is not in it | [optional] [default to undefined]
**is_redemption_period** | **boolean** | Whether the domain is in its redemption period | [optional] [default to undefined]
**redemption_period_ends_at** | **string** | When the redemption period ends, set even when the domain is not in it | [optional] [default to undefined]
**is_renewable** | **boolean** | Whether the domain can be renewed | [optional] [default to undefined]

## Example

```typescript
import { DomainsV1PortfolioRenewalRenewalInformationResource } from '@hostinger/sdk';

const instance: DomainsV1PortfolioRenewalRenewalInformationResource = {
    domain,
    status,
    expires_at,
    is_grace_period,
    grace_period_ends_at,
    is_redemption_period,
    redemption_period_ends_at,
    is_renewable,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
