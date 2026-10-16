# EcommerceV1ProductUpdateRequestSeoSettings

Search-engine settings to change. Send at least one field; omitted fields keep their current values.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | Search-engine title for the product page. | [optional] [default to undefined]
**description** | **string** | Search-engine description for the product page. | [optional] [default to undefined]
**slug** | **string** | URL slug of the product page. Lowercase letters, digits and dashes. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductUpdateRequestSeoSettings } from '@hostinger/sdk';

const instance: EcommerceV1ProductUpdateRequestSeoSettings = {
    title,
    description,
    slug,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
