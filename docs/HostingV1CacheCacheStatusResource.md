# HostingV1CacheCacheStatusResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_enabled** | **boolean** | Whether server-side caching is enabled for the website | [default to undefined]
**is_cacheless_mode_enabled** | **boolean** | Whether development (cacheless) mode is on. While it is on, caching is bypassed even when &#x60;is_enabled&#x60; is true. Can take a few minutes to follow a cacheless mode toggle. | [default to undefined]

## Example

```typescript
import { HostingV1CacheCacheStatusResource } from '@hostinger/sdk';

const instance: HostingV1CacheCacheStatusResource = {
    is_enabled,
    is_cacheless_mode_enabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
