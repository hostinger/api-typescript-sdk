# EcommerceV1OrderFulfillRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**Array&lt;EcommerceV1OrderFulfillRequestItemsInner&gt;**](EcommerceV1OrderFulfillRequestItemsInner.md) | Line items to fulfil. Omit to fulfil every remaining unfulfilled item. | [optional] [default to undefined]
**tracking_number** | **string** | Carrier tracking number for the shipment. | [optional] [default to undefined]
**tracking_url** | **string** | Public tracking URL for the shipment. Requires tracking_number. | [optional] [default to undefined]
**notify_customer** | **boolean** | Whether to email the customer about the fulfilment. Defaults to true. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1OrderFulfillRequest } from 'hostinger-api-sdk';

const instance: EcommerceV1OrderFulfillRequest = {
    items,
    tracking_number,
    tracking_url,
    notify_customer,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
