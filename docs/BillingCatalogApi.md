# BillingCatalogApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getCatalogItemListV1**](#getcatalogitemlistv1) | **GET** /api/billing/v1/catalog | Get catalog item list|

# **getCatalogItemListV1**
> Array<BillingV1CatalogCatalogItemResource> getCatalogItemListV1()

Retrieve catalog items available for order.  Prices in catalog items is displayed as cents (without floating point), e.g: float `17.99` is displayed as integer `1799`.  Use this endpoint to view available services and pricing before placing orders.

### Example

```typescript
import {
    BillingCatalogApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new BillingCatalogApi(configuration);

let category: 'DOMAIN' | 'VPS'; //Filter catalog items by category (optional) (default to undefined)
let name: string; //Filter catalog items by name. Use `*` for wildcard search, e.g. `.COM*` to find .com domain (optional) (default to undefined)

const { status, data } = await apiInstance.getCatalogItemListV1(
    category,
    name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **category** | [**&#39;DOMAIN&#39; | &#39;VPS&#39;**]**Array<&#39;DOMAIN&#39; &#124; &#39;VPS&#39;>** | Filter catalog items by category | (optional) defaults to undefined|
| **name** | [**string**] | Filter catalog items by name. Use &#x60;*&#x60; for wildcard search, e.g. &#x60;.COM*&#x60; to find .com domain | (optional) defaults to undefined|


### Return type

**Array<BillingV1CatalogCatalogItemResource>**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

