# ReachV1StoresStoreResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**store_id** | **string** | Pass this to the disconnect eCommerce store endpoint. | [optional] [default to undefined]
**business_name** | **string** |  | [optional] [default to undefined]
**domain** | **string** |  | [optional] [default to undefined]
**logo_url** | **string** |  | [optional] [default to undefined]
**version** | **string** |  | [optional] [default to undefined]
**sales_channels** | [**Array&lt;ReachV1StoresStoreResourceSalesChannelsInner&gt;**](ReachV1StoresStoreResourceSalesChannelsInner.md) | Storefronts of the store. | [optional] [default to undefined]
**connection_status** | **string** | &#x60;connected&#x60; to the profile in the path, &#x60;connected_to_other_profile&#x60; when another profile of the account holds it, or &#x60;not_connected&#x60;. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1StoresStoreResource } from '@hostinger/sdk';

const instance: ReachV1StoresStoreResource = {
    store_id,
    business_name,
    domain,
    logo_url,
    version,
    sales_channels,
    connection_status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
