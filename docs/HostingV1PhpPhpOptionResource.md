# HostingV1PhpPhpOptionResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Declared option type (e.g. bool, string) | [optional] [default to undefined]
**value** | **string** | Current value for this website | [optional] [default to undefined]
**comment** | **string** | Human-readable description | [optional] [default to undefined]
**_default** | **string** | Default value | [optional] [default to undefined]
**range** | **string** | Allowed value range or limits, when applicable | [optional] [default to undefined]
**max** | **string** | Maximum value allowed by the account hosting plan, when applicable | [optional] [default to undefined]

## Example

```typescript
import { HostingV1PhpPhpOptionResource } from 'hostinger-api-sdk';

const instance: HostingV1PhpPhpOptionResource = {
    type,
    value,
    comment,
    _default,
    range,
    max,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
