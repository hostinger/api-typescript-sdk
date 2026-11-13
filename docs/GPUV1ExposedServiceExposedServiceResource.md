# GPUV1ExposedServiceExposedServiceResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Exposed service ID | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**hostname** | **string** | Public hostname or IP address of the service | [optional] [default to undefined]
**internal_port** | **number** | Port the service listens on inside the instance | [optional] [default to undefined]
**external_port** | **number** | Public port the service is reachable on | [optional] [default to undefined]
**protocol** | **string** |  | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { GPUV1ExposedServiceExposedServiceResource } from '@hostinger/sdk';

const instance: GPUV1ExposedServiceExposedServiceResource = {
    id,
    name,
    hostname,
    internal_port,
    external_port,
    protocol,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
