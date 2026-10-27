# HostingV1WebsitesTriggerEventRequestEvent

Event to trigger; `name` decides which `params` it takes

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the event: - &#x60;headless_onboarding.tool.connected&#x60;: an AI coding tool started building this website   with the Hostinger headless skill. Takes &#x60;params.tool&#x60;. | [default to undefined]
**params** | [**HostingV1WebsitesTriggerEventRequestEventParams**](HostingV1WebsitesTriggerEventRequestEventParams.md) |  | [default to undefined]

## Example

```typescript
import { HostingV1WebsitesTriggerEventRequestEvent } from '@hostinger/sdk';

const instance: HostingV1WebsitesTriggerEventRequestEvent = {
    name,
    params,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
