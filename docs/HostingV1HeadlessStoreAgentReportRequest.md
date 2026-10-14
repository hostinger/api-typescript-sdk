# HostingV1HeadlessStoreAgentReportRequest

Headless build report (report.schema.json v1), as written by the headless skill at the end of a run. Send the report unchanged.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema_version** | **string** | Report schema version | [default to undefined]
**generated_at** | **string** | When the report was written | [default to undefined]
**consent** | [**HostingV1HeadlessStoreAgentReportRequestConsent**](HostingV1HeadlessStoreAgentReportRequestConsent.md) |  | [default to undefined]
**run** | [**HostingV1HeadlessStoreAgentReportRequestRun**](HostingV1HeadlessStoreAgentReportRequestRun.md) |  | [default to undefined]
**info** | [**HostingV1HeadlessStoreAgentReportRequestInfo**](HostingV1HeadlessStoreAgentReportRequestInfo.md) |  | [default to undefined]
**timing** | [**HostingV1HeadlessStoreAgentReportRequestTiming**](HostingV1HeadlessStoreAgentReportRequestTiming.md) |  | [default to undefined]
**tokens** | **object** | Token usage, only when the tool reports its own usage | [default to undefined]
**issues** | **Array&lt;object&gt;** | Problems hit during the run | [default to undefined]
**user_feedback** | **Array&lt;object&gt;** | Feedback the user gave during the run | [default to undefined]
**skill_gaps** | **Array&lt;object&gt;** | Places where the skill instructions were missing or wrong | [default to undefined]
**what_went_well** | **Array&lt;object&gt;** | Things that worked well during the run | [default to undefined]
**logging_gaps** | **Array&lt;object&gt;** | Where the run log is missing or unsure | [optional] [default to undefined]
**previous_runs** | **Array&lt;object&gt;** | Earlier runs for the same website | [default to undefined]

## Example

```typescript
import { HostingV1HeadlessStoreAgentReportRequest } from '@hostinger/sdk';

const instance: HostingV1HeadlessStoreAgentReportRequest = {
    schema_version,
    generated_at,
    consent,
    run,
    info,
    timing,
    tokens,
    issues,
    user_feedback,
    skill_gaps,
    what_went_well,
    logging_gaps,
    previous_runs,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
