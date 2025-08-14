# BillingSubscriptionsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**cancelSubscriptionV1**](#cancelsubscriptionv1) | **DELETE** /api/billing/v1/subscriptions/{subscriptionId} | Cancel subscription|
|[**getSubscriptionListV1**](#getsubscriptionlistv1) | **GET** /api/billing/v1/subscriptions | Get subscription list|

# **cancelSubscriptionV1**
> CommonSuccessEmptyResource cancelSubscriptionV1(billingV1SubscriptionCancelRequest)

Cancel a subscription and stop any further billing.  Use this endpoint when users want to terminate active services.

### Example

```typescript
import {
    BillingSubscriptionsApi,
    Configuration,
    BillingV1SubscriptionCancelRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new BillingSubscriptionsApi(configuration);

let subscriptionId: string; //Subscription ID (default to undefined)
let billingV1SubscriptionCancelRequest: BillingV1SubscriptionCancelRequest; //

const { status, data } = await apiInstance.cancelSubscriptionV1(
    subscriptionId,
    billingV1SubscriptionCancelRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billingV1SubscriptionCancelRequest** | **BillingV1SubscriptionCancelRequest**|  | |
| **subscriptionId** | [**string**] | Subscription ID | defaults to undefined|


### Return type

**CommonSuccessEmptyResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success empty response |  -  |
|**422** | Validation error response |  -  |
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
} from 'hostinger-api-sdk';

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

