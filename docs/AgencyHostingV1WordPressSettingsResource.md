# AgencyHostingV1WordPressSettingsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**core_version** | **string** | Currently installed WordPress core version, or null when it cannot be determined. | [optional] [default to undefined]
**is_lite_speed_cache_enabled** | **boolean** | Whether the LiteSpeed Cache plugin is active. | [optional] [default to undefined]
**is_object_cache_enabled** | **boolean** | Whether LiteSpeed object cache is enabled. | [optional] [default to undefined]
**is_maintenance_mode_enabled** | **boolean** | Whether WordPress maintenance mode is currently enabled. | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WordPressSettingsResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WordPressSettingsResource = {
    core_version,
    is_lite_speed_cache_enabled,
    is_object_cache_enabled,
    is_maintenance_mode_enabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
