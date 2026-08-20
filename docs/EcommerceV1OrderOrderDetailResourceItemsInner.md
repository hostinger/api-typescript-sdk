# EcommerceV1OrderOrderDetailResourceItemsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The line item ID, required by the fulfil endpoint. | [optional] [default to undefined]
**title** | **string** | The line item title. | [optional] [default to undefined]
**sku** | **string** | The variant SKU. | [optional] [default to undefined]
**variant_id** | **string** | The variant ID. | [optional] [default to undefined]
**quantity** | **number** | Quantity ordered. | [optional] [default to undefined]
**fulfilled_quantity** | **number** | Quantity already fulfilled. | [optional] [default to undefined]
**returned_quantity** | **number** | Quantity returned. | [optional] [default to undefined]
**unit_price** | **number** | Unit price in the smallest currency unit. | [optional] [default to undefined]
**total** | **number** | Line total in the smallest currency unit. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1OrderOrderDetailResourceItemsInner } from 'hostinger-api-sdk';

const instance: EcommerceV1OrderOrderDetailResourceItemsInner = {
    id,
    title,
    sku,
    variant_id,
    quantity,
    fulfilled_quantity,
    returned_quantity,
    unit_price,
    total,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
