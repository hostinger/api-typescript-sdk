# WordPressV1InstallationsCheckIsValidRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**software_ids** | **Array&lt;string&gt;** | WordPress installation (software) identifiers to validate. | [default to undefined]
**force** | **boolean** | Force fresh validation without cache. Preferable for troubleshooting purposes. | [optional] [default to false]

## Example

```typescript
import { WordPressV1InstallationsCheckIsValidRequest } from 'hostinger-api-sdk';

const instance: WordPressV1InstallationsCheckIsValidRequest = {
    software_ids,
    force,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
