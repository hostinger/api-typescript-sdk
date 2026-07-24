# WordPressV1InstallationsWordPressMcpInstallationResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | WordPress installation (software) id | [optional] [default to undefined]
**username** | **string** | Hosting account username | [optional] [default to undefined]
**domain** | **string** | Domain the installation belongs to | [optional] [default to undefined]
**directory** | **string** | Installation directory on the server | [optional] [default to undefined]
**mcp_details** | [**WordPressV1InstallationsWordPressMcpDetailsResource**](WordPressV1InstallationsWordPressMcpDetailsResource.md) |  | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1InstallationsWordPressMcpInstallationResource } from 'hostinger-api-sdk';

const instance: WordPressV1InstallationsWordPressMcpInstallationResource = {
    id,
    username,
    domain,
    directory,
    mcp_details,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
