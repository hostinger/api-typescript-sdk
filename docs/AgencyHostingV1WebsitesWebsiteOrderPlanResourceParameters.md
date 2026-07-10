# AgencyHostingV1WebsitesWebsiteOrderPlanResourceParameters

Plan parameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**disk_quota_bytes** | **number** | Disk quota in bytes | [optional] [default to undefined]
**inode_quota** | **number** | Inode quota | [optional] [default to undefined]
**cpu_cores** | **number** | CPU cores | [optional] [default to undefined]
**memory_quota_bytes** | **number** | Memory quota in bytes | [optional] [default to undefined]
**disk_iops_quota** | **number** | Disk IOPs quota | [optional] [default to undefined]
**process_quota** | **number** | Process quota | [optional] [default to undefined]
**website_quota** | **number** | Website quota | [optional] [default to undefined]
**max_databases_per_website** | **number** | Maximum number of databases per website | [optional] [default to undefined]
**is_cdn_available** | **boolean** | Is CDN available | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesWebsiteOrderPlanResourceParameters } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesWebsiteOrderPlanResourceParameters = {
    disk_quota_bytes,
    inode_quota,
    cpu_cores,
    memory_quota_bytes,
    disk_iops_quota,
    process_quota,
    website_quota,
    max_databases_per_website,
    is_cdn_available,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
