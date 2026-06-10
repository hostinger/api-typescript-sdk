# HostingV1NodeJsCreateFromArchiveRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**archive** | **string** | Project archive file (.zip, .tar.gz, or .tgz), maximum 50MB | [default to undefined]
**node_version** | **number** | Node.js version override (auto-detected from package.json if omitted) | [optional] [default to undefined]
**app_type** | **string** | Node.js application type override | [optional] [default to undefined]
**root_directory** | **string** | Application root directory override (where package.json is located) relative to public_html | [optional] [default to undefined]
**output_directory** | **string** | Build output directory override relative to the root directory | [optional] [default to undefined]
**build_script** | **string** | Build script override | [optional] [default to undefined]
**entry_file** | **string** | Main entry point file override | [optional] [default to undefined]
**package_manager** | **string** | Package manager override | [optional] [default to undefined]

## Example

```typescript
import { HostingV1NodeJsCreateFromArchiveRequest } from 'hostinger-api-sdk';

const instance: HostingV1NodeJsCreateFromArchiveRequest = {
    archive,
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
