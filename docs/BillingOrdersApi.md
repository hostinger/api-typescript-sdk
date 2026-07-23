# BillingOrdersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createPurchaseOrderV1**](#createpurchaseorderv1) | **POST** /api/billing/v1/orders | Create purchase order|

# **createPurchaseOrderV1**
> BillingV1OrderOrderResource createPurchaseOrderV1(billingV1OrderPurchaseRequest)

Create a purchase order for any Hostinger product.  This unified endpoint places an order for one or more catalog items and works across all Hostinger products, leveraging the existing billing infrastructure. Use the [catalog endpoint](#tag/billing-catalog) to look up the `item_id` values available for purchase.  If no payment method is provided, your default payment method will be used automatically.  This endpoint only places the order. Product-specific provisioning (e.g. VPS setup or domain registration) is not performed here — once the order completes, use the relevant product endpoints or [hPanel](https://hpanel.hostinger.com/) to finalize setup.  Use this endpoint to purchase any product available in the catalog.

### Example

```typescript
import {
    BillingOrdersApi,
    Configuration,
    BillingV1OrderPurchaseRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new BillingOrdersApi(configuration);

let billingV1OrderPurchaseRequest: BillingV1OrderPurchaseRequest; //

const { status, data } = await apiInstance.createPurchaseOrderV1(
    billingV1OrderPurchaseRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billingV1OrderPurchaseRequest** | **BillingV1OrderPurchaseRequest**|  | |


### Return type

**BillingV1OrderOrderResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

