# EcommerceV1SalesChannelStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Sales channel type. Only \&quot;custom\&quot; channels can be created via the API. | [default to undefined]
**name** | **string** | Merchant-facing custom name shown in the sales channels list. | [default to undefined]
**url** | **string** | Optional public address where the custom sales channel lives. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1SalesChannelStoreRequest } from 'hostinger-api-sdk';

const instance: EcommerceV1SalesChannelStoreRequest = {
    type,
    name,
    url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
