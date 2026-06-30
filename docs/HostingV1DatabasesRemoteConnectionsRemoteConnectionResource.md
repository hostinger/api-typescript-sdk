# HostingV1DatabasesRemoteConnectionsRemoteConnectionResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**database_name** | **string** | Full name of the database the rule applies to. | [optional] [default to undefined]
**database_user** | **string** | Database user the rule applies to. | [optional] [default to undefined]
**ip** | **string** | Allowed remote host: an IPv4/IPv6 address, or \&quot;%\&quot; for any host. | [optional] [default to undefined]

## Example

```typescript
import { HostingV1DatabasesRemoteConnectionsRemoteConnectionResource } from 'hostinger-api-sdk';

const instance: HostingV1DatabasesRemoteConnectionsRemoteConnectionResource = {
    database_name,
    database_user,
    ip,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
