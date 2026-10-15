# AgentReadinessV1ScansScanResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name that was scanned | [default to undefined]
**status** | **string** | Scan status. Result fields are null until the status is &#x60;completed&#x60;. | [default to undefined]
**score** | **number** | Agent readiness score from 0 to 100. Null unless completed, and null when unreachable. | [default to undefined]
**grade** | **string** | Letter grade for the score, from &#x60;A&#x60; to &#x60;F&#x60;. Null unless completed, and null when unreachable. | [default to undefined]
**is_unreachable** | **boolean** | Whether the website homepage could not be fetched | [default to undefined]
**scanner_version** | **number** | Version of the scoring method that produced this scan | [default to undefined]
**is_outdated** | **boolean** | Whether the scan was produced by an older scoring method than the current one | [default to undefined]
**scanned_at** | **string** | When the scan finished. Null unless completed. | [default to undefined]
**categories** | [**AgentReadinessV1ScansCategoriesResource**](AgentReadinessV1ScansCategoriesResource.md) |  | [default to undefined]
**unassessed_categories** | **Array&lt;string&gt;** | Categories where no check could be counted. They still cost their full weight. Null unless completed. | [default to undefined]
**results** | [**Array&lt;AgentReadinessV1ScansCheckResultResource&gt;**](AgentReadinessV1ScansCheckResultResource.md) | Result of every check. Null unless completed. | [default to undefined]

## Example

```typescript
import { AgentReadinessV1ScansScanResource } from '@hostinger/sdk';

const instance: AgentReadinessV1ScansScanResource = {
    domain,
    status,
    score,
    grade,
    is_unreachable,
    scanner_version,
    is_outdated,
    scanned_at,
    categories,
    unassessed_categories,
    results,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
