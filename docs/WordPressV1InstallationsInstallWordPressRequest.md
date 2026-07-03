# WordPressV1InstallationsInstallWordPressRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain of the existing website where WordPress will be installed | [default to undefined]
**site_title** | **string** | Title of the WordPress site | [default to undefined]
**language** | **string** | WordPress locale. Defaults to en_US when omitted. | [optional] [default to undefined]
**directory** | **string** | Relative directory to install WordPress into. Defaults to the website root when omitted. | [optional] [default to undefined]
**overwrite** | **boolean** | When false (default), does not replace an existing installation. If WordPress is already installed on the domain/path, the async install job fails unless true. | [optional] [default to undefined]
**auto_updates** | **string** | WordPress core auto-update policy | [optional] [default to undefined]
**version** | **string** | WordPress core version to install. If omitted, the latest core version compatible with the account vhost PHP version is selected. | [optional] [default to undefined]
**credentials** | [**WordPressV1InstallationsInstallWordPressRequestCredentials**](WordPressV1InstallationsInstallWordPressRequestCredentials.md) |  | [default to undefined]
**database** | [**WordPressV1InstallationsInstallWordPressRequestDatabase**](WordPressV1InstallationsInstallWordPressRequestDatabase.md) |  | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1InstallationsInstallWordPressRequest } from 'hostinger-api-sdk';

const instance: WordPressV1InstallationsInstallWordPressRequest = {
    domain,
    site_title,
    language,
    directory,
    overwrite,
    auto_updates,
    version,
    credentials,
    database,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
