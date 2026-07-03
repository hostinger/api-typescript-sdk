# EcommerceMiscellaneousApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getCustomStorefrontSetupInstructionsV1**](#getcustomstorefrontsetupinstructionsv1) | **GET** /api/ecommerce/v1/miscellaneous/custom-storefront-instructions | Get custom storefront setup instructions|

# **getCustomStorefrontSetupInstructionsV1**
> EcommerceV1MiscellaneousCustomStorefrontInstructionsResource getCustomStorefrontSetupInstructionsV1()

Retrieve step-by-step setup instructions, formatted as Markdown, for connecting a custom sales channel to your store and keeping your catalog, orders, shipping and payments in sync through the Ecommerce API.

### Example

```typescript
import {
    EcommerceMiscellaneousApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceMiscellaneousApi(configuration);

const { status, data } = await apiInstance.getCustomStorefrontSetupInstructionsV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**EcommerceV1MiscellaneousCustomStorefrontInstructionsResource**

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

