# HostingV1PocketBaseBackendCreatedResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**instance_id** | **string** | PocketBase instance ID | [default to undefined]
**domain** | **string** | Website domain that serves the PocketBase API | [default to undefined]
**api_url** | **string** | Base URL of the PocketBase REST API | [default to undefined]
**admin_url** | **string** | URL of the PocketBase dashboard | [default to undefined]
**superuser_email** | **string** | Email of the superuser set up when the backend was created | [default to undefined]
**superuser_password** | **string** | Password of that superuser, generated when the request had none. Returned only here: Hostinger does not store it, so save it right away. | [default to undefined]
**state** | **string** | Live process state. The instance sleeps when idle and wakes on the first request. Usually null right after creation. | [default to undefined]
**version** | **string** | PocketBase version | [default to undefined]
**next_steps** | **Array&lt;string&gt;** | What to do next with this backend | [default to undefined]

## Example

```typescript
import { HostingV1PocketBaseBackendCreatedResource } from '@hostinger/sdk';

const instance: HostingV1PocketBaseBackendCreatedResource = {
    instance_id,
    domain,
    api_url,
    admin_url,
    superuser_email,
    superuser_password,
    state,
    version,
    next_steps,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
