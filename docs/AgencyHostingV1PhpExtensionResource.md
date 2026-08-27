# AgencyHostingV1PhpExtensionResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | PHP extension name. | [optional] [default to undefined]
**description** | **string** | What the extension provides. | [optional] [default to undefined]
**state** | **string** | Whether the extension is currently enabled. Extensions in the \&quot;built-in\&quot; state are compiled into PHP and cannot be turned off. | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1PhpExtensionResource } from '@hostinger/sdk';

const instance: AgencyHostingV1PhpExtensionResource = {
    name,
    description,
    state,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
