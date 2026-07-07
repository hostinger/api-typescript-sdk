# WordPressV1InstallationsVersionResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **string** | Installed WordPress core version | [optional] [default to undefined]
**vulnerabilities** | [**Array&lt;WordPressV1CommonVulnerabilityResource&gt;**](WordPressV1CommonVulnerabilityResource.md) | Known vulnerabilities affecting the installed core version | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1InstallationsVersionResource } from 'hostinger-api-sdk';

const instance: WordPressV1InstallationsVersionResource = {
    version,
    vulnerabilities,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
