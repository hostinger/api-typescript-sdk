# HostingV1PocketBaseInstanceResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**instance_id** | **string** | PocketBase instance ID | [default to undefined]
**domain** | **string** | Website domain that serves the PocketBase API | [default to undefined]
**api_url** | **string** | Base URL of the PocketBase REST API | [default to undefined]
**admin_url** | **string** | URL of the PocketBase dashboard | [default to undefined]
**state** | **string** | Live process state. The instance sleeps when idle and wakes on the first request. Null when the server could not be reached. | [default to undefined]
**failure_reason** | **string** | Why the last start did not succeed, set only while &#x60;state&#x60; is &#x60;failed&#x60;. &#x60;process_limit&#x60; means the hosting account has no free process slots, usually because its Node.js apps are running; &#x60;start_failed&#x60; is any other cause. | [default to undefined]
**retry_after_seconds** | **number** | Seconds until Hostinger tries to start the instance again, set only while &#x60;state&#x60; is &#x60;failed&#x60;. Null when the next try is due now. | [default to undefined]
**version** | **string** | PocketBase version | [default to undefined]
**disk_usage_kb** | **number** | Disk space used by the instance data, in KB | [default to undefined]

## Example

```typescript
import { HostingV1PocketBaseInstanceResource } from '@hostinger/sdk';

const instance: HostingV1PocketBaseInstanceResource = {
    instance_id,
    domain,
    api_url,
    admin_url,
    state,
    failure_reason,
    retry_after_seconds,
    version,
    disk_usage_kb,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
