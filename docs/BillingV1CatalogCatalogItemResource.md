# BillingV1CatalogCatalogItemResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Catalog item ID | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**category** | **string** |  | [optional] [default to undefined]
**metadata** | **object** | Flexible key-value storage containing category-specific metadata for the catalog item. The structure and available fields vary depending on the item category. | [optional] [default to undefined]
**prices** | [**Array&lt;BillingV1CatalogCatalogItemPriceResource&gt;**](BillingV1CatalogCatalogItemPriceResource.md) | Array of [&#x60;Billing.V1.Catalog.CatalogItemPriceResource&#x60;](#model/billingv1catalogcatalogitempriceresource) | [optional] [default to undefined]

## Example

```typescript
import { BillingV1CatalogCatalogItemResource } from 'hostinger-api-sdk';

const instance: BillingV1CatalogCatalogItemResource = {
    id,
    name,
    category,
    metadata,
    prices,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
