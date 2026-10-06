# HostingV1OnboardingsStartOnboardingRequestWordpress

WordPress install settings. Required when `type` is `wordpress`, not allowed otherwise. The site title is the domain.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**language** | **string** | WordPress locale, for example &#x60;en_US&#x60; or &#x60;lt_LT&#x60;. Defaults to &#x60;en_US&#x60; when omitted. | [optional] [default to undefined]
**is_ai_builder** | **boolean** | When &#x60;true&#x60;, installs the Hostinger AI theme (&#x60;hostinger-ai-theme&#x60;). Defaults to &#x60;false&#x60; when omitted. | [optional] [default to undefined]
**admin** | [**HostingV1OnboardingsStartOnboardingRequestWordpressAdmin**](HostingV1OnboardingsStartOnboardingRequestWordpressAdmin.md) |  | [default to undefined]

## Example

```typescript
import { HostingV1OnboardingsStartOnboardingRequestWordpress } from '@hostinger/sdk';

const instance: HostingV1OnboardingsStartOnboardingRequestWordpress = {
    language,
    is_ai_builder,
    admin,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
