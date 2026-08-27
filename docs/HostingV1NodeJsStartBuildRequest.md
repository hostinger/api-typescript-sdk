# HostingV1NodeJsStartBuildRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_version** | **number** | Node.js version | [default to undefined]
**app_type** | **string** | Node.js application type | [default to undefined]
**root_directory** | **string** | Application root directory (where package.json is located) relative to public_html | [default to undefined]
**output_directory** | **string** | Build output directory relative to the root directory | [default to undefined]
**build_script** | **string** | Build script that will be ran to build the application | [default to undefined]
**entry_file** | **string** | The main entry point file for the application | [optional] [default to undefined]
**package_manager** | **string** | Package manager | [optional] [default to undefined]
**source_type** | **string** | The source type of the files | [default to undefined]
**source_options** | [**HostingV1NodeJsStartBuildRequestSourceOptions**](HostingV1NodeJsStartBuildRequestSourceOptions.md) |  | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsStartBuildRequest } from '@hostinger/sdk';

const instance: HostingV1NodeJsStartBuildRequest = {
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
