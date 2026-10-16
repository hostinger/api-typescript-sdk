# EcommerceV1ProductUpdateRequestCollectionChanges

Adds the product to or removes it from collections without touching its other collections. Send at least one collection in add or remove.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**add** | [**Array&lt;EcommerceV1ProductUpdateRequestCollectionChangesAddInner&gt;**](EcommerceV1ProductUpdateRequestCollectionChangesAddInner.md) | Collections to add the product to. Every id must exist in the store. | [optional] [default to undefined]
**remove** | [**Array&lt;EcommerceV1ProductUpdateRequestCollectionChangesAddInner&gt;**](EcommerceV1ProductUpdateRequestCollectionChangesAddInner.md) | Collections to take the product out of. Ids the product is not in are ignored. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductUpdateRequestCollectionChanges } from '@hostinger/sdk';

const instance: EcommerceV1ProductUpdateRequestCollectionChanges = {
    add,
    remove,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
