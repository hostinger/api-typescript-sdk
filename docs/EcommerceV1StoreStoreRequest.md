# EcommerceV1StoreStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [optional] [default to undefined]
**country_code** | **string** | ISO 3166-1 alpha-2 country code. | [optional] [default to undefined]
**company_email** | **string** |  | [optional] [default to undefined]
**company_name** | **string** |  | [optional] [default to undefined]
**language** | **string** | ISO 639-1 language code. | [optional] [default to undefined]
**sales_channel** | [**EcommerceV1StoreStoreRequestSalesChannel**](EcommerceV1StoreStoreRequestSalesChannel.md) |  | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1StoreStoreRequest } from 'hostinger-api-sdk';

const instance: EcommerceV1StoreStoreRequest = {
    name,
    country_code,
    company_email,
    company_name,
    language,
    sales_channel,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
