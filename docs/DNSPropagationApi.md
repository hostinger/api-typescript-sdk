# DNSPropagationApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**checkDNSRecordPropagationV1**](#checkdnsrecordpropagationv1) | **GET** /api/dns/v1/propagation/{domain}/{type} | Check DNS record propagation|

# **checkDNSRecordPropagationV1**
> DNSV1PropagationPropagationReportResource checkDNSRecordPropagationV1()

Check whether a DNS record of a domain or host name has propagated to public resolvers around the world.  `authoritative` shows what the domain\'s authoritative nameservers serve now. It is the best signal of the current record value. Its TTL tells how long resolvers may keep serving the old value.  `vantage_points` shows what public resolvers at different locations return. `is_propagated` is true when the location returns the same records as the authoritative nameservers. For GeoDNS domains, whose nameservers answer differently by region, true means the location returned a record. A records served from the Hostinger CDN count as propagated. When every responding authoritative nameserver returns no records, `is_propagated` is true.  Works for any domain or host name, either a domain or a subdomain. Read-only: it changes nothing.  A 404 response with error code 2025 can also mean the check could not be completed, for example when the DNS checker is busy or timed out. It is safe to retry after a short delay.

### Example

```typescript
import {
    DNSPropagationApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DNSPropagationApi(configuration);

let domain: string; //Domain or host name to check, either a domain or a subdomain (default to undefined)
let type: string; //DNS record type to check. One of: A, AAAA, CNAME, MX, SRV, TXT, CAA (default to undefined)

const { status, data } = await apiInstance.checkDNSRecordPropagationV1(
    domain,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain or host name to check, either a domain or a subdomain | defaults to undefined|
| **type** | [**string**] | DNS record type to check. One of: A, AAAA, CNAME, MX, SRV, TXT, CAA | defaults to undefined|


### Return type

**DNSV1PropagationPropagationReportResource**

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
|**404** | Error response |  -  |
|**422** | Validation error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

