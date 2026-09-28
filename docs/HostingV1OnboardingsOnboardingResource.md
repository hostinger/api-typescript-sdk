# HostingV1OnboardingsOnboardingResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain of the website being set up. | [default to undefined]
**username** | **string** | Hosting account username. | [default to undefined]
**status** | **string** | &#x60;running&#x60; while the website is still being set up, &#x60;completed&#x60; once the setup has finished, &#x60;failed&#x60; when it stopped before finishing or has not reported progress for over an hour. | [default to undefined]
**created_at** | **string** | When the setup was requested. | [default to undefined]
**updated_at** | **string** | When the setup last reported progress. | [default to undefined]

## Example

```typescript
import { HostingV1OnboardingsOnboardingResource } from '@hostinger/sdk';

const instance: HostingV1OnboardingsOnboardingResource = {
    domain,
    username,
    status,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
