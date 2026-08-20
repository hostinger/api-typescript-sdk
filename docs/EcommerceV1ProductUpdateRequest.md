# EcommerceV1ProductUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The product name. | [optional] [default to undefined]
**description** | **string** | The product description. | [optional] [default to undefined]
**status** | **string** | Set \&quot;published\&quot; to make the product buyable, \&quot;draft\&quot; to hide it, or \&quot;archived\&quot; to retire it. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductUpdateRequest } from 'hostinger-api-sdk';

const instance: EcommerceV1ProductUpdateRequest = {
    name,
    description,
    status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
