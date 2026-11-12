# HostingV1PocketBaseBackendResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**instance_id** | **string** | PocketBase instance ID | [default to undefined]
**domain** | **string** | Website domain that serves the PocketBase API | [default to undefined]
**api_url** | **string** | Base URL of the PocketBase REST API | [default to undefined]
**admin_url** | **string** | URL of the PocketBase dashboard | [default to undefined]
**state** | **string** | Live process state. The instance sleeps when idle and wakes on the first request. Null when the server could not be reached. | [default to undefined]
**version** | **string** | PocketBase version | [default to undefined]
**next_steps** | **Array&lt;string&gt;** | What to do next with this backend | [default to undefined]

## Example

```typescript
import { HostingV1PocketBaseBackendResource } from '@hostinger/sdk';

const instance: HostingV1PocketBaseBackendResource = {
    instance_id,
    domain,
    api_url,
    admin_url,
    state,
    version,
    next_steps,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
