# HostingV1PocketBaseUpdateSuperuserRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**superuser_email** | **string** | Email of the superuser to create or update. Defaults to the email of the website owner. | [optional] [default to undefined]
**superuser_password** | **string** | New password of the PocketBase superuser, 10-128 characters. Leave it out to have a strong one generated. Either way it is returned once in the response and never stored. | [optional] [default to undefined]

## Example

```typescript
import { HostingV1PocketBaseUpdateSuperuserRequest } from '@hostinger/sdk';

const instance: HostingV1PocketBaseUpdateSuperuserRequest = {
    superuser_email,
    superuser_password,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
