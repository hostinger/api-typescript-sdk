# HostingV1DatabasesDatabaseResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Database name. | [optional] [default to undefined]
**user** | **string** | Database user. | [optional] [default to undefined]
**domain** | **string** | Domain assigned to the database, or null when the database is unassigned. | [optional] [default to undefined]
**permissions** | **object** | Database user permissions keyed by permission name. | [optional] [default to undefined]
**created_at** | **string** | Database creation date in ISO 8601 format. | [optional] [default to undefined]
**updated_at** | **string** | Database last update date in ISO 8601 format. | [optional] [default to undefined]
**disk_usage_mb** | **number** | Current database disk usage in megabytes. | [optional] [default to undefined]
**max_size_mb** | **number** | Maximum allowed database size in megabytes. | [optional] [default to undefined]

## Example

```typescript
import { HostingV1DatabasesDatabaseResource } from 'hostinger-api-sdk';

const instance: HostingV1DatabasesDatabaseResource = {
    name,
    user,
    domain,
    permissions,
    created_at,
    updated_at,
    disk_usage_mb,
    max_size_mb,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
