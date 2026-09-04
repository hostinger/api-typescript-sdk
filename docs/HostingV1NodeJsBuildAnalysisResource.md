# HostingV1NodeJsBuildAnalysisResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**analysis** | **string** | Why the build failed. null when no analysis could be produced. | [default to undefined]
**solution** | **string** | Suggested fix for the build failure. null when no analysis could be produced. | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsBuildAnalysisResource } from '@hostinger/sdk';

const instance: HostingV1NodeJsBuildAnalysisResource = {
    analysis,
    solution,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
