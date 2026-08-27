# EcommerceV1SalesChannelStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Sales channel type. \&quot;custom\&quot; is a headless channel: it requires a name and takes an optional public url. \&quot;quick-link\&quot; is a one-page store whose handle is auto-generated; it supports neither name nor url. | [default to undefined]
**name** | **string** | Merchant-facing custom name. Required for custom channels; not supported for quick-link. | [optional] [default to undefined]
**url** | **string** | Optional public url for the channel. Custom channels only; not supported for quick-link. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1SalesChannelStoreRequest } from '@hostinger/sdk';

const instance: EcommerceV1SalesChannelStoreRequest = {
    type,
    name,
    url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
