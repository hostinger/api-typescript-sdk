# AgencyHostingV1WebsitesCronJobsCreateCronJobRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**time** | **string** | Cron schedule expression (standard 5-field crontab syntax). | [default to undefined]
**command** | **string** | Command to run on the schedule. Must not contain pipe (|) or redirection (&lt;, &gt;) characters. | [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesCronJobsCreateCronJobRequest } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesCronJobsCreateCronJobRequest = {
    time,
    command,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
