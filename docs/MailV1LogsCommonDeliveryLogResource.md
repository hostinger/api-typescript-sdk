# MailV1LogsCommonDeliveryLogResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account** | **string** |  | [optional] [default to undefined]
**rcpt** | **string** |  | [optional] [default to undefined]
**rcpts** | **string** |  | [optional] [default to undefined]
**client_ip** | **string** |  | [optional] [default to undefined]
**from** | **string** |  | [optional] [default to undefined]
**nrcpt** | **string** |  | [optional] [default to undefined]
**timestamp** | **string** |  | [optional] [default to undefined]
**relay_events** | [**Array&lt;MailV1LogsCommonDeliveryLogRelayEventResource&gt;**](MailV1LogsCommonDeliveryLogRelayEventResource.md) |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**is_spam** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1LogsCommonDeliveryLogResource } from 'hostinger-api-sdk';

const instance: MailV1LogsCommonDeliveryLogResource = {
    account,
    rcpt,
    rcpts,
    client_ip,
    from,
    nrcpt,
    timestamp,
    relay_events,
    status,
    is_spam,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
