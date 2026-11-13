# GPUV1MetricsMetricsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **number** | Unix timestamp of the measurement | [optional] [default to undefined]
**cpu_percentage** | **number** | CPU utilisation in percent | [optional] [default to undefined]
**memory_used** | **number** | Used memory in bytes | [optional] [default to undefined]
**gpu_percentage** | **number** | GPU utilisation in percent | [optional] [default to undefined]
**gpu_memory_used** | **number** | Used GPU memory in bytes | [optional] [default to undefined]
**gpu_tflops** | **number** | GPU throughput in TFLOPS | [optional] [default to undefined]

## Example

```typescript
import { GPUV1MetricsMetricsResource } from '@hostinger/sdk';

const instance: GPUV1MetricsMetricsResource = {
    timestamp,
    cpu_percentage,
    memory_used,
    gpu_percentage,
    gpu_memory_used,
    gpu_tflops,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
