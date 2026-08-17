# AgencyHostingV1PhpOptionResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | php.ini directive name. | [optional] [default to undefined]
**description** | **string** | What the directive controls. | [optional] [default to undefined]
**default_value** | **string** | Value applied when no custom value is set. | [optional] [default to undefined]
**allowed_values** | **Array&lt;string&gt;** | Values this option accepts. Null when the option accepts any value of its type. | [optional] [default to undefined]
**value** | **string** | Value currently in effect for the website. | [optional] [default to undefined]
**type** | **string** | Whether the option takes a single value or a list of values. | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1PhpOptionResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1PhpOptionResource = {
    name,
    description,
    default_value,
    allowed_values,
    value,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
