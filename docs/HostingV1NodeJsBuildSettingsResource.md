# HostingV1NodeJsBuildSettingsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app_type** | **string** | Node.js application type | [default to undefined]
**node_version** | **number** | Node.js version | [default to undefined]
**root_directory** | **string** | Application root directory | [default to undefined]
**output_directory** | **string** | Build output directory | [default to undefined]
**build_script** | **string** | The npm script to run to build the application | [default to undefined]
**entry_file** | **string** | The main entry point file for the application | [default to undefined]
**package_manager** | **string** | Package manager | [default to undefined]
**available_scripts** | **Array&lt;string&gt;** | The scripts configured in the package.json file | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsBuildSettingsResource } from '@hostinger/sdk';

const instance: HostingV1NodeJsBuildSettingsResource = {
    app_type,
    node_version,
    root_directory,
    output_directory,
    build_script,
    entry_file,
    package_manager,
    available_scripts,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
