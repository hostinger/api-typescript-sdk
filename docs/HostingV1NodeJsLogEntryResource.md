# HostingV1NodeJsLogEntryResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **string** | ISO 8601 timestamp of the log entry | [default to undefined]
**level** | **string** | Log level in upper case (usually ERROR, WARN, INFO, LOG, DEBUG or TRACE). Numeric pino levels are mapped to these names. | [default to undefined]
**message** | **string** | Log message | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsLogEntryResource } from '@hostinger/sdk';

const instance: HostingV1NodeJsLogEntryResource = {
    timestamp,
    level,
    message,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
