# GPUV1PoolPoolInstanceResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | GPU pool instance type ID | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**cpu_cores** | **number** | Number of CPU cores | [optional] [default to undefined]
**ram** | **number** | Total RAM in bytes | [optional] [default to undefined]
**storage** | **number** | Total storage in bytes | [optional] [default to undefined]
**price_per_hour** | **number** | Hourly price in cents (USD) | [optional] [default to undefined]

## Example

```typescript
import { GPUV1PoolPoolInstanceResource } from '@hostinger/sdk';

const instance: GPUV1PoolPoolInstanceResource = {
    id,
    name,
    description,
    cpu_cores,
    ram,
    storage,
    price_per_hour,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
