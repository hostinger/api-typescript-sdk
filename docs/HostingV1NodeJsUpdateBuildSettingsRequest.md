# HostingV1NodeJsUpdateBuildSettingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_version** | **number** | Node.js major version | [default to undefined]
**app_type** | **string** | Node.js application framework. Set it explicitly when auto-detection picked the wrong one. | [optional] [default to undefined]
**root_directory** | **string** | Application root directory (where package.json is located) relative to public_html. Omit it, or send \&quot;.\&quot;, for public_html itself. | [optional] [default to undefined]
**output_directory** | **string** | Build output directory relative to the root directory | [optional] [default to undefined]
**build_script** | **string** | The package.json script that builds the application | [optional] [default to undefined]
**entry_file** | **string** | The main entry point file for the application (required for express, fastify, nest, nuxt and hono app types) | [optional] [default to undefined]
**package_manager** | **string** | Package manager used to install dependencies | [optional] [default to undefined]

## Example

```typescript
import { HostingV1NodeJsUpdateBuildSettingsRequest } from '@hostinger/sdk';

const instance: HostingV1NodeJsUpdateBuildSettingsRequest = {
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
