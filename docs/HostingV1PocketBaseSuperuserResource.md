# HostingV1PocketBaseSuperuserResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Website domain that serves the PocketBase API | [default to undefined]
**superuser_email** | **string** | Email of the superuser that was created or got the new password | [default to undefined]
**superuser_password** | **string** | The new password of that superuser, generated when the request had none. Hostinger does not store it and will not show it again, so save it right away. | [default to undefined]

## Example

```typescript
import { HostingV1PocketBaseSuperuserResource } from '@hostinger/sdk';

const instance: HostingV1PocketBaseSuperuserResource = {
    domain,
    superuser_email,
    superuser_password,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
