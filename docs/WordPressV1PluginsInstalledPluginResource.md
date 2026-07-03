# WordPressV1PluginsInstalledPluginResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Plugin slug | [optional] [default to undefined]
**title** | **string** | Human readable plugin name | [optional] [default to undefined]
**version** | **string** | Installed plugin version | [optional] [default to undefined]
**status** | **string** | Whether the plugin is active or inactive | [optional] [default to undefined]
**update** | **string** | Available update version, or \&quot;none\&quot; when up to date | [optional] [default to undefined]
**vulnerabilities** | [**Array&lt;WordPressV1CommonVulnerabilityResource&gt;**](WordPressV1CommonVulnerabilityResource.md) | Known vulnerabilities affecting the installed version | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1PluginsInstalledPluginResource } from 'hostinger-api-sdk';

const instance: WordPressV1PluginsInstalledPluginResource = {
    name,
    title,
    version,
    status,
    update,
    vulnerabilities,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
