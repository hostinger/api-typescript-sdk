# AgencyHostingV1DatacentersDatacenterResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | Datacenter title | [default to undefined]
**code** | **string** | Datacenter code | [default to undefined]
**country** | **string** | Datacenter country code | [default to undefined]
**coordinates** | [**AgencyHostingV1DatacentersCoordinatesResource**](AgencyHostingV1DatacentersCoordinatesResource.md) |  | [default to undefined]
**pinger_url** | **string** | URL you can ping to measure round-trip latency to this datacenter. Compare the measured latency across datacenters to identify the nearest one (lowest ping) for your website. Null when no online server is currently available to measure against. | [default to undefined]

## Example

```typescript
import { AgencyHostingV1DatacentersDatacenterResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1DatacentersDatacenterResource = {
    title,
    code,
    country,
    coordinates,
    pinger_url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
