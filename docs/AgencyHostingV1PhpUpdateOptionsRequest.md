# AgencyHostingV1PhpUpdateOptionsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_options** | [**Array&lt;AgencyHostingV1PhpUpdateOptionsRequestOptionsInner&gt;**](AgencyHostingV1PhpUpdateOptionsRequestOptionsInner.md) | Option names and values. Each name must be one of the options returned by the options endpoint, and each value must satisfy that option\&#39;s allowed_values when it declares them. | [default to undefined]

## Example

```typescript
import { AgencyHostingV1PhpUpdateOptionsRequest } from '@hostinger/sdk';

const instance: AgencyHostingV1PhpUpdateOptionsRequest = {
    _options,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
