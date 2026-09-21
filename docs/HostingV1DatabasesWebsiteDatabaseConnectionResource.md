# HostingV1DatabasesWebsiteDatabaseConnectionResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Database name, as written into DB_NAME | [default to undefined]
**user** | **string** | Database user, as written into DB_USER | [default to undefined]
**host** | **string** | MySQL host as written into DB_HOST. The application connects over the loopback. | [default to undefined]
**port** | **number** | MySQL port as written into DB_PORT | [default to undefined]

## Example

```typescript
import { HostingV1DatabasesWebsiteDatabaseConnectionResource } from '@hostinger/sdk';

const instance: HostingV1DatabasesWebsiteDatabaseConnectionResource = {
    name,
    user,
    host,
    port,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
