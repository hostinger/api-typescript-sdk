# HorizonsV1WebsitesBuildTaskResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The build task ID, used with the &#x60;Get website build task&#x60; tool | [default to undefined]
**state** | **string** | The build state. &#x60;TASK_STATE_SUBMITTED&#x60; and &#x60;TASK_STATE_WORKING&#x60; mean the build is still running. &#x60;TASK_STATE_COMPLETED&#x60; means it finished. &#x60;TASK_STATE_FAILED&#x60; means it broke, and &#x60;TASK_STATE_REJECTED&#x60; means it never started: the website does not contain the requested changes. &#x60;TASK_STATE_CANCELED&#x60; means the user stopped it; changes made before that may be kept. | [default to undefined]
**updated_at** | **string** | When the build last changed state | [optional] [default to undefined]
**reason_code** | **string** | Why the build stopped, or null. &#x60;insufficient_credits&#x60;: the user has no credits left; &#x60;execution_error&#x60; or &#x60;missing_result&#x60;: the build broke; &#x60;iteration_limit&#x60;: the build stopped early and kept the work done so far. | [optional] [default to undefined]
**message** | **string** | Guidance to tell the user about the build outcome, or null | [optional] [default to undefined]
**summary** | **string** | An internal changelog entry describing what the build changed, or null until the build ends. Rewrite it in plain language before showing it to the user. | [optional] [default to undefined]

## Example

```typescript
import { HorizonsV1WebsitesBuildTaskResource } from '@hostinger/sdk';

const instance: HorizonsV1WebsitesBuildTaskResource = {
    id,
    state,
    updated_at,
    reason_code,
    message,
    summary,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
