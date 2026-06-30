# HostingV1CronJobsCronJobResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uid** | **string** | Unique identifier of the cron job. Use it to delete the cron job or fetch its output. | [optional] [default to undefined]
**username** | **string** | Username of the account that owns the cron job. | [optional] [default to undefined]
**time** | **string** | Cron schedule expression. | [optional] [default to undefined]
**command** | **string** | Command executed on the schedule. | [optional] [default to undefined]

## Example

```typescript
import { HostingV1CronJobsCronJobResource } from 'hostinger-api-sdk';

const instance: HostingV1CronJobsCronJobResource = {
    uid,
    username,
    time,
    command,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
