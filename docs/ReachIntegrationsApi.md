# ReachIntegrationsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**connectAIWebsiteBuilderSiteV1**](#connectaiwebsitebuildersitev1) | **POST** /api/reach/v1/profiles/{profileUuid}/websites/website-builder | Connect AI Website Builder site|
|[**disconnectAIWebsiteBuilderSiteV1**](#disconnectaiwebsitebuildersitev1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/websites/website-builder | Disconnect AI Website Builder site|
|[**disconnectEcommerceStoreV1**](#disconnectecommercestorev1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/ecommerce/stores/{storeId} | Disconnect Ecommerce store|
|[**disconnectWordPressSiteV1**](#disconnectwordpresssitev1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/websites/wordpress | Disconnect WordPress site|
|[**listConnectedWebsitesV1**](#listconnectedwebsitesv1) | **GET** /api/reach/v1/profiles/{profileUuid}/websites | List connected websites|
|[**listEcommerceStoresV1**](#listecommercestoresv1) | **GET** /api/reach/v1/profiles/{profileUuid}/ecommerce/stores | List Ecommerce stores|

# **connectAIWebsiteBuilderSiteV1**
> CommonSuccessEmptyResource connectAIWebsiteBuilderSiteV1(reachV1WebsitesWebsiteBuilderConnectRequest)

Connect an AI Website Builder site the customer built manually to the profile, so its subscribers flow into Reach.  Fails with not found when the customer owns no AI Website Builder site with that domain. Fails with `DOMAIN_ALREADY_EXISTS` when the domain is connected to any profile - to move a site to another plan, disconnect it from the old profile first - and with `WEBSITE_CONNECTION_ALREADY_EXISTS` when this profile already has an AI Website Builder site. The eCommerce store selling on the site, if it is not connected anywhere, is connected too. WordPress sites and sites made with the agentic AI Website Builder cannot be connected here.

### Example

```typescript
import {
    ReachIntegrationsApi,
    Configuration,
    ReachV1WebsitesWebsiteBuilderConnectRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachIntegrationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1WebsitesWebsiteBuilderConnectRequest: ReachV1WebsitesWebsiteBuilderConnectRequest; //

const { status, data } = await apiInstance.connectAIWebsiteBuilderSiteV1(
    profileUuid,
    reachV1WebsitesWebsiteBuilderConnectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1WebsitesWebsiteBuilderConnectRequest** | **ReachV1WebsitesWebsiteBuilderConnectRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


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
|**401** | Unauthenticated response |  -  |
|**422** | Validation error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disconnectAIWebsiteBuilderSiteV1**
> CommonSuccessEmptyResource disconnectAIWebsiteBuilderSiteV1(reachV1WebsitesWebsiteBuilderDisconnectRequest)

Disconnect an AI Website Builder site from the profile; the site stops sending subscribers to Reach.  Take `domain` from the list connected websites endpoint. Works for a site that was already deleted in the builder. Fails with not found when the domain is not connected to this profile. Contacts and any connected eCommerce store stay. The site stays disconnected until it is connected again, so confirm the site and the plan with the customer before calling.

### Example

```typescript
import {
    ReachIntegrationsApi,
    Configuration,
    ReachV1WebsitesWebsiteBuilderDisconnectRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachIntegrationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1WebsitesWebsiteBuilderDisconnectRequest: ReachV1WebsitesWebsiteBuilderDisconnectRequest; //

const { status, data } = await apiInstance.disconnectAIWebsiteBuilderSiteV1(
    profileUuid,
    reachV1WebsitesWebsiteBuilderDisconnectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1WebsitesWebsiteBuilderDisconnectRequest** | **ReachV1WebsitesWebsiteBuilderDisconnectRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


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

# **disconnectEcommerceStoreV1**
> CommonSuccessEmptyResource disconnectEcommerceStoreV1()

Disconnect an eCommerce store from the profile.  Reach stops receiving the store\'s customers and orders, and its products and coupons are removed from Reach; contacts and past orders stay. Take `store_id` from the list eCommerce stores endpoint; for a store that is `connected_to_other_profile`, call this with that profile. Also succeeds when the store is not connected to this profile, so success is not proof that anything was disconnected. Confirm the store and the plan with the customer before calling.

### Example

```typescript
import {
    ReachIntegrationsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachIntegrationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let storeId: string; //Hostinger eCommerce store ID, as returned by the eCommerce stores list (default to undefined)

const { status, data } = await apiInstance.disconnectEcommerceStoreV1(
    profileUuid,
    storeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **storeId** | [**string**] | Hostinger eCommerce store ID, as returned by the eCommerce stores list | defaults to undefined|


### Return type

**CommonSuccessEmptyResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success empty response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disconnectWordPressSiteV1**
> CommonSuccessEmptyResource disconnectWordPressSiteV1(reachV1WebsitesWordPressDisconnectRequest)

Disconnect a WordPress site from the profile.  The Reach plugin on the site stops sending subscribers and store data, and the site\'s products and coupons are removed from Reach; contacts and past orders stay. Take `domain` from the list connected websites endpoint. Fails with not found when the domain is not connected to this profile. This cannot be undone through the API - the customer reconnects from the WordPress plugin - so confirm the site and the plan with the customer before calling.

### Example

```typescript
import {
    ReachIntegrationsApi,
    Configuration,
    ReachV1WebsitesWordPressDisconnectRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachIntegrationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1WebsitesWordPressDisconnectRequest: ReachV1WebsitesWordPressDisconnectRequest; //

const { status, data } = await apiInstance.disconnectWordPressSiteV1(
    profileUuid,
    reachV1WebsitesWordPressDisconnectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1WebsitesWordPressDisconnectRequest** | **ReachV1WebsitesWordPressDisconnectRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


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

# **listConnectedWebsitesV1**
> Array<ReachV1WebsitesWebsiteResource> listConnectedWebsitesV1()

Get the websites connected to the profile, each with its `domain` and `platform_type`.  A domain is connected to at most one profile, so to find which plan a site is on, call this for each profile. Only connected sites are listed, not every website the customer owns, and eCommerce stores are not included - use the list eCommerce stores endpoint for those. Pass `domain` to the disconnect WordPress site or disconnect AI Website Builder site endpoint.

### Example

```typescript
import {
    ReachIntegrationsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachIntegrationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.listConnectedWebsitesV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**Array<ReachV1WebsitesWebsiteResource>**

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

# **listEcommerceStoresV1**
> Array<ReachV1StoresStoreResource> listEcommerceStoresV1()

Get all of the customer\'s Hostinger eCommerce stores, each with its `store_id` and `connection_status` for the profile in the path.  A store is connected to at most one profile. `connected_to_other_profile` does not name that profile - call this for each profile to find it. The list is empty, not an error, when the eCommerce service cannot be reached. Pass `store_id` to the disconnect eCommerce store endpoint. Connecting an AI Website Builder site connects the store selling on it.

### Example

```typescript
import {
    ReachIntegrationsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachIntegrationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.listEcommerceStoresV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**Array<ReachV1StoresStoreResource>**

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

