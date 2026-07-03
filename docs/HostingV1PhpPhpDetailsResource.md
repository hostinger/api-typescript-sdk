# HostingV1PhpPhpDetailsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**php_version** | **string** | Current PHP version name | [optional] [default to undefined]
**php_version_full** | **string** | Full PHP version name | [optional] [default to undefined]
**php_versions** | [**HostingV1PhpPhpVersionsResource**](HostingV1PhpPhpVersionsResource.md) |  | [optional] [default to undefined]
**_options** | [**{ [key: string]: HostingV1PhpPhpOptionResource; }**](HostingV1PhpPhpOptionResource.md) | PHP options keyed by option name | [optional] [default to undefined]
**extensions** | **object** | PHP extensions keyed by extension name | [optional] [default to undefined]
**conflicting_extensions** | **Array&lt;Array&lt;string&gt;&gt;** | Groups of extensions that conflict with each other | [optional] [default to undefined]

## Example

```typescript
import { HostingV1PhpPhpDetailsResource } from 'hostinger-api-sdk';

const instance: HostingV1PhpPhpDetailsResource = {
    php_version,
    php_version_full,
    php_versions,
    _options,
    extensions,
    conflicting_extensions,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
