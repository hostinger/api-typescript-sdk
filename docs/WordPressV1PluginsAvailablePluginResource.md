# WordPressV1PluginsAvailablePluginResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **string** | Plugin slug used when installing the plugin | [optional] [default to undefined]
**title** | **string** | Human readable plugin name | [optional] [default to undefined]
**description** | **string** | Short plugin description | [optional] [default to undefined]
**onboarding_description_slug** | **string** | Translation slug for the onboarding description | [optional] [default to undefined]
**recommended_description_slug** | **string** | Translation slug for the recommended description | [optional] [default to undefined]
**link** | **string** | Link to the plugin page on WordPress.org | [optional] [default to undefined]
**version** | **string** | Latest available plugin version | [optional] [default to undefined]
**required_wordpress_version** | **string** | Minimum WordPress version required by the plugin | [optional] [default to undefined]
**required_php_version** | **string** | Minimum PHP version required by the plugin | [optional] [default to undefined]
**is_plan_upgrade_needed** | **boolean** | Whether a hosting plan upgrade is required to use the plugin | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1PluginsAvailablePluginResource } from 'hostinger-api-sdk';

const instance: WordPressV1PluginsAvailablePluginResource = {
    slug,
    title,
    description,
    onboarding_description_slug,
    recommended_description_slug,
    link,
    version,
    required_wordpress_version,
    required_php_version,
    is_plan_upgrade_needed,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
