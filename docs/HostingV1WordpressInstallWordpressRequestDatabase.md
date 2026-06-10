# HostingV1WordpressInstallWordpressRequestDatabase

Optional. If the named database already exists, it will be used for this WordPress install. Otherwise a new database is created with a generated name and random credentials.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Database name (username prefix added if missing) | [optional] [default to undefined]
**password** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { HostingV1WordpressInstallWordpressRequestDatabase } from 'hostinger-api-sdk';

const instance: HostingV1WordpressInstallWordpressRequestDatabase = {
    name,
    password,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
