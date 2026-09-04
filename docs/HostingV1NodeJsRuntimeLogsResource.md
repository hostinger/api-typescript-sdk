# HostingV1NodeJsRuntimeLogsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**logs** | [**Array&lt;HostingV1NodeJsLogEntryResource&gt;**](HostingV1NodeJsLogEntryResource.md) | Array of [&#x60;Hosting.V1.NodeJs.LogEntryResource&#x60;](#model/hostingv1nodejslogentryresource) | [default to undefined]
**started_at** | **string** | Timestamp of the first line of the log file; null when the file is empty or its first line has no timestamp field | [default to undefined]
**total_lines** | **number** | Total number of lines in the raw log file. Send total_lines + 1 as from_line in the next poll to receive only new entries. | [default to undefined]
**last_deployed_at** | **string** | Time of the last completed build; entries before it belong to the previous deployment. null when no build has completed yet. | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsRuntimeLogsResource } from '@hostinger/sdk';

const instance: HostingV1NodeJsRuntimeLogsResource = {
    logs,
    started_at,
    total_lines,
    last_deployed_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
