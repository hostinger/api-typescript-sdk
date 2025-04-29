# BillingCatalogApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getCatalogItemListV1**](#getcatalogitemlistv1) | **GET** /api/billing/v1/catalog | Get catalog item list|

# **getCatalogItemListV1**
> Array<BillingV1CatalogCatalogItemResource> getCatalogItemListV1()

This endpoint retrieves a list of catalog items available for order.   Prices in catalog items is displayed as cents (without floating point), e.g: float `17.99` is displayed as integer `1799`.

### Example

```typescript
import {
    BillingCatalogApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new BillingCatalogApi(configuration);

const { status, data } = await apiInstance.getCatalogItemListV1();
```

### Parameters
This endpoint does not have any parameters.


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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

