# AgencyHostingV1OrdersResourceUsageMetricsWebsiteResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uid** | **string** | Website UID | [optional] [default to undefined]
**domains** | **Array&lt;string&gt;** | Domains associated with the website | [optional] [default to undefined]
**metrics** | [**Array&lt;AgencyHostingV1OrdersResourceUsageMetricsMetricResource&gt;**](AgencyHostingV1OrdersResourceUsageMetricsMetricResource.md) | Array of [&#x60;AgencyHosting.V1.Orders.ResourceUsageMetrics.MetricResource&#x60;](#model/agencyhostingv1ordersresourceusagemetricsmetricresource) | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1OrdersResourceUsageMetricsWebsiteResource } from '@hostinger/sdk';

const instance: AgencyHostingV1OrdersResourceUsageMetricsWebsiteResource = {
    uid,
    domains,
    metrics,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
