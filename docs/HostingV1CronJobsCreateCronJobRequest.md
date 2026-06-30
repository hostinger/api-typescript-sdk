# HostingV1CronJobsCreateCronJobRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**time** | **string** | Cron schedule expression (for example \&quot;0 2 * * *\&quot; runs daily at 02:00). | [default to undefined]
**command** | **string** | Command to execute on the schedule. | [default to undefined]

## Example

```typescript
import { HostingV1CronJobsCreateCronJobRequest } from 'hostinger-api-sdk';

const instance: HostingV1CronJobsCreateCronJobRequest = {
    time,
    command,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
