# WordPressV1InstallationsWordPressInstallationResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | WordPress installation (software) id | [optional] [default to undefined]
**username** | **string** | Hosting account username | [optional] [default to undefined]
**domain** | **string** | Domain the installation belongs to | [optional] [default to undefined]
**site_title** | **string** | WordPress site title | [optional] [default to undefined]
**url** | **string** | WordPress site URL | [optional] [default to undefined]
**directory** | **string** | Installation directory | [optional] [default to undefined]
**language** | **string** | WordPress locale | [optional] [default to undefined]
**login** | **string** | WordPress admin username | [optional] [default to undefined]
**email** | **string** | WordPress admin email | [optional] [default to undefined]
**is_valid** | **boolean** | Whether the installation is considered valid | [optional] [default to undefined]
**validation_error** | **string** | Reason the installation is invalid, if any | [optional] [default to undefined]
**created_at** | **string** | Installation creation timestamp | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1InstallationsWordPressInstallationResource } from 'hostinger-api-sdk';

const instance: WordPressV1InstallationsWordPressInstallationResource = {
    id,
    username,
    domain,
    site_title,
    url,
    directory,
    language,
    login,
    email,
    is_valid,
    validation_error,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
