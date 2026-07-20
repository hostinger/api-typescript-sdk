# AgencyHostingV1WebsitesCronJobsCronJobResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | Unique identifier of the cron job. Use it to delete the cron job. | [optional] [default to undefined]
**time** | **string** | Cron schedule expression. | [optional] [default to undefined]
**command** | **string** | Command executed on the configured schedule. | [optional] [default to undefined]
**created_at** | **string** | Cron job creation timestamp. | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesCronJobsCronJobResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesCronJobsCronJobResource = {
    uuid,
    time,
    command,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
