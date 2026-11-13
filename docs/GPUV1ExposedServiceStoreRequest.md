# GPUV1ExposedServiceStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Service name, unique within the instance | [default to undefined]
**internal_port** | **number** | Port the service listens on inside the instance, unique within the instance | [default to undefined]
**protocol** | **string** |  | [default to undefined]
**type** | **string** |  | [default to undefined]

## Example

```typescript
import { GPUV1ExposedServiceStoreRequest } from '@hostinger/sdk';

const instance: GPUV1ExposedServiceStoreRequest = {
    name,
    internal_port,
    protocol,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
