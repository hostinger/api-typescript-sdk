# HostingV1NodeJsStoredBuildSettingsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_version** | **number** | Node.js major version used to build and run the application | [default to undefined]
**app_type** | **string** | Detected or chosen application framework | [default to undefined]
**root_directory** | **string** | Application root directory (where package.json is located) relative to public_html; null means public_html itself | [default to undefined]
**output_directory** | **string** | Build output directory relative to the root directory | [default to undefined]
**build_script** | **string** | The package.json script that builds the application | [default to undefined]
**entry_file** | **string** | The main entry point file for the application | [default to undefined]
**package_manager** | **string** | Package manager used to install dependencies | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsStoredBuildSettingsResource } from '@hostinger/sdk';

const instance: HostingV1NodeJsStoredBuildSettingsResource = {
    node_version,
    app_type,
    root_directory,
    output_directory,
    build_script,
    entry_file,
    package_manager,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
