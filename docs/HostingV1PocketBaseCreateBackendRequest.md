# HostingV1PocketBaseCreateBackendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**superuser_email** | **string** | Email of the PocketBase superuser. Defaults to the email of the website owner. | [optional] [default to undefined]
**superuser_password** | **string** | Password for the PocketBase superuser, 10-128 characters. Leave it out to have a strong one generated. Either way it is returned once in the response and never stored. | [optional] [default to undefined]

## Example

```typescript
import { HostingV1PocketBaseCreateBackendRequest } from '@hostinger/sdk';

const instance: HostingV1PocketBaseCreateBackendRequest = {
    superuser_email,
    superuser_password,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
