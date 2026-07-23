# MailV1LogsAccessAccessLogResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account** | **string** |  | [optional] [default to undefined]
**domain** | **string** |  | [optional] [default to undefined]
**session** | **string** |  | [optional] [default to undefined]
**protocol** | **string** |  | [optional] [default to undefined]
**remote_ip** | **string** |  | [optional] [default to undefined]
**login_time** | **string** |  | [optional] [default to undefined]
**_in** | **number** | Bytes received | [optional] [default to undefined]
**out** | **number** | Bytes sent | [optional] [default to undefined]
**deleted** | **number** |  | [optional] [default to undefined]
**expunged** | **number** |  | [optional] [default to undefined]
**trashed** | **number** |  | [optional] [default to undefined]
**logout_time** | **string** |  | [optional] [default to undefined]
**timestamp** | **string** |  | [optional] [default to undefined]
**app_name** | **string** |  | [optional] [default to undefined]
**has_deletions** | **boolean** |  | [optional] [default to undefined]
**result** | **string** |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**is_important** | **boolean** | True when the session deleted, expunged or trashed messages | [optional] [default to undefined]

## Example

```typescript
import { MailV1LogsAccessAccessLogResource } from 'hostinger-api-sdk';

const instance: MailV1LogsAccessAccessLogResource = {
    account,
    domain,
    session,
    protocol,
    remote_ip,
    login_time,
    _in,
    out,
    deleted,
    expunged,
    trashed,
    logout_time,
    timestamp,
    app_name,
    has_deletions,
    result,
    status,
    is_important,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
