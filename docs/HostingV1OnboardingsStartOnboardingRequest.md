# HostingV1OnboardingsStartOnboardingRequest

Website type, domain and WordPress settings for a new website setup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Website type. Omit or &#x60;null&#x60; for an empty website. &#x60;wordpress&#x60; installs WordPress in the website root and requires &#x60;wordpress&#x60;. The headless types (&#x60;headless_wordpress&#x60;, &#x60;headless_ecommerce&#x60;, &#x60;headless_pocketbase&#x60;) create a headless website; &#x60;headless_wordpress&#x60; additionally installs WordPress into the &#x60;cms&#x60; directory with generated credentials. | [optional] [default to undefined]
**domain** | **string** | Customer-owned domain. Cannot start with \&quot;www.\&quot;. Omit or &#x60;null&#x60; to set the website up on a generated temporary free subdomain. | [optional] [default to undefined]
**wordpress** | [**HostingV1OnboardingsStartOnboardingRequestWordpress**](HostingV1OnboardingsStartOnboardingRequestWordpress.md) |  | [optional] [default to undefined]

## Example

```typescript
import { HostingV1OnboardingsStartOnboardingRequest } from '@hostinger/sdk';

const instance: HostingV1OnboardingsStartOnboardingRequest = {
    type,
    domain,
    wordpress,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
