# HostingV1NodeJsBuildOptionsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_version** | **number** | Node.js version | [default to undefined]
**app_type** | **string** | Node.js application type | [default to undefined]
**root_directory** | **string** | Application root directory | [default to undefined]
**output_directory** | **string** | Build output directory | [default to undefined]
**build_script** | **string** | The npm script to run to build the application | [default to undefined]
**entry_file** | **string** | The main entry point file for the application | [default to undefined]
**package_manager** | **string** | Package manager | [default to undefined]
**source_type** | **string** | Source type for the build | [default to undefined]
**source_options** | [**HostingV1NodeJsSourceOptionsResource**](HostingV1NodeJsSourceOptionsResource.md) |  | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsBuildOptionsResource } from 'hostinger-api-sdk';

const instance: HostingV1NodeJsBuildOptionsResource = {
    node_version,
    app_type,
    root_directory,
    output_directory,
    build_script,
    entry_file,
    package_manager,
    source_type,
    source_options,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
