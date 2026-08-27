# BillingSubscriptionsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**disableAutoRenewalV1**](#disableautorenewalv1) | **DELETE** /api/billing/v1/subscriptions/{subscriptionId}/auto-renewal/disable | Disable auto-renewal|
|[**enableAutoRenewalV1**](#enableautorenewalv1) | **PATCH** /api/billing/v1/subscriptions/{subscriptionId}/auto-renewal/enable | Enable auto-renewal|
|[**getSubscriptionListV1**](#getsubscriptionlistv1) | **GET** /api/billing/v1/subscriptions | Get subscription list|
|[**renewSubscriptionV1**](#renewsubscriptionv1) | **POST** /api/billing/v1/subscriptions/{subscriptionId}/renew | Renew subscription|

# **disableAutoRenewalV1**
> BillingV1SubscriptionSubscriptionResource disableAutoRenewalV1()

Disable auto-renewal for a subscription.  Use this endpoint when disable auto-renewal for a subscription.

### Example

```typescript
import {
    BillingSubscriptionsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new BillingSubscriptionsApi(configuration);

let subscriptionId: string; //Subscription ID (default to undefined)

const { status, data } = await apiInstance.disableAutoRenewalV1(
    subscriptionId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **subscriptionId** | [**string**] | Subscription ID | defaults to undefined|


### Return type

**BillingV1SubscriptionSubscriptionResource**

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

# **enableAutoRenewalV1**
> BillingV1SubscriptionSubscriptionResource enableAutoRenewalV1()

Enable auto-renewal for a subscription.  Use this endpoint when enable auto-renewal for a subscription.

### Example

```typescript
import {
    BillingSubscriptionsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new BillingSubscriptionsApi(configuration);

let subscriptionId: string; //Subscription ID (default to undefined)

const { status, data } = await apiInstance.enableAutoRenewalV1(
    subscriptionId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **subscriptionId** | [**string**] | Subscription ID | defaults to undefined|


### Return type

**BillingV1SubscriptionSubscriptionResource**

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

# **getSubscriptionListV1**
> Array<BillingV1SubscriptionSubscriptionResource> getSubscriptionListV1()

Retrieve a list of all subscriptions associated with your account.  Use this endpoint to monitor active services and billing status.

### Example

```typescript
import {
    BillingSubscriptionsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new BillingSubscriptionsApi(configuration);

const { status, data } = await apiInstance.getSubscriptionListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<BillingV1SubscriptionSubscriptionResource>**

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

# **renewSubscriptionV1**
> BillingV1OrderOrderResource renewSubscriptionV1()

Create a renewal order for an existing Hostinger subscription.  This endpoint places a renewal order for a single subscription, leveraging the existing billing infrastructure. Use the [subscriptions endpoint](#tag/billing-subscriptions) to look up the `subscriptionId` values available for renewal.  If no payment method is provided, your default payment method will be used automatically.  Use this endpoint to renew any subscription available in your account.

### Example

```typescript
import {
    BillingSubscriptionsApi,
    Configuration,
    BillingV1SubscriptionRenewalRenewRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new BillingSubscriptionsApi(configuration);

let subscriptionId: string; //Subscription ID (default to undefined)
let billingV1SubscriptionRenewalRenewRequest: BillingV1SubscriptionRenewalRenewRequest; // (optional)

const { status, data } = await apiInstance.renewSubscriptionV1(
    subscriptionId,
    billingV1SubscriptionRenewalRenewRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billingV1SubscriptionRenewalRenewRequest** | **BillingV1SubscriptionRenewalRenewRequest**|  | |
| **subscriptionId** | [**string**] | Subscription ID | defaults to undefined|


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

